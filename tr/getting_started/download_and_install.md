# İndirme ve Kurulum

The sections below can be used to download the [current stable release](../releases/release_notes.md) of *QGroundControl* for each platform.

> **Tip** *QGroundControl*'i indirdikten sonra çalıştırmakta bir problem yaşıyorsanız [QGC Install/Config Problems](../Support/troubleshooting_qgc.md)'e bir göz atın!

## Sistem Gereksinimleri

QGC tüm güncel bilgisayar ya da mobil cihazlarda iyi bir şekilde çalışacaktır. Performansı sistem ortamına, 3. taraf uygulamalara ve mevcut sistem kaynaklarına bağlıdır. Daha yüksek kapasiteli donanım daha iyi bir deneyim sunacaktır. En az 8 Gb Ram'e, SSD'ye, Nvidia ya da AMD ekran kartına ve i5 veya daha iyi bir işlemciye sahip bir bilgisayar çoğu uygulama için yeterince iyi olacaktır.

En iyi deneyim ve uyumluluk için size işletim sisteminizin en yeni sürümünü kullanmanızı öneriyoruz.

## Windows {#windows}

*QGroundControl* Windows'un 64 bit versiyonlarına kurulabilir:

1. Download [QGroundControl-installer.exe](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl-installer.exe).
2. Yükleyiciyi başlatmak için QGroundControl-installer. exe'ye çift tıklayın.

> **Note** Windows kurulum programı 3 kısayol oluşturur: **QGroundControl**, **GPU Compatibility Mode**, **GPU Safe Mode**. Eğer başlatma veya video işleme sorunları yaşamıyorsanız ilk kısayolu kullanın. Daha fazla bilgi için [QGC Install/Config Problems > Windows: UI Rendering/Video Driver Issues](../Support/troubleshooting_qgc.md#opengl_troubleshooting)'e göz atın.

<span></span>

> **Note** 4.0'dan itibaren önceki *QGroundControl* sürümleri sadece 64 bittir. Manuel olarak 32 bit sürümler oluşturmak mümkündür (bu, geliştirici ekip tarafından desteklenmez).

## Mac OS X {#macOS}

*QGroundControl* macOS 10.20 veya daha güncel sürümlere kurulabilir:

1. Download [QGroundControl.dmg](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl.dmg).
2. .dmg dosyasına çift tıklayın, ardından çıkan ekranda *QGroundControl*'ü *Application* dosyasına sürükleyin.
    
    > **Note** QGroundControl imzasız olduğu için Catalina'da problem olmaya devam etmektedir. QGC uygulamasını ilk defa açmak için:
    > 
    > * QGC uygulama ikonuna sağ tıklayın, menüden Aç'ı seçin. Karşınıza yalnızca İptal Et seçeneği çıkacaktır. İptal Et'i seçin.
    > * QGC uygulama ikonuna tekrar sağ tıklayın, menüden Aç'ı seçin. Bu sefer Aç seçeneği de size sunulacaktır.

## Ubuntu Linux {#ubuntu}

*QGroundControl* can be installed/run on Ubuntu LTS 20.04 (and later).

Ubuntu, bir seri bağlantı noktasının (veya USB serisinin) robotikle ilgili kullanımına müdahale eden bir seri modem yöneticisi ile birlikte gelir. * QGroundControl * 'ü kurmadan önce modem yöneticisini kaldırmalı ve seri bağlantı noktasına erişim için kendinize izin vermelisiniz. Ayrıca video akışını desteklemek için * GStreamer * 'ı da yüklemeniz gerekmektedir.

* QGroundControl * 'ı ilk kez kurmadan önce:

1. Terminalde şunu girin: 
        sh
        sudo usermod -a -G dialout $USER
        sudo apt-get remove modemmanager -y
        sudo apt install gstreamer1.0-plugins-bad gstreamer1.0-libav gstreamer1.0-gl -y

2. Kullanıcı izinlerinde değişikliği etkinleştirmek için oturumunuzu kapatın ve tekrar oturum açın.

&nbsp; * QGroundControl * yüklemek için:

1. Download [QGroundControl.AppImage](https://d176tv9ibo4jno.cloudfront.net/latest/QGroundControl.AppImage).
2. Aşağıdaki terminal komutlarını kullanarak kurun (ve çalıştırın): 
        sh
        chmod +x ./QGroundControl.AppImage
        ./QGroundControl.AppImage  (or double click)

> **Note** Çift adaptörlü Ubuntu 18.04 sistemlerinde bilinen [ video steaming issues ](../Support/troubleshooting_qgc.md#dual_vga) vardır.

<span></span>

> **Note** 4.0'dan itibaren önceki *QGroundControl* sürümleri Ubuntu 16.04'te çalıştırılamaz. Bu versiyonları Ubuntu 16.04'te çalıştırabilmek için [build QGroundControl from source without video libraries](https://dev.qgroundcontrol.com/en/getting_started/).

## Android {#android}

*QGroundControl* is temporily unavailable from the Google Play Store. You can install manually from here:

* [Android 32 bit APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl32.apk)
* [Android 64 bit APK](https://qgroundcontrol.s3-us-west-2.amazonaws.com/latest/QGroundControl64.apk)

## Old Stable Releases

Old stable releases can be found on <a href="https://github.com/mavlink/qgroundcontrol/releases/" target="_blank">GitHub</a>.

## Daily Builds

Daily builds can be [downloaded from here](../releases/daily_builds.md).