# 设备模块 Device

## 获取 设备基本信息
设备基本信息 包括：ip、局域网ip、mac、nick、cy、sn、version

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| deviceId | String | 是 | 设备Id |

**接口定义**

```swift
RokidMobileSDK.device.getBasicInfo(deviceId: String) -> [String: Any]?
```

---


