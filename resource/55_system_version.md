# 设备模块 Device

## 获取系统版本信息

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| deviceId | String | 是 | 设备Id |
| completion |   | 是 | 结果回调 |

**接口定义**

Swift:

```swift
RokidMobileSDK.device.getVersion(deviceId: String, completion: @escaping (_ error: Error?, _ versionInfo: RKDeviceVersionInfo?) -> Void )
```

Objc:

```objc
[RokidMobileSDK.device getVersionWithDeviceId:self.device.id completion:^(NSError * error, SDKDeviceVersionInfo * versionInfo) {
    // ...
}];
```

---

## 开始系统升级

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| deviceId | String | 是 | 设备Id |

**接口定义**

Swift:

```swift
let result = RokidMobileSDK.device.startSystemUpdate(deviceId: String)
```

Objc:

```objc
BOOL result = [RokidMobileSDK.device startSystemUpdateWithDeviceId:self.device.id];
```
---

