# 配网模块 Binder

## 1、获取蓝牙开启状态,未授权时先授权再check

**示例代码**

Swift:

```swift
RokidMobileSDK.binder.enableBLE()
```

Objc:

```objc
[RokidMobileSDK.binder enableBLE];
```

---

在 SDKBinderObserver 实现类中的 onBLEEnabled() 函数 获取蓝牙开启状态。

Swift:

```swift
// 手机蓝牙状态变更，用户是开起来了蓝牙功能
func onBLEEnabled(_ isEnable: Bool) {
    self.sdkObservers.forEach({$0.value?.onBLEEnabled?(isEnable)})
}
```


