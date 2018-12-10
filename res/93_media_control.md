# 媒体模块

## 播放

 请求参数：
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| skillId | String | 是 | 当前技能ID |
| id | String | 是 | 待播放的媒体ID |

举个大栗子：

Swift

```swift
RokidMobileSDK.media?.requestPlayIntent(skillId: "$skillId", id: "$id", completion: { (error, josn) in
    // ...
})
```

MediaWareControlData具体格式如下：

```json
{
    "deviceId": "0201021712001400",
    "masterId": "2F6CF9622BA60B9290089C3EF5C9E7E2",
    "requestId": "73d81c4134974404af9f3b967baf99fc",
    "success": true,
    "version": "3.0.0"
}
```

---

## 暂停

 请求参数：
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| skillId | String | 是 | 当前技能ID |

举个大栗子：

Swift

```swift
RokidMobileSDK.media?.requestPauseIntent(skillId: "$skillId", completion: { (error, json) in
    // ...
})
```

---

## 继续播放

 请求参数：
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| skillId | String | 是 | 当前技能ID |

举个大栗子：

Swift

```swift
RokidMobileSDK.media?.requestResumeIntent(skillId: "$skillId", completion: { (error, json) in
    // ...
})
```

---

## 上一首

 请求参数：
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| skillId | String | 是 | 当前技能ID |

举个大栗子：

Swift

```swift
RokidMobileSDK.media?.requestPreviousIntent(skillId: "$SKillId", completion: { (error, json) in
    // ...
})
```

---

## 下一首

 请求参数：
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| skillId | String | 是 | 当前技能ID |

举个大栗子：

Swift

```swift
RokidMobileSDK.media?.requestNextIntent(skillId: "$skillId", completion: { (error, json) in
    // ...
})
```


以上5个接口的需要订阅以下事件，收到事件后才表示当前的操作是真的执行成功：

Swift

```swift
// 媒体播放中
NotificationCenter.rokidsdk.addObserver(self, selector: #selector(handleMediaPlayingNotification(_:)), name: NSNotification.Name(rawValue: SDKNotificationName.MediaPlaying), object: nil)

@objc private func handleMediaPlayingNotification(_ notification: Notification) {
    // ...
}
    
// 媒体暂停
NotificationCenter.rokidsdk.addObserver(self, selector: #selector(handleMediaPausedNotification(_:)), name: NSNotification.Name(rawValue: SDKNotificationName.MediaPaused), object: nil)

@objc private func handleMediaPausedNotification(_ notification: Notification) {
    // ...
}
    
// 媒体停止
NotificationCenter.rokidsdk.addObserver(self, selector: #selector(handleMediaStoppedNotification(_:)), name: NSNotification.Name(rawValue: SDKNotificationName.MediaStopped), object: nil)

@objc private func handleMediaStoppedNotification(_ notification: Notification) {
    // ...
}
```

---

## 当前播放信息

 请求参数：
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| skillId | String | 是 | 当前技能ID |

举个大栗子：

Swift

```swift
RokidMobileSDK.media?.requestPlayInfoIntent(skillId: "$skillId", completion: { (error, json) in
    // ...
})
```

该接口需要订阅以下事件：

Swift

```swift
// 媒体播放中
NotificationCenter.rokidsdk.addObserver(self, selector: #selector(handleMediaPlayingNotification(_:)), name: NSNotification.Name(rawValue: SDKNotificationName.MediaPlaying), object: nil)

@objc private func handleMediaPlayingNotification(_ notification: Notification) {
    // ...
}
```


