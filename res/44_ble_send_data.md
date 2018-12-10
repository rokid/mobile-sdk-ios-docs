# 配网模块 Binder

## 蓝牙配网

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| wifi | RKWiFi | 是 | 蓝牙发送Wifi信息 |

**示例代码**

Swift:

```swift
// 获取 手机当前连接的 WIFI
var wifi: RKWiFi = RKWiFi.current()
RokidMobileSDK.binder?.sendWiFi(device: device, wifi: wifi, password:"123456")
```

Objc:

```objc
// 自定义 WIFI 信息 
RKWiFi *wifi = [[RKWiFi alloc] initWithSsid:"wifi_test" bssid:@""];
                                          
[RokidMobileSDK.binder sendWiFiWithDevice:device wifi: wifi password:@"123456"];
```

---


## 配网状态

设备配网过程中，状态判断。

需要 在 SDKBinderObserver 实现类中的 onBLEDeviceBindStateUpdated() 函数 获取蓝牙开启状态。

Swift

```swift
public class CustomBinderObserver: SDKBinderObserver {
    
    func onBLEDeviceBindStateUpdated(device: RKBLEDevice, response: RKBLEResponse) {
        switch response.sCode {
        case "10":  //连接wifi中
                // ...
            break
        case "11":  //wifi连接成功
                // ...
            break
        // ...
        }
    }
}
```

### 状态值判断

| 状态值 | 说明 | 备注 |
| --- | --- | --- |
| 10 | wifi连接中 ||
| 11 | wifi连接成功 ||
| -11 | wifi密码错误 ||
| -12 | wifi连接超时 ||
| -13 | 没找到当前wifi ||
| -14 | wifi密码长度不正确 ||
| -98 | 运营商网络错误 ||
| 100 | 登录中 ||
| 101 | 登录成功 ||
| -101 | 登录失败 ||
| 200 | 绑定中 ||
| 201 | 绑定成功 ||
| -201 | 绑定失败 ||

