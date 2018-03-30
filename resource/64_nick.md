# 设备模块 Device

## 设置设备昵称前缀名



**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| name | String | 否 |重要：设备nick前缀，如果想要设定设备前缀名，一定要在获取设备列表之前设置该前缀； 如果不设定将是默认设备前缀名：Rokid。 也可以通过更新设备昵称修改|


**接口定义**

Swift:

```
RokidMobileSDK.device.setInitDeviceNickPrefix(name:"XXX")
```

Objc:

```
 [RokidMobileSDK.device setInitDeviceNickPrefixWithName:@"XXX"];
```

## 更新当前设备的昵称

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| deviceId | String | 是 | 设备Id |
| newNick | String | 是 | 新昵称 |
| completion |   | 是 | 结果回调 |

**接口定义**

Swift:

```swift
RokidMobileSDK.device.updateNick(deviceId: String, newNick: String, completion: @escaping (_ error: RKError?) -> Void)
```

Objc:

```objc
[RokidMobileSDK.device updateNickWithDeviceId:self.device.id newNick:@"XXX" completion:^(RKError * error) {
    // ...
}];
```

---

