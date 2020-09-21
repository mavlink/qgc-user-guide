# 下载和安装

以下部分内容可被用于在对应每个工作平台上，下载*QGroundControl*当前的[稳定版本](../releases/release_notes.md)。

> **小贴士** 如果您在安装完*QGroundControl*后运行时遇到了任何问题，可以查看 [QGC 安装/配置问题集](../Support/troubleshooting_qgc.md)

## 系统配置要求

QGC可以在任何当下流行的计算机或移动设备上正常运行。 性能表现将取决于系统环境、第三方应用程序和当前系统可使用的资源状况。 更牛的硬件配置将会提供一个更好的使用体验。 最低配置也至少要8Gb的内存，一个固态硬盘，Nvidia 或 AMD的显示卡和i5级别或更强的CPU，会让大多数应用程序执行起来爽到666

为了获得最好的体验和兼容性，我们推荐您使用最新版本的操作系统。

## Windows 系统 {#windows}

*QGroundControl* can be installed on 64 bit versions of Windows:

1. 下载[QGroundControl-installer.exe](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl-installer.exe)。
2. 双击可执行文件来启动安装程序。

> **注意** Windows 安装程序有三个快捷选项：**QGroundControl**, **GPU 兼容性模式**, **GPU 安全模式**。 除非您有遇到启动或图像渲染问题，一般情况下，使用第一个选项来安装， 想了解更多详情可以参考[QGC Install/Config Problem>Windows：UI Rendering/Video Driver Issues](../Support/troubleshooting_qgc.md#opengl_troubleshooting)。

<span></span>

> **Note** Prebuilt *QGroundControl* versions from 4.0 onwards are 64-bit only. It is possible to manually build 32 bit versions (this is not supported by the dev team).

## Mac OS X 系统 {#macOS}

*QGroundControl* can be installed on macOS 10.20 or later:

1. 下载[QGroundControl.dmg](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.dmg)。
2. 双击.dmg 文件以挂载它，然后将*QGroundControl*应用程序拖动到您的*应用程序*文件夹。
    
    > **注意** QGroundControlControl在Catalina系统上如果没有被签名认证，会有些问题发生。 当您首次打开 QGC 应用：
    > 
    > * 右键点击QGC 应用图标，从菜单中选择Open 您只有一个选项，就是Cancel 选择 Cancel。
    > * 再次右键点击QGC 应用图标，从菜单中选择Open。 这次您会发现有 Open的选项了。

## Ubuntu Linux 系统 {#ubuntu}

*QGroundControl* can be installed/run on Ubuntu LTS 18.04 (and later).

Ubuntu comes with a serial modem manager that interferes with any robotics related use of a serial port (or USB serial). Before installing *QGroundControl* you should remove the modem manager and grant yourself permissions to access the serial port. You also need to install *GStreamer* in order to support video streaming.

Before installing *QGroundControl* for the first time:

1. 在命令提示符下输入: 
        sh
        sudo usermod -a -G dialout $USER
        sudo apt-get remove modemmanager -y
        sudo apt install gstreamer1.0-plugins-bad gstreamer1.0-libav gstreamer1.0-gl -y

2. 注销并重新登录以启用对用户权限的更改。

&nbsp; To install *QGroundControl*:

1. 下载[QGroundControl.AppImage](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.AppImage)。
2. 使用终端命令安装(并运行)： 
        sh
        chmod +x ./QGroundControl.AppImage
        ./QGroundControl.AppImage  (or double click)

> **Note** There are known [video steaming issues](../Support/troubleshooting_qgc.md#dual_vga) on Ubuntu 18.04 systems with dual adaptors.

<span></span>

> **Note** Prebuilt *QGroundControl* versions from 4.0 cannot run on Ubuntu 16.04. To run these versions on Ubuntu 16.04 you can [build QGroundControl from source without video libraries](https://dev.qgroundcontrol.com/en/getting_started/).

## Android {#android}

*QGroundControl* is available from the Google Play Store.

You can also install manually:

* [Android 32 位 APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl32.apk)
* [Android 64 位 APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl64.apk)

## iOS 版 {#iOS}

*QGroundControl* is available from the App Store.

## 旧稳定版本

Old stable releases can be found on <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">GitHub</a>.

## 每日构建

Daily builds can be [downloaded from here](../releases/daily_builds.md).