# 配网模块 Binder
## 蓝牙配网

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| binderData | DevicebinderData | 是 | 蓝牙发送信息 |

**示例代码**

Swift:

```swift
RokidMobileSDK.binder?.sendBLEBindWifi(device: RKBLEDevice, ssid: String, password, bssid, completion)
```

Objc:

```objc
[RokidMobileSDK.binder sendBLEBindWifiWithDevice:device ssid:@"xxx" password:@"xxx" bssid:@"xxx" completion:^(RKError * error) {
    // ...
}];
```

---

