# Скачать и установить

The sections below can be used to download the [current stable release](../releases/release_notes.md) of *QGroundControl* for each platform.

> **Tip** See [Troubleshooting QGC Setup](../troubleshooting/qgc_setup.md) if *QGroundControl* doesn't start and run properly after installation!

## Системные требования

QGC должен хорошо работать на любом современном компьютере или мобильном устройстве. Однако производительность будет зависеть от системной среды, сторонних приложений и доступных системных ресурсов. Более мощное и современное оборудование обеспечит лучшую производительность. Рекомендуемые системные требования: процессор - Intel i5 (или старше), 8Gb RAM, SSD, видеокарта: Nvidia или AMD (не имеет принципиального значения).

Для большего комфорта и наилучшей совместимости, мы рекомендуем вам новейшую версию вашей операционной системы.

## Windows {#windows}

*QGroundControl* can be installed on 64 bit versions of Windows:

1. Download [QGroundControl-installer.exe](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl-installer.exe).
2. Для запуска программы установки дважды кликните на исполняемый файл.

> **Примечание** Установщик создает 3 ярлыка: **QGroundControl**, **GPU Compatibility Mode**, **GPU Safe Mode**. Use the first shortcut unless you experience startup or video rendering issues. For more information see [Troubleshooting QGC Setup > Windows: UI Rendering/Video Driver Issues](../troubleshooting/qgc_setup.md#opengl_troubleshooting).

<span></span>

> **Note** Prebuilt *QGroundControl* versions from 4.0 onwards are 64-bit only. It is possible to manually build 32 bit versions (this is not supported by the dev team).

## Mac OS X {#macOS}

*QGroundControl* can be installed on macOS 10.11 or later: <!-- match version using https://dev.qgroundcontrol.com/master/en/getting_started/#native-builds -->

<!-- usually based on Qt macOS dependency -->

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
2. Выполните в терминале следующие команды: 
        sh
        chmod +x ./QGroundControl.AppImage
        ./QGroundControl.AppImage (или двойной клик)

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