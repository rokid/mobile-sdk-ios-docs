通用通知消息

消息体

ChannelMessage
 
例子

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



