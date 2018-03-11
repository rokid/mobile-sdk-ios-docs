# 设备模块 Device
## 通过 id 获取 device 信息

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| deviceId | String | 是 | 设备Id |

**接口定义**

Swift:

```swift
let device = RokidMobileSDK.device.getDevice(deviceId: String) -> RKDevice?
```

Objc:

```objc
RKDevice * device = [RokidMobileSDK.device getDeviceWithDeviceId:self.device.id];
```

---

