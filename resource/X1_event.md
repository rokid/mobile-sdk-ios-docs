# SDK 通知

**接口定义**

Swift:

```swift
NotificationCenter.rokid.addObserver()
```

**通知定义**

通知名都定义在 RKNotificationName

| 通知名   | 说明   |
| ------ | ----- |
| .CurrentDeviceUpdated | 当前设备改变 |
| .DeviceStatusUpdated | 设备在线状态改变 |
| .DeviceListUpdated | 设备列表改变 增加或解绑 |
| .CardListUpdated | card列表改变，增加或减少 |
| .AlarmVolumeChanged | 音量变化 |
| .ShouldLogout | 被登出 |
| .ChannelMessage | 长连接完整消息 |



## 通用消息

### event名称

ChannelMessage
 
### 例子

Swift:

```swift
NotificationCenter.rokidsdk.addObserver(self, selector: #selector(handleChannelMsgsNotification(_:)), name: NSNotification.Name(rawValue: SDKNotificationName.ChannelMessages ), object: nil)

@objc private func handleChannelMsgsNotification(_ notification: Notification) {
    print("\(String(describing: notification.userInfo))")
    print("handleChannelMsgsNotification:", notification)
}
```

Objc

```objc
[NSNotificationCenter.rokidsdk addObserver:self selector:@selector(handleChannelMsgsNotification:) name:SDKNotificationName.ChannelMessage object:nil];

- (void)handleChannelMsgsNotification: (NSNotification *)notification {
    NSLog(@"%@", notification.userInfo);
    NSLog(@"handleChannelMsgsNotification %@", notification.object);
}
```

