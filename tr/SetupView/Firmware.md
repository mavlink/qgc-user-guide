# Yazılımı Yükleme

* QGroundControl *'ün ** masaüstü ** sürümleri [ PX4 Pro ](http://px4.io/) veya [ ArduPilot ](http://ardupilot.com) yazılımını Pixhawk ailesinin uçuş kontrolörü kartlarına yükleyebilir. Varsayılan olarak QGC, seçili otopilotun mevcut kararlı sürümünü kuracaktır, ancak beta sürümleri, günlük sürümleri veya özel donanım yazılımı dosyalarını da kurmayı seçebilirsiniz.

* QGroundControl * ayrıca SiK Radyoları ve PX4 Flow cihazları için yazılımları da yükleyebilir.

> **Caution** Yazılım Yükleme özelliği şu anda * QGroundControl * tablet veya telefon sürümlerinde kullanılamamaktadır.

## Yazılım Güncellemesi için Cihazı Bağlayın

> **Caution** ** Aygıt Yazılımını yüklemeye başlamadan önce ** aracınıza olan tüm USB bağlantılarının * kesilmesi * (hem doğrudan hem de telemetri radyosu aracılığıyla) gerekir. Araca bir batarya ile * güç verilmemelidir *.

1. İlk olarak araç çubuğunun üstündeki **dişli** simgesini (*Vechicle Setup*), daha sonra kenar çubuğundan **Firmware**'i seçin.
    
    ![Yazılım bağlantısı kesildi](../../assets/setup/firmware/firmware_disconnected.jpg)

2. Cihazınızı (Pixhawk, SiK Radio, PX4 Flow) USB aracılığıyla doğrudan bilgisayarınıza bağlayın.
    
    > **Note** Doğrudan makinenizdeki elektrik akışı olan bir USB bağlantı noktasına bağlayın (bir USB hub aracılığıyla bağlamayın).

## Yüklenecek Yazılımı Seçin

Cihaz bağlandıktan sonra, hangi aygıt yazılımının yükleneceğini seçebilirsiniz (* QGroundControl *, bağlı donanıma göre mantıklı seçenekler sunar).

1. Pixhawk uyumlu bir anakart için * mevcut kararlı sürümü * indirmek için ** PX4 Flight Stack vX.X.X Stable Release ** veya ** ArduPilot Flight Stack ** seçeneklerinden birini seçin.
    
    ![PX4'ü seçin](../../assets/setup/firmware/firmware_select_default_px4.jpg)
    
    * ArduPilot * 'ı seçerseniz, aynı zamanda araç tipini belirleyen donanım yazılımını da seçmeniz gerekecektir (aşağıda gösterildiği gibi).
    
    ![ArduPilot'ı seçin](../../assets/setup/firmware/firmware_selection_ardupilot.jpg)

2. Belirli geliştirici sürümlerini seçmek veya yerel dosya sisteminizden ürün yazılımı yüklemek için ** Advanced settings **'i kontrol edin.
    
    ![ArduPilot - Advanced Settings](../../assets/setup/firmware/firmware_selection_advanced_settings.jpg)

## Yazılımı güncelleme

1. Güncellemeyi başlatmak için ** OK ** tuşuna tıklayın.
    
    Ardından, aygıt yazılımı bir dizi yükseltme adımından geçecektir (yeni aygıt yazılımının indirilmesi, eski aygıt yazılımının silinmesi vb.). Her adım ekrana yazdırılır ve genel ilerleme bir ilerleme çubuğunda görüntülenir.
    
    ![Yazılım güncellemesi tamamlandı](../../assets/setup/firmware/firmware_upgrade_complete.jpg)

Yazılım yüklemesi tamamlandığında, cihaz / araç yeniden başlatılacak ve yeniden bağlanacaktır. Daha sonra [ gövdeyi](../SetupView/Airframe.md) (ve sonra sensörler, radyo vb.) Yapılandırmanız gerekir