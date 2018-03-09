# 设备模块 Device
## 1、设置当前设备(本地缓存)

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| device | RKDevice | 是 | 设备Entity |

**接口定义**

Swift:

```swift
RokidMobileSDK.device.setCurrentDevice(device: RKDevice)
```

---

## 2、获取当前设备(本地缓存)

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |

**接口定义**

Swift:

```swift
RokidMobileSDK.device.getCurrentDevice() -> RKDevice?
```

---

