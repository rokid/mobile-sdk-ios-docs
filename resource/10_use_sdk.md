# Rokid Mobile SDK iOS版 使用方式
## SDK导入方式

**目前只支持手动添加,后续会添加CocoaPods**

* 暂时只支持 Debug 版本的 Framework 包
* 提供了测试工程，在 RokidSDKDemo 下，包括 Objc 和 swift(暂未实现) 两个版本

### 使用时的工程设置

* Podfile

```
Demo 工程中提供了 Podfile，里面已经写好了依赖的工程
```

* 工程设置

```
在工程的 Embed Library 中加上我们的 framework
在 Framework Search Path 中把 framework 所在路径设置好
```

* 注意目前只有 Debug 版本，且运行时注意是模拟器或真机环境 

