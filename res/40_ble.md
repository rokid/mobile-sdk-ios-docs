# 绑定模块 Binder

### 绑定模式

绑定模块 主要提供给 搭载了 Rokid服务的设备进行配置网络环境。

Mobile SDK 提供了蓝牙配网 API，使用观察者模式，所以使用之前，请 实现如下接口，并添加到 RokidMobileSDK.binder 中。

请确认 APP 是否开通蓝牙权限。

### 配网流程

![](media/binder.png)

### 配网模块观察者

实现这个观察者可以获取整个配网过程中的回调和状态。

**示例代码**

Swift:

```swift
public class CustomBinder: SDKBinderObserver {
    
    init() {
        // 注入观察者
        RokidMobileSDK.binder.addObserver(self)
    }
    
    /// 手机蓝牙状态变更，用户是开起来了蓝牙功能
    func onBLEEnabled(_ isEnable: Bool) {
    }
    
    /// 检测到的设备列表更新
    func onBLEDeviceListChanged(list: [RKBLEDevice]) {
    }
    
    /// 连接设备
    func onBLEDeviceConnected(device: RKBLEDevice) {
    }
    
    /// 连接设备失败
    func onBLEDeviceConnectFailed(device: RKBLEDevice, error: NSError) {
    }
    
    /// 断开设备连接
    func onBLEDeviceDisconnected(device: RKBLEDevice) {
    }
    
    /// 设备Wi-Fi列表更新
    func onBLEDeviceWiFiListUpdated(device: RKBLEDevice, response: RKBLEResponse) {
    }
    
    /// 发送Wi-Fi账号密码成功
    func onBLEDeviceSendWiFiSuccessed(device: RKBLEDevice) {
    }
    
    /// 发送Wi-Fi账号密码失败
    func onDeviceSendWiFiFailed(device: RKBLEDevice) {
    }
    
    /// 设备联网状态更新了
    func onBLEDeviceBindStateUpdated(device: RKBLEDevice, response: RKBLEResponse) {
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
| 100 | 登录中 ||
| 101 | 登录成功 ||
| -101 | 登录失败 ||
| 200 | 绑定中 ||
| 201 | 绑定成功 ||
| -201 | 绑定失败 ||


