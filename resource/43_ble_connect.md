# 绑定模块 Binder

## 连接设备

**接口说明** 
用于连接 扫描出来的蓝牙设备。

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| device | RKBLEDevice | 是 | 蓝牙设备 |

**示例代码**

Swift:

```swift
RokidMobileSDK.binder.connect(device: RKBLEDevice)
```

Objc:

```objc
[RokidMobileSDK.binder connect:device];
```

---

