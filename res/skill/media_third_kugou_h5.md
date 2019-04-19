## 酷狗音乐授权

### 概述

本文档适用于第三方厂商使用酷狗音乐技能。用户通过手机号和短信验证码登录获取token，RokidSDK对设备进行授权，授权成功的设备才可以使用酷狗音乐skill。

### 酷狗音乐授权流程

* 时序图


![酷狗音乐登录](![third_kugou](media/third_kugou_h5.png))



### 第三方厂商接入步骤

* 集成RokidSDK

  集成文档：[https://rokid.github.io/mobile-sdk-ios-docs/res/11_pod_sdk.html]

* 集成酷狗音乐SDK

  酷狗SDK framework和文档地址：[<https://github.com/Rokid/RokidMobileSDKiOSDemo/tree/master/Third/KuGou>]

* 酷狗音乐授权H5页面接入

  1）h5页面 url地址：<https://s.rokidcdn.com/mobile-app/h5/media/index.html#/kugou/userInfo>

  2）对应业务的webviewController

  ​	a. 导入RokidSDK

  ~~~objective-c
  #import <RokidSDK/RokidSDK.h>
  ~~~

  ​	b. 注入Bridge,设置delegate

  ​	OC demo：

  ~~~objective-c
  @interface WebviewViewController () <RKBridgeModuleViewDelegate>
  
  @property (strong, nonatomic) WKWebView *webView;
  @property (weak, nonatomic) RKWebBridge *webbridge;
  
  @end
  
  @implementation WebviewViewController
  
  - (void)viewDidLoad {
      [super viewDidLoad];
      // Do any additional setup after loading the view.
      
      self.webView = [[WKWebView alloc] init];
      
      // 注入RKWebBridge
      self.webbridge = [RKWebBridge injectWebBridgeTo:self.webView];
      
      // 设置 RKBridgeModuleViewDelegate，用于实现 Native UI 的功能
      [self.webbridge setViewDelegateWithDelegate: self];
      
      [self.view addSubview:self.webView];
      self.webView.frame = CGRectMake(0, 0, self.view.frame.size.width, self.view.frame.size.height);
      
      NSURL *url = [NSURL URLWithString: self.urlStr];
      //NSURL *url =[NSBundle.mainBundle URLForResource:@"test" withExtension:@"html"];
      
      NSURLRequest* request = [NSURLRequest requestWithURL:url];
      [self.webView loadRequest:request];
  }
  
  
  ~~~

  ​	c. delegate回调，UI层，如需要就去实现delegate

  ~~~objective-c
  //WebViewUIDelegate UI层的回调
  - (void)showBridgeLoading {
      NSLog(@"start showLoading");
  }
  
  - (void)hideBridgeLoading {
      NSLog(@"start hideLoading");
  }
  /// 展示toast信息
  - (void)showToastWithMessage:(NSString * _Nonnull)message {
      NSLog(@"%@", message);
  }
  
  
  ~~~




