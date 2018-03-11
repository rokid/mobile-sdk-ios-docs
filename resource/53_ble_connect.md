# 配网模块 Binder
## 连接设备

**接口说明** 接口需传入蓝牙名称（蓝牙address重启后会变）

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| name | String | 是 | 设备名称 |

**示例代码**

Swift:

```swift
RokidMobileSDK.binder.connectBLEDevice(device: RKBLEDevice, complete:(RKError?)->Void) {
    // ...
}
```

Objc:

```objc
[RokidMobileSDK.binder connectBLEDevice:device complete:^(BOOL result, NSError * error) {
    // ...
}];
```

---

