# Mobile SDK 调试

开发者可以 切换到 测试环境，并打印一些日志用于分析问题。

## 测试环境

开启 Debug 开发，切换到测试环境。

**示例代码：**

Swift:

```swift
RokidMobileSDK.shared.debug = true
```

Objc:

```objc
RokidMobileSDK.shared.debug = true;
```

---

## 开启日志

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


