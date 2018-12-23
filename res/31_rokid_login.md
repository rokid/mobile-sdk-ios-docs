# 若琪账号体系

## 登录流程

1、流程

![](media/rokid_login.png)

2、接口

参数说明

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| phoneNum  | String | 是 | 手机号 |
| passwd   | String | 否 | 密码 |

**举个大栗子：**

Swift:

```swift
// token 有些平台没有
RokidMobileSDK.account.login(phoneNum: String, passwd: String, complete:((RKError?) -> Void))
```

