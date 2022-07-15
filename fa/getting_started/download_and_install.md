# دانلود و نصب

The sections below can be used to download the [current stable release](../releases/release_notes.md) of *QGroundControl* for each platform.

> **Tip** See [Troubleshooting QGC Setup](../troubleshooting/qgc_setup.md) if *QGroundControl* doesn't start and run properly after installation!

## سیستم مورد نیاز

کیوگراند باید روی هر کامپیوتر و گوشی هوشمند امروزی به خوبی کار کند. اما عملکرد برنامه به منابع آزاد سیستم بستگی دارد تجربه نشان داده که سیستم هایی با سخت افزار قوی تر بهتر نرم افزار رو اجرا میکنند بنظر ما یک کامپیوتر با ۸ گیگ رم ، گرافیک Nvidia یا AMD ، هارد SSD و پردازنده i5 برای اجرای کیوگراند مناسب است

برای کار کردن در بهترین حالت ما سیستم عامل اخرین نسخه را پیشنهاد میکنیم

## ویندوز {#windows}

*کیوگراند* را میتوان در نسخه های ۶۴ بیتی ویندوز نصب کرد

1. دانلود [QGroundControl-installer.exe](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl-installer.exe).
2. بعد از دانلود روی فایل اجرایی دوبار کلیک کنید

> **Note** The Windows installer creates 3 shortcuts: **QGroundControl**, **GPU Compatibility Mode**, **GPU Safe Mode**. Use the first shortcut unless you experience startup or video rendering issues. For more information see [Troubleshooting QGC Setup > Windows: UI Rendering/Video Driver Issues](../troubleshooting/qgc_setup.md#opengl_troubleshooting).

<span></span>

> **Note** Prebuilt *QGroundControl* versions from 4.0 onwards are 64-bit only. It is possible to manually build 32 bit versions (this is not supported by the dev team).

## مک او اس ایکس {#macOS}

*کیوگراند*را میتوان برای مک او اس نسخه 10.20 یا جدیدترنصب کرد

1. دانلود [QGroundControl.dmg](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl.dmg).
2. روی فایل .dmg دوبارکلیک کنید تا فرایند نصب شروع بشه و ایکون کیوگراند رو درگ کنید روی پوشه *Application*
    
    > **یادداشت** ممکن است کیوگراند در نسخه Catalina دچار مشکل شود برای بازکردن کیوگراند برای اولین بار:
    > 
    > * روی ایکون QGC راست کلیک کنید و روی Open را انتخاب کنید. You will only be presented with an option to Cancel. Select Cancel.
    > * Right-click the QGC app icon again, Open from the menu. This time you will be presented with the option to Open.

## لینوکس (ابونتو) {#ubuntu}

*کیوگراند*را میتوان برای Ubuntu LTS 20.04 یا جدیدتر نصب کرد.

Ubuntu comes with a serial modem manager that interferes with any robotics related use of a serial port (or USB serial). Before installing *QGroundControl* you should remove the modem manager and grant yourself permissions to access the serial port. You also need to install *GStreamer* in order to support video streaming.

ثبت از نصب *کیوگراند برای اولین بار* این مراحل را انجام دهید

1. On the command prompt enter:
    
    ```sh
    sudo usermod -a -G dialout $USER
    sudo apt-get remove modemmanager -y
    sudo apt install gstreamer1.0-plugins-bad gstreamer1.0-libav gstreamer1.0-gl -y
    sudo apt install libqt5gui5 -y
    ```
    
    <!-- Note, remove install of libqt5gui5 https://github.com/mavlink/qgroundcontrol/issues/10176 fixed -->

2. Logout and login again to enable the change to user permissions.

&nbsp; برای نصب *کیوگراند*:

1. دانلود [QGroundControl.AppImage](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl.AppImage).
2. برای نصب و اجرا دستور زیر دا در ترمینال وارد کنید 
        sh
        chmod +x ./QGroundControl.AppImage
        ./QGroundControl.AppImage  (or double click)

> **Note** There are known [video steaming issues](../troubleshooting/qgc_setup.md#dual_vga) on Ubuntu 18.04 systems with dual adaptors.

<span></span>

> **Note** Prebuilt *QGroundControl* versions from 4.0 cannot run on Ubuntu 16.04. To run these versions on Ubuntu 16.04 you can [build QGroundControl from source without video libraries](https://dev.qgroundcontrol.com/en/getting_started/).

## اندروید {#android}

*کیوگراند* به طور موقت از فوشگاه پلی قابل دانلور نیست و باید از قسمت پایین به صورت دستی دانلود کنید

* [Android 32 bit APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl32.apk)
* [Android 64 bit APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl64.apk)

## نسخه های پایدار قدیمی

میتوانید نسخه های پایدار قدیمی را از <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">گیتهاب</a> دریافت کنید.

## نسخه روزانه

شما میتوانید این نسخه را [ از اینجا دریافت کنید](../releases/daily_builds.md).