# SDK 初始化
## 1、初始化

 * 异步初始化RokidMobileSDK, 请确保初始化成功，否则其余API都会失败.

 **参数说明：**

| 字段         | 类型    | 必须？| 说明 |
| :---------  | --------- | :---: | --- |
| appKey | String | 是 | Rokid 发放的 appKey |
| appSecret | String | 是 | Rokid 发放的 appSecret

**示例代码：**

Swift:

```swift
// complete: 初始化结果，成功success = true, 失败success = false
RokidMobileSDK.shared.initSDK(appKey: String,
                              appSecret: String,
                              escaping complete:(success: Bool) -> Void)
```

---

## 2、Debug 模式
开启 Debug 开发，切换到开发环境。

**示例代码：**

Swift:

```swift
RokidMobileSDK.debug()
```

---

## 3、开启日志

<font color="red">此API 未启用</font>

**示例代码：**

Swift:

```swift
// Log默认关闭
RokidMobileSDK.log.enable = true;
```

```
Log DEMO:

RokidMobileSDK:开始SDK初始化：appKey:xxxxxxxx, appSecret:yyyyyy
RokidMobileSDK:初始化0:开始验证app...
RokidMobileSDK:初始化1:开始生成本地权限...
RokidMobileSDK:初始化0：校验app成功（失败,失败原因：无效网络）
RokidMobileSDK:初始化1:SDK权限已生成，具有权限：账户管理-true、设备管理-true

RokidMobileSDK: 开始登陆: userId:xxxxxxxx, token: yyyyyy
RokidMobileSDK: 登陆成功(失败, 失败原因：token校验失败)

```

---

