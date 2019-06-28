# Pod 引入方式（推荐）

**1、引入 Mobile SDK**

```
pod 'RokidSDK', '~> 1.9.3'
```

**2、引入头文件**

```
#import <RokidSDK/RokidSDK-Swift.h>
```

**3、增加依赖库**

在 Podfile 中添加如下配置

```
source 'https://github.com/aliyun/aliyun-specs.git'

pod 'RokidSDK', '~> 1.9.3'
pod 'AliyunOSSiOS', '2.10.7'

```

### <font color=#ff0000>注意</font>

#### 1. swift 版本 错误

最新版 Xcode 10.2.1 可能会报 Swift 版本错误，需要按照如下来修改。

![如下图](media/alamofire-error.png)

解决方法是，在 Xcode 的 **Pods** 子工程中修改 **Alamofire** 的 **Swift Language Version** 为 **4.0**，如果有其他 swift 库，修改方式一样。

![如图](media/swift-version-error.png)

---

#### 2. Reachability.swift 运行时报错

原则上你只要在 Podfile 中配置如下两个依赖，执行 **pod install** 会自动安装 **RokidSDK** 的一些依赖，并且是最新的版本，比如 **ReachabilitySwift**，**Alamofire**，**MQTTClient** 等，当然你也可以指定版本，比如 **pod 'ReachabilitySwift', '4.3.1'**，这样 安装的就是指定版本的依赖。
```
pod 'RokidSDK', '~> 1.9.3'
pod 'AliyunOSSiOS', '2.10.7'

```

其中 **pod 'ReachabilitySwift', '4.1.0'** 这个版本编译没问题，但运行时会 crash，类型于找个 [#308 issues](https://github.com/ashleymills/Reachability.swift/issues/308)

![如图](media/reachability_run_error.png)

### **所以如果你要指定依赖的版本的话，建议使用较新的版本。**