# 媒体模块

## 授权交互流程

![](media/media_thirdauth.jpg)

### 获取已授权信息

参数说明：

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| type | ThirdAuth | 是 | 获取第三方授权信息标识。<br>如：SDKThirdAuthType.QQ、SDKThirdAuthType.WX |
| deviceTypeId | String | 是 | 设备类型 | 
| deviceId  | String | 是 | 设备SN | 

SDKThirdAuthToken 说明

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| access_token | String | 是 | 授权 Token | 
| expires_in | String | 是 | 有效期 | 
| refresh_token | String | 是 | 刷新所需 Token | 
| type | String | 是 | 获取第三方授权信息标识 | 

举个大栗子

Swift

```swift
RokidMobileSDK.media?.getThirdOauthToken(type: SDKThirdAuthType.QQ, deviceTypeId: "$deviceTypeId", deviceId: "$deviceId" , completion: { (error, thirdAuthToken) in
    // ...
})
```

---

### 获取 三方平台授权所需信息

参数说明：

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| type | ThirdAuth | 是 | 获取第三方授权信息标识。<br>如：SDKThirdAuthType.QQ、SDKThirdAuthType.WX  |
| deviceTypeId | String | 是 | 设备类型 | 

ThirdOauthInfoBean 说明

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| baseAppId | String | 是 |  第三方平台申请的 AppId |
| baseAppSecret | String | 是 | 第三方平台申请的 AppSecret |
| baseRedirectUri | String | 是 | 授权完成，信息上报地址 |
| callbackThirdUrl | String | 是 | 授权完成，回调地址 |

举个大栗子

Swift

```Swift
RokidMobileSDK.media?.getThirdOauthInfo(type: SDKThirdAuthType.QQ, deviceTypeId: "$deviceTypeId", completion: { (error, thirdAuthInfo) in
    // ...
})
```

---

### 解除绑定

解绑 第三方授权。

参数说明：

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| type | ThirdAuth | 是 | 获取第三方授权信息标识。<br>如：SDKThirdAuthType.QQ、SDKThirdAuthType.WX  |

举个大栗子

Swift

```Swift
RokidMobileSDK.media?.unbindThirdAuth(SDKThirdAuthType.QQ, completion: { (error) in
    // ...
}
```
 
----

