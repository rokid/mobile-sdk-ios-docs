# 配网模块 Binder
## 开启蓝牙扫描

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| type | String | 是 | 设备名称类型前缀 |

**示例代码**

Swift:

```swift
RokidMobileSDK.binder.startBLEScan(type: String, onNewDeviceCallback: (BTDevice)->Void) ->RKError?
```

Objc:

```objc
[RokidMobileSDK.binder startBLEScanWithType:@"Rokid-Pebble-" onDeviceChange:^(NSArray<RKBLEDevice *> * devices) {
    //...
}];
```

---

## 停止蓝牙扫描

**示例代码**

Swift:

```swift
RokidMobileSDK.binder.stopBLEScan()
```

Objc:

```objc
[RokidMobileSDK.binder stopBLEScan]
```

---

