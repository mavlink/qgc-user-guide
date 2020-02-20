# Скачать и установить

The sections below can be used download the [current stable release](../releases/release_notes.md) of *QGroundControl* for each platform.

> **Совет** Смотрите раздел [QGC Установка/Проблеммы при конфигурировании](../Support/troubleshooting_qgc.md), если у вас возникли какие-либо проблемы с запуском *QGroundControl* после установки!

## Системные требования

QGC должен хорошо работать на любом современном компьютере или мобильном устройстве. Однако производительность будет зависеть от системной среды, сторонних приложений и доступных системных ресурсов. Более мощное и современное оборудование обеспечит лучшую производительность. Рекомендуемые системные требования: процессор - Intel i5 (или старше), 8Gb RAM, SSD, видеокарта: Nvidia или AMD (не имеет принципиального значения).

Для большего комфорта и наилучшей совместимости, мы рекомендуем вам новейшую версию вашей операционной системы.

## Windows {#windows}

Для установки *QGroundControl* на ОС Windows Vista и выше:

1. Скачайте [QGroundControl-installer.exe](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl-installer.exe).
2. Для запуска программы установки дважды кликните на исполняемый файл.

> **Примечание** Установщик создает 3 ярлыка: **QGroundControl**, **GPU Compatibility Mode**, **GPU Safe Mode**. Use the first shortcut unless you experience startup or video rendering issues. For more information see [QGC Install/Config Problems > Windows: UI Rendering/Video Driver Issues](../Support/troubleshooting_qgc.md#opengl_troubleshooting).

## Mac OS X {#macOS}

Для установки *QGroundControl* на macOS 10.10 и выше:

1. Скачайте [QGroundControl.dmg](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.dmg).
2. Дважды кликните на .dmg файле, чтобы смонтировать его, затем перетащите *QGroundControl* в папку *Приложения*.

## Ubuntu Linux {#ubuntu}

Ubuntu comes with a serial modem manager that interferes with any robotics related use of a serial port (or USB serial). Before installing *QGroundControl* you should remove the modem manager and grant yourself permissions to access the serial port. You also need to install *GStreamer* in order to support video streaming.

При первой инсталяции *QGroundControl*:

1. Выполните в командной строке (каждая строка отдельная команда): 
        sh
        sudo usermod -a -a -G dialout $USER
        sudo apt-get remove modemmanager -y
        sudo apt install gstreamer1.0-plugins-bad gstreamer1.0-libav -y

2. Завершите текущий сеанс и войдите снова, для применения изменений прав пользователя.

&nbsp; Для установки *QGroundControl* на ОС Ubuntu Linux 16.04 LTS или выше:

1. Скачайте [QGroundControl.AppImage](https://s3-us-west-2.amazonaws.com/qgroundcontrol/latest/QGroundControl.AppImage).
2. Выполните в терминале следующие команды: 
        sh
        chmod +x ./QGroundControl.AppImage
        ./QGroundControl.AppImage (или двойной клик)

## Android {#android}

*QGroundControl* временно недоступен в Google Play. Мы работаем над этим, но это может занять некоторое время.

Между тем вы можете [скачать необходимые APK здесь](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl.apk) (для Android 5.1 и выше).

## iOS {#iOS}

> **Note** *QGroundControl* for iOS is in beta. It can only be installed as a [daily build](../releases/daily_builds.md).

Install *QGroundControl* for iOS 8.0 or later:

1. Follow the instructions for [Installing iOS Daily Beta](../releases/daily_builds.md).

## Прошлые Стабильные Релизы

Прошлые стабильные релизы можно найти на <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">GitHub</a>.

## Ежедневные сборки

Ежедневные сборки могут быть [загружены отсюда](../releases/daily_builds.md).