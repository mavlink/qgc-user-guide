# 다운로드 및 설치

아래 섹션에서 여러 플랫폼의 *QGroundControl* [최신 안정 배포판](../releases/release_notes.md)를 다운로드할 수 있습니다.

> **Tip** 설치 후 *QGroundControl*이 정상적으로 실행되지 않으면 [QGC 설정 문제 해결](../troubleshooting/qgc_setup.md)편을 참조하십시오!

## 시스템 요구 사항

QGC는 최신 컴퓨터나 모바일 장치에서 월활하게 실행됩니다. 성능은 시스템 환경과 사용 가능한 시스템 리소스 상태에 따라 차이가 납니다. 하드웨어가 좋은 수록 더 좋은 성능을 발휘하는 것은 당연합니다. 최소 8Gb RAM, SSD, Nvidia 또는 AMD 그래픽 및 i5 이상의 CPU가 장착된 컴퓨터이면 충분합니다.

최상의 경험과 호환성을 위해 최신 버전의 운영 체제를 사용하는 것이 좋습니다.

## Windows {#windows}

*QGroundControl* can be installed on 64 bit versions of Windows:

1. Download [QGroundControl-installer.exe](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl-installer.exe).
2. Double click the executable to launch the installer.

> **Note** The Windows installer creates 3 shortcuts: **QGroundControl**, **GPU Compatibility Mode**, **GPU Safe Mode**. Use the first shortcut unless you experience startup or video rendering issues. For more information see [Troubleshooting QGC Setup > Windows: UI Rendering/Video Driver Issues](../troubleshooting/qgc_setup.md#opengl_troubleshooting).

<span></span>

> **Note** Prebuilt *QGroundControl* versions from 4.0 onwards are 64-bit only. It is possible to manually build 32 bit versions (this is not supported by the dev team).

## Mac OS X {#macOS}

*QGroundControl* can be installed on macOS 10.20 or later:

1. Download [QGroundControl.dmg](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl.dmg).
2. Double-click the .dmg file to mount it, then drag the *QGroundControl* application to your *Application* folder.
    
    > **Note** QGroundControl continues to not be signed which causes problem on Catalina. To open QGC app for the first time:
    > 
    > * Right-click the QGC app icon, select Open from the menu. You will only be presented with an option to Cancel. Select Cancel.
    > * Right-click the QGC app icon again, Open from the menu. This time you will be presented with the option to Open.

## Ubuntu Linux {#ubuntu}

*QGroundControl* can be installed/run on Ubuntu LTS 20.04 (and later).

Ubuntu comes with a serial modem manager that interferes with any robotics related use of a serial port (or USB serial). Before installing *QGroundControl* you should remove the modem manager and grant yourself permissions to access the serial port. You also need to install *GStreamer* in order to support video streaming.

Before installing *QGroundControl* for the first time:

1. On the command prompt enter:
    
    ```sh
    sudo usermod -a -G dialout $USER
    sudo apt-get remove modemmanager -y
    sudo apt install gstreamer1.0-plugins-bad gstreamer1.0-libav gstreamer1.0-gl -y
    sudo apt install libqt5gui5 -y
    ```
    
    <!-- Note, remove install of libqt5gui5 https://github.com/mavlink/qgroundcontrol/issues/10176 fixed -->

2. Logout and login again to enable the change to user permissions.

&nbsp; To install *QGroundControl*:

1. Download [QGroundControl.AppImage](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl.AppImage).
2. Install (and run) using the terminal commands: 
        sh
        chmod +x ./QGroundControl.AppImage
        ./QGroundControl.AppImage  (or double click)

> **Note** There are known [video steaming issues](../troubleshooting/qgc_setup.md#dual_vga) on Ubuntu 18.04 systems with dual adaptors.

<span></span>

> **Note** Prebuilt *QGroundControl* versions from 4.0 cannot run on Ubuntu 16.04. To run these versions on Ubuntu 16.04 you can [build QGroundControl from source without video libraries](https://dev.qgroundcontrol.com/en/getting_started/).

## Android {#android}

*QGroundControl* is temporily unavailable from the Google Play Store. You can install manually from here:

* [Android 32 bit APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl32.apk)
* [Android 64 bit APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl64.apk)

## Old Stable Releases

Old stable releases can be found on <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">GitHub</a>.

## Daily Builds

Daily builds can be [downloaded from here](../releases/daily_builds.md).