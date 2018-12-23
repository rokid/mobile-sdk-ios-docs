# SDK 通知

## 流程

![](media/event.png)

## 接口

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


