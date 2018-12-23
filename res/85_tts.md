# 发送TTS 

发送 TTS，就是 发送一条 能让设备立即说的 内容。

## 流程

![](media/vui_tts.png)

## 接口

**参数说明**
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| device | String | 是 | 需要发送的设备  |
| tts | String | 是 | 让设备说的话  |

**示例代码**：
 
Swift:
 
```swift
RokidMobileSDK.vui.sendTts(tts: String, to device: RKDevice)
```

Objc:

```objc
[RokidMobileSDK.vui sendTtsWithTts: @"XXX" to: self.device];
```

---

