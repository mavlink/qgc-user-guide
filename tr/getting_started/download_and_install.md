# İndirme ve Kurulum

Aşağıdaki bölümler tüm platformlar için *QGroundControl*'ün [current stable release](../releases/release_notes.md)'lerini indirmek için kullanılabilir.

> **Tip** *QGroundControl*'i indirdikten sonra çalıştırmakta bir problem yaşıyorsanız [QGC Install/Config Problems](../Support/troubleshooting_qgc.md)'e bir göz atın!

## Sistem Gereksinimleri

QGC tüm güncel bilgisayar ya da mobil cihazlarda iyi bir şekilde çalışacaktır. Performansı sistem ortamına, 3. taraf uygulamalara ve mevcut sistem kaynaklarına bağlıdır. Daha yüksek kapasiteli donanım daha iyi bir deneyim sunacaktır. En az 8 Gb Ram'e, SSD'ye, Nvidia ya da AMD ekran kartına ve i5 veya daha iyi bir işlemciye sahip bir bilgisayar çoğu uygulama için yeterince iyi olacaktır.

En iyi deneyim ve uyumluluk için size işletim sisteminizin en yeni sürümünü kullanmanızı öneriyoruz.

## Windows {#windows}

*QGroundControl* Windows'un 64 bit versiyonlarına kurulabilir:

1. [QGroundControl-installer.exe](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl-installer.exe)'i indirin.
2. Yükleyiciyi başlatmak için QGroundControl-installer. exe'ye çift tıklayın.

> **Note** The Windows installer creates 3 shortcuts: **QGroundControl**, **GPU Compatibility Mode**, **GPU Safe Mode**. Use the first shortcut unless you experience startup or video rendering issues. For more information see [QGC Install/Config Problems > Windows: UI Rendering/Video Driver Issues](../Support/troubleshooting_qgc.md#opengl_troubleshooting).

<span></span>

> **Note** Prebuilt *QGroundControl* versions from 4.0 onwards are 64-bit only. It is possible to manually build 32 bit versions (this is not supported by the dev team).

## Mac OS X {#macOS}

*QGroundControl* can be installed on macOS 10.20 or later:

1. Download [QGroundControl.dmg](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.dmg).
2. Double-click the .dmg file to mount it, then drag the *QGroundControl* application to your *Application* folder.
    
    > **Note** QGroundControl continues to not be signed which causes problem on Catalina. To open QGC app for the first time:
    > 
    > * Right-click the QGC app icon, select Open from the menu. You will only be presented with an option to Cancel. Select Cancel.
    > * Right-click the QGC app icon again, Open from the menu. This time you will be presented with the option to Open.

## Ubuntu Linux {#ubuntu}

*QGroundControl* can be installed/run on Ubuntu LTS 18.04 (and later).

Ubuntu comes with a serial modem manager that interferes with any robotics related use of a serial port (or USB serial). Before installing *QGroundControl* you should remove the modem manager and grant yourself permissions to access the serial port. You also need to install *GStreamer* in order to support video streaming.

Before installing *QGroundControl* for the first time:

1. On the command prompt enter: 
        sh
        sudo usermod -a -G dialout $USER
        sudo apt-get remove modemmanager -y
        sudo apt install gstreamer1.0-plugins-bad gstreamer1.0-libav gstreamer1.0-gl -y

2. Logout and login again to enable the change to user permissions.

&nbsp; To install *QGroundControl*:

1. Download [QGroundControl.AppImage](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.AppImage).
2. Install (and run) using the terminal commands: 
        sh
        chmod +x ./QGroundControl.AppImage
        ./QGroundControl.AppImage  (or double click)

> **Note** There are known [video steaming issues](../Support/troubleshooting_qgc.md#dual_vga) on Ubuntu 18.04 systems with dual adaptors.

<span></span>

> **Note** Prebuilt *QGroundControl* versions from 4.0 cannot run on Ubuntu 16.04. To run these versions on Ubuntu 16.04 you can [build QGroundControl from source without video libraries](https://dev.qgroundcontrol.com/en/getting_started/).

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