# 配网模块 Binder
## 1、获取蓝牙开启状态,未授权时先授权再check

**示例代码**

Swift:

```swift
RokidMobileSDK.binder.getBLEStatus()
```

Objc:

```objc
CBCentralManagerState state = [RokidMobileSDK.binder getBLEStatus];
```

---

## 2、监听蓝牙状态改变

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| statusChange | CBCentralManagerState) -> Void | 是 | 状态改变回调 |

**示例代码**

Swift:

```swift
RokidMobileSDK.binder.onBLEStatusChange(statusChange: @escaping (CBCentralManagerState) -> Void)
```

Objc:

```objc
[RokidMobileSDK.binder onBLEStatusChangeWithStatusChange:^(CBCentralManagerState state) {
    //...
}];
```

---


