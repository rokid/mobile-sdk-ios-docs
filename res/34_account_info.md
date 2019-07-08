
# 获取用户信息

**接口定义**


```objc
[RokidMobileSDK.account fetchUserInfoWithCompletion:^(RKError * error, SDKUserInfo * userInfo) {
        if (error == nil) {
            NSLog(@"user info nickname = %@, birth = %@, gender = %@, userId = %@", userInfo.nickname, userInfo.birthday, userInfo.gender, userInfo.userId);
        }
}];
```

## SDKUserInfo
| 字段    | 类型   | 说明 |
| ------ | ----- | ----- |
| birthday | String | 生日 “2019/07/08” |
| userId | String | 用户 id |
| nickname | String | 用户昵称 |
| gender | String | 用户性别 如：“male” ”female“ |

# 更新用户信息

**接口定义**

```objc
[RokidMobileSDK.account updateUserInfoWithNickname:@"rokiddemo"
                                                gender:@"male"
                                              birthday:@"2014/11/26"
                                            completion:^(RKError * error) {
                                                if (error == nil) {
                                                    
                                                }
                                            }];
```

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| nickname | String | 是 | 用户昵称 |
| gender | String | 是 | 用户性别 如：“male” ”female“ |
| birthday | String | 是 | 生日 如：“2019/07/08” |


## Token

接口说明：获取用户登录的 Token

**示例代码：**

Swift:

```swift
RokidMobileSDK.account.token()
```

Objc:

```objc
[RokidMobileSDK.account token];
```

---

## UserId

接口说明：获取用户登录的 userId

Swift:

```swift
RokidMobileSDK.account.userId()
```

Objc:

```objc
[RokidMobileSDK.account userId];
```