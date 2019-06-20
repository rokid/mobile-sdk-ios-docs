# Pod 引入方式（推荐）

** 1、引入 Mobile SDK **

```
pod 'RokidSDK', '~> 1.9.3'
```

** 2、引入头文件 **

```
#import <RokidSDK/RokidSDK-Swift.h>
```

** 3、增加依赖库 **

在 Podfile 中添加如下配置

```
source 'https://github.com/aliyun/aliyun-specs.git'

...

pod 'AliyunOSSiOS', '2.10.7'
```

### <font color=#ff0000>注意</font>

最新版 Xcode 10.2.1 可能会报 Swift 版本错误，需要按照如下来修改。

![如下图](media/alamofire-error.png)

解决方法是，在 Xcode 的 Pods 子工程中修改 Alamofire 的 **Swift Language Version** 为 **4.0**

![如图](media/swift-version-error.png)


