# 配网模块 Binder
## 开启蓝牙扫描

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| blePrefix | String | 是 | 设备名称类型前缀 |

**示例代码**

Swift:

```swift
RokidMobileSDK.binder.startBLEScan(blePrefix: String) ->Bool
```

Objc:

```objc
[RokidMobileSDK.binder startBLEScanWithBlePrefix:@"Rokid-"];
```

<font color="red">手机蓝牙未打开时，扫描接口会返回 false</font>

---

## 停止蓝牙扫描

**示例代码**

Swift:

```swift
RokidMobileSDK.binder.stopScan()
```

Objc:

```objc
[RokidMobileSDK.binder stopScan]
```

---

