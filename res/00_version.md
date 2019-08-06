#  版本更新详情

* v1.10.2

    [删除] `AliyunOSSiOS` 相关依赖

* v1.10.1

    [修改] OC 版本的 `Reachability` 和 Swift 版本的 `ReachabilitySwift` 冲突问题

* v1.10.0

    [新增] 注册流程相关接口：获取验证码，校验验证码，注册，修改密码，重置密码<br>
    [新增] 获取和更新用户信息接口<br>

* v1.9.3

    [优化] 优化日志输出，增强 SDK 稳定性<br>

* v1.9.1

    [新增] 配网时，设备蓝牙连上后，回调 设备信息，比如 sn
    
    [删除] 一些不必要的 log 输出


* v1.9.0

    [修改] 媒体模块 - `RokidMobileSDK.media.requestListIntent`接口增加`linkUrl`参数<br>
    [新增] 媒体模块 - 增加酷狗登录H5支持<br>


* v1.8.0

    [新增] 媒体模块 - 三方账号授权增加酷狗音乐登录支持<br>
    [新增] 账号模块 - 增加新的获取验证码接口以支持传入国际区号<br>

* v1.7.0

    [更新] 修复 一些 bug<br>
    [更新] 增强 SDK 稳定性<br>
    [修改] 删除一些 无效的文件<br>

* v1.6.6

    [修改] 获取云闹钟列表接口<br>

* v1.6.5

    [新增] 设备模块 - SDKDevice增加ssid（当前设备连接wifi）<br>
    [新增] 设备模块 - 增加获取YodaOS系统设备在线状态接口<br>

* v1.6.1

    [新增] Skill模块 - 云闹钟 列表获取、新增、删除、更新。<br>
    [新增] Skill模块 - 云提醒 列表获取、删除<br>

* v1.6.0

    [新增] 设备模块 - 设备音量设置、获取<br>
    [新增] 媒体模块 - 授权媒体 Skill 列表<br>
    [新增] 媒体模块 - 获取媒体 首页、列表、详情页信息<br>
    [新增] 媒体模块 - 媒体内容点播、暂停、继续播放、上一首、下一首<br>
    [新增] 媒体模块 - 三方账号授权API<br>
    [新增] 账号模块 - 新增重置密码接口。<br>
    [删除] 设备模块 - 删除设备基本信息(base_info) ，各个信息参数 都在 RKDevice 中 <br>
    [删除] ProtocolBuffers-Swift 依赖库<br>
    [删除] SQLite.swift 依赖库<br>
    [删除] AliyunLog 依赖库<br>
    [更新] AliyunOSSiOS 到 2.10.7<br>

* v1.3.0

    [新增] 蓝牙协议 2.0，配网过程中 设备状态的判断

* v1.2.1

    [新增] ChannelMessage 长连接全部消息 <br>

* v1.2.0

    [优化] 长连接稳定性

* v1.0.9

    [新增] Vui sendMessage接口

* v1.0.8

    [修改] Account token login

* v1.0.7 

    [新增] Web Bridge 接入说明

* v1.0.6

    [新增] 闹钟、提醒 skill 接口

* v1.0.5

    [修改] 增加asr纠错接口<br>
    [修改] pod中引入 'ReachabilitySwift'

* v1.0.4

    [修改] 统一 SDK 前缀。<br>
    [修改] home -> vui

* v1.0.3

    [新增] WebBridge 的 PhoneDelegate H5 touch 事件。

* v1.0.2

    [新增] WebBridge 接入说明

* v1.0.1

    [添加] Skill 闹钟、提醒

* v1.0.0 

    [新增] SDK 初完成版

