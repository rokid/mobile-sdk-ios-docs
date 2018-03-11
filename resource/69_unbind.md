# 设备模块 Device
## 解绑设备

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| deviceId | String | 是 | 设备Id |
| completion |   | 是 | 结果回调 |

**接口定义**

Swift:

```swift
RokidMobileSDK.device.unbindDevice(deviceId: String, completion: @escaping (_ error: RKError?) -> Void)
```

Objc:

```objc
[RokidMobileSDK.device unbindDeviceWithDeviceId:self.device.id completion:^(RKError * error) {
    // ...
}];
```

---


