# 媒体模块

## 获取Skill列表
 请求参数：
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| callback | Callback | 是 | 请求结果回调 |
示例：

swift

```swift
RokidMobileSDK.media?.requestSkillListIntent(completion: { (error, json) in
    // ...
})
```
SkillBean具体格式如下：

```json
{
    "skillId": "RC528E2DD8E745E195173D9F8BE48436",
    "skillName": "喜马拉雅"
}
```

