# 配网模块 Binder
## 蓝牙配网

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| binderData | DevicebinderData | 是 | 蓝牙发送信息 |

**示例代码**

Swift:

```swift
let binderData: DevicebinderData = DevicebinderData()
binderData.wifiPwd("your wifiPwd")     //wifi密码（可以为空）
binderData.wifiSsid("your wifiSsid")   //wifi名字（可以为空）
binderData.wifiBssid("your wifiBssid") //wifi地址（可以为空）

RokidMobileSDK.binder.sendBLEBinderData(binderData: DevicebinderData, complete: (RKError?)->Void)
```

---

