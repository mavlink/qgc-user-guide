# Скачать и установить

The sections below can be used download the [current stable release](../releases/release_notes.md) of *QGroundControl* for each platform.

> **Совет** Смотрите раздел [QGC Установка/Проблеммы при конфигурировании](../Support/troubleshooting_qgc.md), если у вас возникли какие-либо проблемы с запуском *QGroundControl* после установки!

## Системные требования

QGC должен хорошо работать на любом современном компьютере или мобильном устройстве. Однако производительность будет зависеть от системной среды, сторонних приложений и доступных системных ресурсов. Более мощное оборудование обеспечит лучшую производительность. A computer with at least 8Gb RAM, an SSD, Nvidia or AMD graphics and an i5 or better CPU will be suitable for most applications.

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

*QGroundControl* is temporarily unavailable from the Google Play Store. We are working on a fix for this, but it may take some time.

In the meantime you can [download and install the APK from here](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl.apk) (for Android 5.1 or later).

## iOS {#iOS}

> **Note** *QGroundControl* for iOS is in beta. It can only be installed as a [daily build](../releases/daily_builds.md).

Install *QGroundControl* for iOS 8.0 or later:

1. Follow the instructions for [Installing iOS Daily Beta](../releases/daily_builds.md).

## Old Stable Releases

Old stable releases can be found on <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">GitHub</a>.

## Daily Builds

Daily builds can be [downloaded from here](../releases/daily_builds.md).