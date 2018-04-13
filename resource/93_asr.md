# Vui 反馈 模块
## 发送 ASR
发送 ASR，就是 发送一条 能让设备立即执行的一条指令。

**参数说明**

| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| asr | String | 是 | ASR 内容 |
| device | RKDevice | 是 | 需要发送的设备 |

**接口定义**

Swift:

```swift
RokidMobileSDK.vui.sendAsr(asr: String, to device: RKDevice)
```

Objc:

```objc
[RokidMobileSDK.vui  sendAsrWithAsr: @"XXX" to: self.device];
```

---

## 创建 ASR 纠错
纠正设备错误识别的 ASR 内容。

**参数说明**
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| originText | String | 是 | 原始的 ASR 内容  |
| targetText | String | 是 | 纠正后的 ASR 内容  |

**示例代码**：
 
```objective-c
    [RokidMobileSDK.vui asrCorrectCreateWithOriginText:originText targetText:targetText complete:^(RKError * error, RKTTExchangeRule * rule) {
        NSLog(@"%@",rule);
    }];
```
 
 **RKTTExchangeRule数据格式**：
   
 ```json
[
    {
        // ASR纠错ID
        "id": "xxx",   
        // 用户ID          
        "accountId": "xxx", 
        // 原始的ASR内容
        "originText": "xxx" ,
        // 纠正后的ASR内容
        "targetText": "xxx" ,
        // ASR纠错的创建时间
        "createTime": "xxx" ,
        // ASR纠错的更新时间
        "updateTime": "xxx" ,
    }
]
 ```
---
## 查询 ASR 纠错 
查询这条 ASR 是否被纠错过。

**参数说明**
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| originText | String | 是 | 原始的 ASR 内容  |

**示例代码**：
 
```objective-c
    [RokidMobileSDK.vui asrCorrectFindWithOriginText:originText complete:^(RKError * error, RKTTExchangeRule * rule) {
        NSLog(@"%@",rule);
    }];```
---
## 更新 ASR 纠错 
修改该条 ASR 的纠错内容。

**参数说明**
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| ruleId | Int | 是 | ASR纠错ID  |
| originText | String | 是 | 原始的 ASR 内容  |
| targetText | String | 是 | 纠正后的 ASR 内容  |

**示例代码**：
 
```objective-c
    [RokidMobileSDK.vui asrCorrectUpdateWithRuleId:ruleId originText:originText targetText:targetText complete:^(RKError * error, NSDictionary<NSString *,NSString *> * dic) {
         NSLog(@"%@",dic);
    }];
    ```
---
## 删除 ASR 纠错 
删除该条 ASR 的纠错内容。

**参数说明**
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| ruleId | Int | 是 | ASR纠错ID  |

**示例代码**：
 
```objective-c
 [RokidMobileSDK.vui asrCorrectDeleteWithRuleId:ruleId complete:^(RKError * error, NSDictionary* dic) {
        NSLog(@"%@", error);
    }];        
```
---
## 获取 ASR 纠错历史列表 
获取该用户全部的 ASR 纠错内容。

**参数说明**
 
| 字段    | 类型   | 必须？| 说明 |
| ------ | ----- | ----- | ----- |
| page | String | 是 | 页码  |
| size | String | 是 | 每页显示的数量, 推荐=@“25”  |

**示例代码**：
 
```objective-c
 [RokidMobileSDK.vui asrCorrectHistoryWithPage:page size:size complete:^(RKError * error, NSArray<RKTTExchangeRule *> * rules) {
        NSLog(@"%@", rules);
    }];        
```
---


