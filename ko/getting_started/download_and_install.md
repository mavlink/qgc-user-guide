# 다운로드 및 설치

아래 섹션에서 여러 플랫폼의 *QGroundControl* [최신 안정 배포판](../releases/release_notes.md)를 다운로드할 수 있습니다.

> **Tip** 설치 후 *QGroundControl*이 정상적으로 실행되지 않으면 [QGC 설정 문제 해결](../troubleshooting/qgc_setup.md)편을 참조하십시오!

## 시스템 요구 사항

QGC는 최신 컴퓨터나 모바일 장치에서 월활하게 실행됩니다. 성능은 시스템 환경과 사용 가능한 시스템 리소스 상태에 따라 차이가 납니다. 하드웨어가 좋은 수록 더 좋은 성능을 발휘하는 것은 당연합니다. 최소 8Gb RAM, SSD, Nvidia 또는 AMD 그래픽 및 i5 이상의 CPU가 장착된 컴퓨터이면 충분합니다.

최상의 경험과 호환성을 위해 최신 버전의 운영 체제를 사용하는 것이 좋습니다.

## 윈도우 {#windows}

*QGroundControl*은 64비트 버전 윈도우 운영체제에 설치할 수 있습니다.

1. [QGroundControl-installer.exe](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl-installer.exe)를 다운로드합니다.
2. 실행 파일을 더블 클릭하여 설치 프로그램을 실행합니다.

> **Note** Windows 설치 프로그램은 **QGroundControl**, **GPU 호환 모드**, **GPU 안전 모드**의 3가지 바로 가기를 생성합니다. 시작 문제나 비디오 렌더링 문제가 발생하지 않는 한 첫 번째 바로 가기를 사용하십시오. 자세한 내용은 [QGC 설정 문제 해결 > Windows: UI 렌더링/비디오 드라이버 문제](../troubleshooting/qgc_setup.md#opengl_troubleshooting)를 참고하십시오.

<span></span>

> **Note** 4.0 버전 이상의 사전 빌드 *QGroundControl* 버전은 64비트 전용입니다. 32비트 버전은 수동으로 빌드할 수 있습니다(개발팀에서 지원하지 않음).

## 맥 OS X {#macOS}

*QGroundControl*은 macOS 10.20 이상에 설치할 수 있습니다.

1. [QGroundControl.dmg](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl.dmg)를 다운로드합니다.
2. dmg 파일을 더블 클릭하여 마운트한 다음 *QGroundControl* 애플리케이션을 *Application* 폴더로 드래그합니다.
    
    > **Note** QGroundControl 미서명 문제로 인하여 Catalina에서 문제가 발생합니다. 처음으로 QGC 앱을 열려면:
    > 
    > * QGC 앱 아이콘을 마우스 오른쪽 버튼으로 클릭하고 메뉴에서 열기를 선택합니다. 취소 옵션만 제공됩니다. 취소를 선택합니다.
    > * QGC 앱 아이콘을 마우스 오른쪽 버튼으로 클릭하고, 메뉴에서 열기를 선택합니다. 이번에는 열기 옵션이 표시됩니다.

## 우분투 리눅스 {#ubuntu}

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