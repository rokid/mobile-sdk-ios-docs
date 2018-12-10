# 提醒 Remind

### 流程

![](media/remind.png)

### 获取提醒列表
请求获取设备上的提醒列表：

Swift:

```swift
RokidMobileSDK.skill?.remind.getList(deviceId: String,
                           completion: @escaping (_ error: RKError?, _ reminds: [SDKRemind]?) -> Void)
```

Objc:

```objc
[RokidMobileSDK.skill.remind getListWithDeviceId:self.device.id completion:^(RKError * error, NSArray<SDKRemind *> * remindArr) {
    // ... 
}];
```

SDKRemind 字段说明：

| 参数 | 类型 | 必要？ | 说明 |
| --- | --- | --- | --- |
| id |  int| 是 | 闹钟Id |
| year | int | 是 | 年 |
| month | int | 是 |  月|
| day | int | 是 | 日 |
| hour | int | 是 | 小时 |
| minute | int | 是 | 分钟 |
| content | String | 是 | 提醒内容 |

---

### 删除提醒
删除一个提醒：

Swift:

```swift
RokidMobileSDK.skill?.remind.delete(deviceId: String, remind: SDKRemind)
```

Objc:

```objc
[RokidMobileSDK.skill.remind deleteWithDeviceId:@"XXX" remind:reminder];
```

---

