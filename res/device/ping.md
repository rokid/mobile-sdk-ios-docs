# 设备模块 Device

## 获取设备在线状态

<font color="red">该接口目前只供使用YodaOS系统的设备类型调用</font>

**接口说明**

通过服务端获取设备当前的在线状态

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| deviceList | [RKDevice] | 是 | 设备列表 |

例子

Swift:

```swift
RokidMobileSDK.device.queryDevicesState(for: [RKDevice], completion: (_ deviceStateList: [RKQueryResClientInfo]?))
```

Objc:

```objc
[RokidMobileSDK.device queryDevicesStateFor:device_list completion:^(NSArray<RKQueryResClientInfo *> * deviceStateList) {
    // ...
}];
```


## ping设备

 **接口说明**
 获取当前设备的在线状态
 
 **参数说明**
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
|sddDevice |SDKDevice | 是 | SDKDevice|


 **示例代码**：
 
 Swift:

```swift
RokidMobileSDK.device.pingDevice(deviceId: self.device, completion: (_ error: RKError?, _ device: RKDevice?) -> Void)
```

Objc:

```objc
[RokidMobileSDK.device pingDeviceWithDevice:self.device completion:^(RKError * error, RKDevice * device) {
    // ...
}];
```
 
 ---

