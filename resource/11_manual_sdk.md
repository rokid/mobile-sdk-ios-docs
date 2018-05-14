# 手动 导入 SDK

1. 新建工程

2. 选择工程文件 -> 选择target -> General

3. 在 Embedded Binaries 中点击 +，选择 RokidSDK.framework，点击确定。

4. 使用第3部的方法将依赖的第三方库依次加入。
![](media/15263095346451.jpg)

5. 检查 setting 中的 framework search path 是否将添加的 framework 路径都包含了，缺少的加上。如果不确定，则在3、4步中添加framework时，选中 Copy item if needed，将 framework 添加到工程根目录下。
![](media/15263095507653.jpg)

6. 在 setting 中打开 swift 标准库（Always Embed Swift Standard Libraries）
![](media/15263095679483.jpg)


