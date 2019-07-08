# 修改密码

**参数说明**

登录之后才能修改密码

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| oldPassword | String | 是 | 旧密码 |
| newPassword | String | 是 | 新密码 |

```objc
[RokidMobileSDK.account changePasswdWithOldPassword:@"your old pwd"  
                                        newPassword:@"your new pwd" 
                                        completion:^(RKError * _Nullable error) {
            if (error) {
                // toast error message
                NSLog(@"error = %@", error.message);
                [MBProgressHUD showMessage:error.message to:self.view afterDelay:1.8];
            }else {
                [MBProgressHUD showMessage:@"密码修改成功" to:self.view afterDelay:1.8];
            }
        }];
```


# 重置密码

**参数说明**

用于忘记密码时候的登录，该接口调用成功后，用重置之后的新密码就可以进行登录了。

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| phoneNum | String | 是 | 旧密码 |
| password | String | 是 | 新密码 |
| scode | String | 是 | 验证码, 需要调用获取验证码接口以获取验证码 |

```objc
[RokidMobileSDK.account resetPasswdWithPhoneNum:@"your phoneNum"
                                        password:@"your pwd"
                                            scode:@"your scode"
                                        completion:^(RKError * _Nullable error) {
                                            if (error) {
                                                // toast error message
                                                NSLog(@"error = %@", error.message);
                                                [MBProgressHUD showMessage:error.message to:self.view afterDelay:1.8];
                                            }else {
                                                [MBProgressHUD showMessage:@"密码重置成功" to:self.view afterDelay:1.8];
                                            }
                                        }];
```