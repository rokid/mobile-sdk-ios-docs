# 流程

![register_flow](media/rokid_register.png)


# 获取验证码

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| areaCode | String | 是 | 国际区号采用中国国际区号：”+86“ |
| phoneNum | String | 是 | 待注册的手机号 |

```objc
[RokidMobileSDK.account getScodeWithAreaCode:@"+86"
                                        phoneNum:@"your phone number"
                                      completion:^(RKError * error) {
                                          if (error == nil) {
                                              //
                                          } else {
                                              // toast error message
                                              NSLog(@"error = %@", error.message);
                                          }
                                      }];
```

# 校验验证码

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| phoneNum | String | 是 | 待注册的手机号 |
| scode | String | 是 | 验证码 |

```objc
[RokidMobileSDK.account checkScodeWithPhoneNum:@"your phone number"
                                             scode:@"your scode number"
                                        completion:^(RKError * error) {
                                            if (error == nil) {
                                                
                                            } else {
                                                // toast error message
                                                NSLog(@"error = %@", error.message);
                                                
                                            }
                                        }];
```


# 注册

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| password | String | 是 | 密码 |
| scode | String | 是 | 验证码 |
| areaCode | String | 是 | 国际区号采用中国国际区号：”+86“ |

```objc
[RokidMobileSDK.account registerWithPhoneNum:@"your phone number"
                                        password:@"your password"
                                           scode:@"your scode number"
                                        areaCode:@"+86"
                                      completion:^(RKError * error) {
                                          
                                          if (error == nil) {
                                              
                                              NSLog(@"succeed: 注册成功，请登录");
                                              

                                          } else {
                                              // toast error message
                                              NSLog(@"error = %@", error.message);
                                          }
                                      }];
```