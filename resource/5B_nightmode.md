# # 设备模块 Device
## 1、获取设备夜间模式

 **接口说明**
 获取设备夜间模式

 **示例代码**：
 
 Swift:

```swift
RokidMobileSDK.device.getNightMode(device: RKDevice, completion: @escaping (_ error: RKError?, _ nightMode: SDKDeviceNightMode?) -> Void)
```

Objc:
 
 ```objc
 RKDevice * device = [RokidMobileSDK.device getCurrentDevice];
            
[RokidMobileSDK.device getNightModeWithDevice:device completion:^(RKError * error, SDKDeviceNightMode * nightMode) {
            /// TODO
}];
 ```

---
 
## 2、更新设备夜间模式

 **接口说明**
 更新设备夜间模式
 
 **参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| device | RKDevice | 是 | 设备 |

SDKDeviceNightMode 对象结构如下:

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| state | SDKDeviceNightModeState | 是 | open: 打开夜间模式; </br> close: 关闭夜间模式 |
| startTime | String | 是 | 开始时间 |
| endTime | String | 是 | 终止时间 |

 **示例代码**：
 
 Swift:
 
 ```swift
 let device = RokidMobileSDK.device.getCurrentDevice()
 let nightMode = SDKDeviceNightMode()
 nightMode.state = .open
 nightMode.startTime = "23:00"
 nightMode.endTime = "7:00"
 
 RokidMobileSDK.device.updateNightMode(device: device,
                                      nightmode: nightMode,
                                      completion: @escaping Completion) {
 ```
 
 Objc:
 
 ```objc
 RKDevice * device = [RokidMobileSDK.device getCurrentDevice];
 SDKDeviceNightMode * nightMode = [SDKDeviceNightMode init];
 nightMode.state = SDKDeviceNightModeStateOpen;
 nightMode.startTime = @"23:00";
 nightMode.endTime = @"7:00";
            
 [RokidMobileSDK.device updateNightModeWithDevice:device nightmode:nightMode completion:^(RKError * error, RKDevice * device) {
                // TODO 处理回调
 }];
 ```


