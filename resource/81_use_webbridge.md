# RKWebBridge
## 快速接入
SDK 提供了 快速接入方法 供开发者集成，请安装下面 Demo 代码使用即可，具体 Native UI View 组件可根据APP业务需求进行实现。

Swift:

```swift

class WebviewViewController: UIViewController {
    
    var webbridge: RKWebBridge?
    var webView: WKWebView?
    
    override func viewDidLoad() {
        super.viewDidLoad()
        
        self.webbridge = RKWebBridge.injectWebBridge(to: self.webView!)
        self.webbridge?.setPhoneDelegate(delegate: self)
        self.webbridge?.setAppDelegate(delegate: self)
        self.webbridge?.setViewDelegate(delegate: self)
    }
    
}

extension WebviewViewController: RKBridgeModulePhoneDelegate {
    // 用户手指按下
    func touchDown() {
    }
    
    // 用户手指移动
    func touchMove() {
    }
    
    // 用户手指抬起
    func touchUp() {
    }
}

extension WebviewViewController: RKBridgeModuleAppDelegate  {
    
    // 关闭当前页面
    func close() {
    }
    
    // 在当前的 webview ，打开Url
    func open(title: String, urlStr: String) {
    }
    
    // 在一个新的 ViewController 中打开Url
    func openNewWebView(title: String, urlStr: String) {
    }
    
    // 使用外部浏览器 打开Url
    func openExternal(urlStr: String) {
    }
    
    // 返回到指定module的page页面
    func goBack(module: String, page: String) {
    }
    
}

extension WebviewViewController: RKBridgeModuleViewDelegate  {
    
    // 显示 Toast
    func showToast(message: String) {
    }
    
    // 显示 加载中UI组件
    func showLoading(message: String) {
    }

    // 隐藏 加载中UI组件    
    func hideLoading() {
    }
    
    // 设置 标题栏标题
    func setNavigationBarTitle(title: String) {
    }
    
    // 设置 标题栏风格
    func setNavigationBarStyle(style: String) {
    }
    
    // 设置 标题栏 右侧按钮
    func setNavigationBarRight(button: [String : Any]) {
    }
    
    // 设置 标题栏 右侧按钮小红点状态
    func setNavigationBarRightDotState(state: Bool) {
    }
    
    // 显示 异常UI组件
    func errorView(state: Bool, retryUrl: String) {
    }
    
}

```

Objc:

```objc
@interface WebviewViewController () <RKBridgeModuleViewDelegate, RKBridgeModuleAppDelegate, RKBridgeModulePhoneDelegate>

@property(nonatomic, strong) RKWebBridge * rkWebBridge ;

- (void)viewDidLoad {
    self.rkWebBridge = [RKWebBridge injectWebBridgeTo:self.webView];

    [self.rkWebBridge setPhoneDelegateWithDelegate:self];
    [self.rkWebBridge setAppDelegateWithDelegate:self];
    [self.rkWebBridge setViewDelegateWithDelegate:self];
}

// 用户手指按下
- (void)touchDown {
}

// 用户手指移动
- (void)touchMove {
}

// 用户手指抬起
- (void)touchUp {
}
    
// 关闭当前页面
- (void)close {
}

// 在当前的 webview ，打开Url
- (void)openWithTitle:(NSString * _Nonnull)title urlStr:(NSString * _Nonnull)urlStr {
}

// 在一个新的 ViewController 中打开Url
- (void)openNewWebViewWithTitle:(NSString * _Nonnull)title urlStr:(NSString * _Nonnull)urlStr {
}

// 使用外部浏览器 打开Url
- (void)openExternalWithUrlStr:(NSString * _Nonnull)urlStr {
}

// 返回到指定module的page页面
- (void)goBackWithModule:(NSString * _Nonnull)module_ page:(NSString * _Nonnull)page;
    
// 显示 Toast
- (void)showToastWithMessage:(NSString * _Nonnull)message {
}

// 显示 加载中UI组件
- (void)showLoadingWithMessage:(NSString * _Nonnull)message {
}

// 隐藏 加载中UI组件 
- (void)hideLoading {
}

// 设置 标题栏标题
- (void)setNavigationBarTitleWithTitle:(NSString * _Nonnull)title {
}

// 设置 标题栏风格
- (void)setNavigationBarStyleWithStyle:(NSString * _Nonnull)style {
}

// 设置 标题栏 右侧按钮
- (void)setNavigationBarRightWithButton:(NSDictionary<NSString *, id> * _Nonnull)button {
}

// 设置 标题栏 右侧按钮小红点状态
- (void)setNavigationBarRightDotStateWithState:(BOOL)state {
}

// 显示 异常UI组件
- (void)errorViewWithState:(BOOL)state retryUrl:(NSString * _Nonnull)retryUrl {
}

```

（1）标题栏风格：
请标题栏风格 根据业务需求设置。

（2）标题栏 右侧 RightButton 参数解释：

| 名称 | 类型 | 必须? | 描述 |
| --- | --- | --- | --- |
| icon | String | 否 | 按钮图片 |
| text | String | 否 | 按钮标题 |
| loadSelf | Bool | 否 | `默认false`: 是否在当前页面打开 |
| targetUrl | String | 是 | `close`:  关闭当前页面</br> \<url>: 打开这个url |

---


