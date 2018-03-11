# Vui 反馈 模块
## 发送 ASR
发送 ASR，就是 发送一条 能让设备立即执行的一条指令。

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| asr | String | 是 | ASR 内容 |
| device | RKDevice | 是 | 需要发送的设备 |

**接口定义**

Swift:

```swift
RokidMobileSDK.vui.sendAsr(asr: String, to device: RKDevice)
```

Objc:

```objc
[RokidMobileSDK.vui  sendAsrWithAsr: @"XXX" to: self.device];
```

---

