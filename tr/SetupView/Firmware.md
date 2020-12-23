# Yazılımı Yükleme

* QGroundControl *'ün ** masaüstü ** sürümleri [ PX4 Pro ](http://px4.io/) veya [ ArduPilot ](http://ardupilot.com) yazılımını Pixhawk ailesinin uçuş kontrolörü kartlarına yükleyebilir. Varsayılan olarak QGC, seçili otopilotun mevcut kararlı sürümünü kuracaktır, ancak beta sürümleri, günlük sürümleri veya özel donanım yazılımı dosyalarını da kurmayı seçebilirsiniz.

* QGroundControl * ayrıca SiK Radyoları ve PX4 Flow cihazları için yazılımları da yükleyebilir.

> **Caution** Yazılım Yükleme özelliği şu anda * QGroundControl * tablet veya telefon sürümlerinde kullanılamamaktadır.

## Yazılım Güncellemesi için Cihazı Bağlayın

> **Caution** ** Aygıt Yazılımını yüklemeye başlamadan önce ** aracınıza olan tüm USB bağlantılarının * kesilmesi * (hem doğrudan hem de telemetri radyosu aracılığıyla) gerekir. Araca bir batarya ile * güç verilmemelidir *.

1. İlk olarak araç çubuğunun üstündeki **dişli** simgesini (*Vechicle Setup*), daha sonra kenar çubuğundan **Firmware**'i seçin.
    
    ![Firmware disconnected](../../assets/setup/firmware/firmware_disconnected.jpg)

2. Cihazınızı (Pixhawk, SiK Radio, PX4 Flow) USB aracılığıyla doğrudan bilgisayarınıza bağlayın.
    
    > **Note** Doğrudan makinenizdeki elektrik akışı olan bir USB bağlantı noktasına bağlayın (bir USB hub aracılığıyla bağlamayın).

## Yüklenecek Yazılımı Seçin

Once the device is connected you can choose which firmware to load (*QGroundControl* presents sensible options based on the connected hardware).

1. For a Pixhawk-compatible board choose either **PX4 Flight Stack vX.X.X Stable Release** or **ArduPilot Flight Stack** radio buttons to download the *current stable release*.
    
    ![Select PX4](../../assets/setup/firmware/firmware_select_default_px4.jpg)
    
    If you select *ArduPilot* you will also have to choose the specific firmware the type of vehicle (as shown below).
    
    ![Select ArduPilot](../../assets/setup/firmware/firmware_selection_ardupilot.jpg)

2. Check **Advanced settings** to select specific developer releases or install firmware from your local file system.
    
    ![ArduPilot - Advanced Settings](../../assets/setup/firmware/firmware_selection_advanced_settings.jpg)

## Update the firmware

1. Click the **OK** button to start the update.
    
    The firmware will then proceed through a number of upgrade steps (downloading new firmware, erasing old firmware etc.). Each step is printed to the screen and overall progress is displayed on a progress bar.
    
    ![Firmware Upgrade Complete](../../assets/setup/firmware/firmware_upgrade_complete.jpg)

Once the firmware has completed loading the device/vehicle will reboot and reconnect. Next you will need to configure the [airframe](../SetupView/Airframe.md) (and then sensors, radio, etc.)