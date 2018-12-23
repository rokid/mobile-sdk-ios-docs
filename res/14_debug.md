# Mobile SDK 调试

开发者可以 切换到 环境，并打印一些日志用于分析问题。

## 环境切换

调用这个 API 可以切换到 线上、预发、测试环境，方便调试开发。

参数说明

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| env  | SDKEnv | 是 | SDK环境：<br> SDKEnv.Release 线上环境;<br> SDKEnv.Pre 预发环境;<br>SDKEnv.Dev 测试环境 |

举个大栗子

Swift:

```swift
RokidMobileSDK.shared.env = .Release
```

Objc:

```objc
RokidMobileSDK.shared.env = SDKEnvRelease;
```

---

## 开启日志

举个大栗子

Swift:

```swift
// Log默认关闭
RokidMobileSDK.shared.openLog = true
```

```objc
RokidMobileSDK.shared.openLog = true;
```

---


