# Vui 反馈 模块
## 发送TOPIC 
发送 TOPIC，就是 发送一条指定topic的message 内容。

**参数说明**
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| device | String | 是 | 需要发送的设备  |
| topic | String | 是 | 消息内容的主题  |
| text | String | 是 | 消息内容  |

**示例代码**：
 
Swift:
 
```swift
RokidMobileSDK.vui.sendMessage(topic: "topic", text: "text", to: device)
```

Objc:

```objc
 [RokidMobileSDK.vui sendMessageWithTopic:@"topic" text:@"text" to: device];
```

---

