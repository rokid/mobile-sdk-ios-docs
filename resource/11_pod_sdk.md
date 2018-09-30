# Pod 引入方式

** 1、引入 Mobile SDK **

```
pod 'RokidSDK', '~> 1.3.0'
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

pod 'AliyunOSSiOS', '2.1.2'
```
** 4、手动导入其他依赖库 **

Mobile SDK 还需要导入其他依赖库，请下载后手动导入到工程里。

[下载依赖库](https://github.com/Rokid/RokidMobileSDKiOSDemo/tree/master/RokidSDK)


