# 设备模块 Device
## 1、获取设备的 Loaction 信息

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| deviceId | String | 是 | 设备Id |
| completion |   | 是 | 结果回调 |

**接口定义**

Swift:

```swift
RokidMobileSDK.device.getLocation(deviceId: String, completion: @escaping (_ error: RKError?, _ location: Location?) -> Void)
```

---

## 2、更新设备的 Location 信息

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| deviceId | String | 是 | 设备Id
| location | Location | 是 | 位置信息 |
| completion |   | 是 | 结果回调 |

**接口定义**

Swift:

```swift
RokidMobileSDK.device.updateLocation(deviceId: String, location: Location, completion: @escaping (_ error: RKError?) -> Void)
```

---

