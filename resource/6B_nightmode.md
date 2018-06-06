# # 设备模块 Device
## 1、获取设备夜间模式

 **接口说明**
 获取设备夜间模式

 **示例代码**：
 
 Swift:

```swift
RokidMobileSDK.device.getNightMode(device: RKDevice, completion: @escaping (_ error: RKError?, _ nightMode: RKDeviceNightMode?) -> Void)
```
## 
---
 
## 2、更新设备夜间模式

 **接口说明**
 更新设备夜间模式
 
 **参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| device | RKDevice | 是 | 设备 |

RKDeviceNightMode 对象结构如下:

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| state | RKDeviceNightModeState | 是 | open: 打开夜间模式</br>close: |
| startTime | String | 是 | 设备ID |
| endTime | String | 是 | 设备ID |

 **示例代码**：
 
 Swift:
 
 ```swift
 RokidMobileSDK.device.updateNightMode(device: RKDevice,
                                      nightmode: RKDeviceNightMode,
                                      completion: @escaping Completion) {
 ```


