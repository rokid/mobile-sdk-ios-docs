# 设备模块 Device

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
RokidMobileSDK.device.pingDevice(deviceId: self.device, 
                                 completion: @escaping (_ error: RKError?, _ device: RKDevice?) -> Void)
```

Objc:

```objc
[RokidMobileSDK.device pingDeviceWithDevice:self.device completion:^(RKError * error, RKDevice * device) {
    // ...
}];
```
 
 ---

