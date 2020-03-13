# 下载和安装

以下部分内容可被用于在对应每个工作平台上，下载*QGroundControl*当前的[稳定版本](../releases/release_notes.md)。

> **小贴士** 如果您在安装完*QGroundControl*后运行时遇到了任何问题，可以查看 [QGC 安装/配置问题集](../Support/troubleshooting_qgc.md)

## 系统配置要求

QGC可以在任何当下流行的计算机或移动设备上正常运行。 性能表现将取决于系统环境、第三方应用程序和当前系统可使用的资源状况。 更牛的硬件配置将会提供一个更好的使用体验。 最低配置也至少要8Gb的内存，一个固态硬盘，Nvidia 或 AMD的显示卡和i5级别或更强的CPU，会让大多数应用程序执行起来爽到666

为了获得最好的体验和兼容性，我们推荐您使用最新版本的操作系统。

## Windows 系统 {#windows}

为Windows Vista或更高版本安装*QGroundControl*：

1. 下载[QGroundControl-installer.exe](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl-installer.exe)。
2. 双击可执行文件来启动安装程序。

> **注意** Windows 安装程序有三个快捷选项：**QGroundControl**, **GPU 兼容性模式**, **GPU 安全模式**。 除非您有遇到启动或图像渲染问题，一般情况下，使用第一个选项来安装， 想了解更多详情可以参考[QGC Install/Config Problem>Windows：UI Rendering/Video Driver Issues](../Support/troubleshooting_qgc.md#opengl_troubleshooting)。

## Mac OS X 系统 {#macOS}

为 macOS 10.10或更高版本安装 *QGroundControl* ︰

1. 下载[QGroundControl.dmg](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.dmg)。
2. 双击.dmg 文件以挂载它，然后将*QGroundControl*应用程序拖动到您的*应用程序*文件夹。
    
    > **注意** QGroundControlControl在Catalina系统上如果没有被签名认证，会有些问题发生。 当您首次打开 QGC 应用：
    > 
    > * 右键点击QGC 应用图标，从菜单中选择Open 您只有一个选项，就是Cancel 选择 Cancel。
    > * 再次右键点击QGC 应用图标，从菜单中选择Open。 这次您会发现有 Open的选项了。

## Ubuntu Linux 系统 {#ubuntu}

Ubuntu 具有一个串行的调制解调的管理器，它会影响干扰任何与机器人相关的串行端口通讯 (或USB 串行)。 所以在安装 *QGroundControl* 之前，您得删除调制解调的管理器并赋予您自己访问串行端口的权限。 为了支持视频流功能，您还需要安装*GStreamer*。

在首次安装*QGroundControl*之前：

1. 在命令提示符下输入: 
        sh
        sudo usermod -a -G dialout $USER
        sudo apt-get remove modemmanager -y
        sudo apt install gstreamer1.0-plugins-bad gstreamer1.0-libav -y

2. 注销并重新登录以启用对用户权限的更改。

&nbsp; 为 Ubuntu Linux 16.04 LTS 安装*QGroundControl*

1. 下载[QGroundControl.AppImage](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.AppImage)。
2. 使用终端命令安装(并运行)： 
        sh
        chmod +x ./QGroundControl.AppImage
        ./QGroundControl.AppImage  (or double click)

## Android {#android}

*QGroundControl*可从Google Play商店获得。

您也可以手动安装：

* [Android 32 位 APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl32.apk)
* [Android 64 位 APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl64.apk)

## iOS 版 {#iOS}

*QGroundControl*可从 App Store 获得。

## 旧稳定版本

Old stable releases can be found on <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">GitHub</a>.

## Daily Builds

Daily builds can be [downloaded from here](../releases/daily_builds.md).