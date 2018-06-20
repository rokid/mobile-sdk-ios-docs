# 设备模块 Device
## 设备恢复出厂设置

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| deviceId | String | 是 | 设备Id |

**接口定义**

Swift:

```swift
let isSucceed = RokidMobileSDK.device.resetDevice(deviceId: String)
```

Objc:

```objc
BOOL isSucceed = [RokidMobileSDK.device resetDeviceWithDeviceId:self.device.id];
```

---

