# Vui 反馈 模块
## 发送TTS 
发送 TTS，就是 发送一条 能让设备立即说的 内容。

 **参数说明**
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| device | String | 是 | 需要发送的设备  |
| tts | String | 是 | 让设备说的话  |

 **示例代码**：
 
```swift
RokidMobileSDK.home.sendTts(tts: String, to device: RKDevice)
```

---

