# 帐号模块 Account
## 授权登陆
* 接口说明：需要传入token和用户id，再监听回调

**参数说明:**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| userId  | String | 是 | 用户id |
| token   | String | 否 | 用户登录token |

**示例代码：**

```swift
// token 有些平台没有
RokidMobileSDK.account.login(userId: String, token: String, complete:((RKError?) -> Void))
```

---

