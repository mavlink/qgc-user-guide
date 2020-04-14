# Скачать и установить

The sections below can be used download the [current stable release](../releases/release_notes.md) of *QGroundControl* for each platform.

> **Совет** Смотрите раздел [QGC Установка/Проблеммы при конфигурировании](../Support/troubleshooting_qgc.md), если у вас возникли какие-либо проблемы с запуском *QGroundControl* после установки!

## Системные требования

QGC должен хорошо работать на любом современном компьютере или мобильном устройстве. Однако производительность будет зависеть от системной среды, сторонних приложений и доступных системных ресурсов. Более мощное и современное оборудование обеспечит лучшую производительность. Рекомендуемые системные требования: процессор - Intel i5 (или старше), 8Gb RAM, SSD, видеокарта: Nvidia или AMD (не имеет принципиального значения).

Для большего комфорта и наилучшей совместимости, мы рекомендуем вам новейшую версию вашей операционной системы.

## Windows {#windows}

*QGroundControl* can be installed on 64 bit versions of Windows:

1. Скачайте [QGroundControl-installer.exe](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl-installer.exe).
2. Для запуска программы установки дважды кликните на исполняемый файл.

> **Примечание** Установщик создает 3 ярлыка: **QGroundControl**, **GPU Compatibility Mode**, **GPU Safe Mode**. Use the first shortcut unless you experience startup or video rendering issues. For more information see [QGC Install/Config Problems > Windows: UI Rendering/Video Driver Issues](../Support/troubleshooting_qgc.md#opengl_troubleshooting).

<span></span>

> **Note** Prebuilt *QGroundControl* versions from 4.0 onwards are 64-bit only. It is possible to manually build 32 bit versions (this is not supported by the dev team).

## Mac OS X {#macOS}

*QGroundControl* can be installed on macOS 10.10 or later:

1. Скачайте [QGroundControl.dmg](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.dmg).
2. Double-click the .dmg file to mount it, then drag the *QGroundControl* application to your *Application* folder.
    
    > **Note** QGroundControl continues to not be signed which causes problem on Catalina. To open QGC app for the first time:
    > 
    > * Right-click the QGC app icon, select Open from the menu. You will only be presented with an option to Cancel. Select Cancel.
    > * Right-click the QGC app icon again, Open from the menu. This time you will be presented with the option to Open.

## Ubuntu Linux {#ubuntu}

*QGroundControl* can be installed/run on Ubuntu LTS 18.04 (and later).

Ubuntu comes with a serial modem manager that interferes with any robotics related use of a serial port (or USB serial). Before installing *QGroundControl* you should remove the modem manager and grant yourself permissions to access the serial port. You also need to install *GStreamer* in order to support video streaming.

Before installing *QGroundControl* for the first time:

1. Выполните в командной строке (каждая строка отдельная команда): 
        sh
        sudo usermod -a -a -G dialout $USER
        sudo apt-get remove modemmanager -y
        sudo apt install gstreamer1.0-plugins-bad gstreamer1.0-libav -y

2. Завершите текущий сеанс и войдите снова, для применения изменений прав пользователя.

&nbsp; To install *QGroundControl*:

1. Скачайте [QGroundControl.AppImage](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.AppImage).
2. Выполните в терминале следующие команды: 
        sh
        chmod +x ./QGroundControl.AppImage
        ./QGroundControl.AppImage (или двойной клик)

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

## Прошлые Стабильные Релизы

Old stable releases can be found on <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">GitHub</a>.

## Ежедневные сборки

Daily builds can be [downloaded from here](../releases/daily_builds.md).