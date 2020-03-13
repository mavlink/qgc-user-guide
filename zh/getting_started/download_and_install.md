# 下载和安装

以下部分内容可被用于在对应每个工作平台上，下载*QGroundControl*当前的[稳定版本](../releases/release_notes.md)。

> **小贴士** 如果您在安装完*QGroundControl*后运行时遇到了任何问题，可以查看 [QGC 安装/配置问题集](../Support/troubleshooting_qgc.md)

## 系统配置要求

QGC可以在任何当下流行的计算机或移动设备上正常运行。 Performance will depend on the system environment, 3rd party applications, and available system resources. More capable hardware will provide a better experience. A computer with at least 8Gb RAM, an SSD, Nvidia or AMD graphics and an i5 or better CPU will be suitable for most applications.

For the best experience and compatibility, we recommend you the newest version of your operating system.

## Windows {#windows}

Install *QGroundControl* for Windows Vista or later:

1. Download [QGroundControl-installer.exe](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl-installer.exe).
2. Double click the executable to launch the installer.

> **Note** The Windows installer creates 3 shortcuts: **QGroundControl**, **GPU Compatibility Mode**, **GPU Safe Mode**. Use the first shortcut unless you experience startup or video rendering issues. For more information see [QGC Install/Config Problems > Windows: UI Rendering/Video Driver Issues](../Support/troubleshooting_qgc.md#opengl_troubleshooting).

## Mac OS X {#macOS}

Install *QGroundControl* for macOS 10.10 or later:

1. Download [QGroundControl.dmg](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.dmg).
2. Double-click the .dmg file to mount it, then drag the *QGroundControl* application to your *Application* folder.
    
    > **Note** QGroundControl continues to not be signed which causes problem on Catalina. To open QGC app for the first time:
    > 
    > * Right-click the QGC app icon, select Open from the menu. You will only be presented with an option to Cancel. Select Cancel.
    > * Right-click the QGC app icon again, Open from the menu. This time you will be presented with the option to Open.

## Ubuntu Linux {#ubuntu}

Ubuntu comes with a serial modem manager that interferes with any robotics related use of a serial port (or USB serial). Before installing *QGroundControl* you should remove the modem manager and grant yourself permissions to access the serial port. You also need to install *GStreamer* in order to support video streaming.

Before installing *QGroundControl* for the first time:

1. On the command prompt enter: 
        sh
        sudo usermod -a -G dialout $USER
        sudo apt-get remove modemmanager -y
        sudo apt install gstreamer1.0-plugins-bad gstreamer1.0-libav -y

2. Logout and login again to enable the change to user permissions.

&nbsp; To install *QGroundControl* for Ubuntu Linux 16.04 LTS or later:

1. Download [QGroundControl.AppImage](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.AppImage).
2. Install (and run) using the terminal commands: 
        sh
        chmod +x ./QGroundControl.AppImage
        ./QGroundControl.AppImage  (or double click)

## Android {#android}

*QGroundControl* is available from the Google Play Store.

You can also install manually:

* [Android 32 bit APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl32.apk)
* [Android 64 bit APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl64.apk)

## iOS {#iOS}

*QGroundControl* is available from the App Store.

## Old Stable Releases

Old stable releases can be found on <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">GitHub</a>.

## Daily Builds

Daily builds can be [downloaded from here](../releases/daily_builds.md).