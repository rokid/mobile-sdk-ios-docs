# 自有帐号体系

注意：

使用 自有账号体系时，开发者必须拥有自己的账号体系，如果没有请直接使用 若琪账号体系，谢谢。

## 登录流程

1、流程

![](images/rokid_login.png)

2、接口

**参数说明:**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| userId  | String | 是 | 用户id |
| token   | String | 否 | 用户登录token |

**示例代码：**

Swift:

```swift
// token 有些平台没有
RokidMobileSDK.account.thirdpartyLogin(userId: String, token: String, complete:((RKError?) -> Void))
```

Objc:

```objc
[RokidMobileSDK.account thirdpartyLoginWithUserId:@"xxx" token:@"xxx" completion:^(RKError * error) {
        if (error) {
            // ....
        }
        
        //...
    }];
```

---

