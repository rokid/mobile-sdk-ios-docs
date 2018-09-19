# 设备配置信息 Device

## 1、获取设备配置信息

根据业务需求获取设备 配置的各种信息。

参数说明

| 字段 | 类型 | 必须 | 备注 |
| --- | --- | --- | --- |
| device | RKDevice | 是 | 设备 |
| namespace | String | 是 | 存储空间、根据业务填写 |
| key | String | 是 | 信息存储Key |

**示例代码**

 Swift:

```swift
RokidMobileSDK.device.getServiceInfo(device: RKDevice, namespace: String,
                                     key: String,
                                     completion: @escaping (_ error: RKError?, _ value: String?) -> Void) {
                                     }
```

## 2、存储、更新设备信息

| 字段 | 类型 | 必须 | 备注 |
| --- | --- | --- | --- |
| device | RKDevice | 是 | 设备 |
| namespace | String | 是 | 存储空间、根据业务填写 |
| kvMapString | String | 是 | 信息存储信息键值对 转换成的 JsonString  |

**示例代码**

 Swift:

```swift
storeServiceInfo(device: RKDevice,
                                       namespace: String,
                                       key: String,
                                       kvMapString: String,
                                       completion: @escaping (_ error: RKError?) -> Void) {
                                       
                                       }
```


