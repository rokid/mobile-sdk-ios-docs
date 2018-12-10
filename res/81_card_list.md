# Vui 反馈 模块

## 获得 card 列表

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| maxDbId | Int | 是 | card 的 db id |
| pageSize | Int | 否 | 页大小 |


**接口定义**

Swift:

```swift
RokidMobileSDK.vui.getCardList(maxDbId: Int, completion: @escaping (_ error: RKError?, _ cardList: [RKCard]?) -> Void) -> Void
```

Objc:

```objc
[RokidMobileSDK.vui getCardListWithMaxDbId:0 completion:^(RKError * error, NSArray<RKCard *> * cardArray) {
    for (RKCard *card in cardArray) {
        NSLog(@"msg = %@", card.msgText);
    }
}];
```

Swift:

```swift
RokidMobileSDK.vui.getCardList(maxDbId: Int, pageSize: Int = 20, completion: @escaping (_ error: RKError?, _ cardList: [RKCard]?) -> Void) -> Void
```

Objc

```objc
[RokidMobileSDK.vui getCardListWithMaxDbId:0 pageSize:20 completion:^(RKError * error, NSArray<RKCard *> * cardArray) {
    for (RKCard *card in cardArray) {
        NSLog(@"msg = %@", card.msgText);
    }
}];
```

---

