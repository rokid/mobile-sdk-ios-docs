# 设备模块 Device
## 更新当前设备的昵称

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| deviceId | String | 是 | 设备Id |
| newNick | String | 是 | 新昵称 |
| completion |   | 是 | 结果回调 |

**接口定义**

Swift:

```swift
RokidMobileSDK.device.updateNick(deviceId: String, newNick: String, completion: @escaping (_ error: RKError?) -> Void)
```

Objc:

```objc
[RokidMobileSDK.device updateNickWithDeviceId:self.device.id newNick:@"XXX" completion:^(RKError * error) {
    // ...
}];
```

---

