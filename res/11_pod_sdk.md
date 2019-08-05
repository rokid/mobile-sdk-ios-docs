# Pod 引入方式（推荐）

**1、引入 Mobile SDK**

```
pod 'RokidSDK', '~> 1.10.1'
```

**2、引入头文件**

```
#import <RokidSDK/RokidSDK-Swift.h>
```

**3、增加依赖库**

在 Podfile 中添加如下配置

```
source 'https://github.com/aliyun/aliyun-specs.git'

pod 'RokidSDK', '~> 1.10.1'
pod 'AliyunOSSiOS', '2.10.7'
```

### <font color=#ff0000>注意</font>

#### 1. swift 版本 错误

最新版 Xcode 10.2.1 可能会报 Swift 版本错误，需要按照如下来修改。

![如下图](media/alamofire-error.png)

解决方法是，在 Xcode 的 **Pods** 子工程中修改 **Alamofire** 的 **Swift Language Version** 为 **4.0**，如果有其他 swift 库，修改方式一样。

![如图](media/swift-version-error.png)

---

#### 2. Alamofire 运行时报错

建议使用 **pod 'Alamofire', '4.8.2'** 的版本，也是 **4.x** 最后的稳定版本。**5.x beta 版** 它是 **deployment target iOS 10.0**  以上（包括 10.0），而我们SDK是在 **deployment target iOS 8.0** 下开发的，**Alamofire** 最新新的版本用到的系统 **API** 在 iOS 8.0-iOS 9.0 上不可用，会造成运行时crash。**所以建议使用**pod 'Alamofire', '4.8.2'** 的版本。**

### **所以如果你要指定依赖的版本的话，建议使用较新的版本。**
