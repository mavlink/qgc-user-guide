# Uçuş Modları Kurulumu

* Uçuş Modları * bölümü, uçuş modlarını radyo kanal(lar)ına ve dolayısıyla radyo kontrol vericinizdeki anahtarlara eşlemenize olanak tanır. Hem uçuş modu kurulumu hem de mevcut uçuş modları PX4 ve ArduPilot'ta farklıdır (ve ArduCopter ile ArduPlane arasında bazı farklılıklar vardır).

Bu bölüme erişmek için, üstteki araç çubuğundan **dişli** simgesini (Vehicle Setup), daha sonra kenar çubuğundan **Flight Modes**'u seçin.

> **Note** Uçuş modlarını ayarlamak için önceden [ telsizinizi yapılandırmış ](../SetupView/Radio.md) olmanız gerekir.

<span></span>

> **Tip** Uçuş modları, farklı seviyelerde * otopilot destekli uçuşları * ve * tam otonom uçuşları *, görevler veya dışarıdan (API tabanlı) kontrol yoluyla sağlar. Farklı uçuş modları, yeni kullanıcıların, yalnızca temel RC kontrolünün sağladığından hataya daha toleranslı bir platformla uçmayı öğrenmelerine olanak tanır. Kalkış, iniş ve fırlatma konumuna geri dönme gibi yaygın görevlerin otomasyonunu da sağlarlar.

<div>
</div>

> Her platformdaki uçuş modları hakkında daha fazla bilgi için bakınız: * [PX4 Flight Modes](https://docs.px4.io/en/flight_modes/) * [ArduCopter Flight Modes](http://ardupilot.org/copter/docs/flight-modes.html) * [ArduPlane Flight Modes](http://ardupilot.org/plane/docs/flight-modes.html)

## ArduPilot Uçuş Modu Kurulumu

ArduPilot'ta vericinizin tek bir kanalına 6'ya kadar farklı uçuş modu atayabilirsiniz (kanal Plane'de seçilebilir, ancak Copter'de kanal 5'e sabitlenmiştir).

ArduCopter (yalnızca), 7-12. Kanallar için ek * Kanal Seçenekleri * belirlemenize de olanak tanır. Bunlar, bu anahtarlara işlevler atamanıza izin verir (örneğin, bir kamerayı açmak veya başlatmak için geri dönmek için). There is additional information about channel configuration in the ArduCopter docs: [Auxiliary Function Switches](https://ardupilot.org/copter/docs/channel-7-and-8-options.html#channel-7-and-8-options)

Uçuş modlarını ayarlamak için:

1. RC vericinizi açın.
2. Üstteki araç çubuğundan **dişli** simgesini (Vechicle Setup), daha sonra kenar çubuğundan **Flight Modes**'u seçin.
    
    ![Uçuş Modları Kurulumu - Arducopter](../../assets/setup/flight_modes_copter_ardupilot.jpg)
    
    > ** Note ** Yukarıdaki görüntü ArduCopter için uçuş modu kurulumunun bir ekran görüntüsüdür.

3. Açılır menülerden 6'ya kadar uçuş modu seçin.

4. ** Yalnızca ArduCopter: ** 7-12. kanallar için ek * Kanal Seçenekleri*ni seçin.
5. ** Yalnızca ArduPlane: ** Açılır menüden mod kanalını seçin.
    
    ![Uçuş Modları Kurulumu - Arduplane](../../assets/setup/flight_modes_plane_ardupilot.jpg)

6. Vericinizdeki her bir mod anahtarını sırayla seçerek modların doğru verici anahtarlarıyla eşleştirildiğini test edin ve istenen uçuş modunun etkinleştirilip etkinleştirilmediğini kontrol edin (etkin mod metni * QGroundControl * 'de sarıya döner).

Tüm değerler değiştirildikçe otomatik olarak kaydedilir.

> **Note** Yukarıdaki ArduCopter ekran görüntüsü, kanal 7 anahtarında ek bir RTL seçeneği bulunan üç konumlu uçuş modu anahtarı için tipik bir kurulumu göstermektedir. Ayrıca iki anahtar ve vericinizde miks kullanarak 6 uçuş modu kurabilirsiniz. Bunun nasıl yapılacağına ilişkin eğitimler için bu [ sayfanın ](http://ardupilot.org/copter/docs/common-rc-transmitter-flight-mode-configuration.html#common-rc-transmitter-flight-mode-configuration) orta bölümüne gidin.

## PX4 Autopilot Flight Mode Setup

*PX4* (*QGroundControl*) supports assigning up to 6 flight modes to switch positions encoded in a single channel.

### Tek Kanal Modu {#single_channel}

Tek kanallı seçim modu, bir "mod" kanalı belirlemenize ve kanalın PWM değerine bağlı olarak etkinleştirilecek en fazla 6 uçuş modu seçmenize olanak tanır. Ayrıca, kapatma anahtarı, kalkış moduna geri dönmek ve offboard modu için kanalları ayrı ayrı belirtebilirsiniz.

> **Note** In order to use approach you will first need to configure your *transmitter* to encode the physical positions of your mode switch(es) into a single channel. There is a video guide of how this is done for the popular *Taranis* transmitter [below](#taranis_setup) (check your documentation if you use a different transmitter).

Tek kanallı uçuş modu seçimini yapılandırmak için:

1. RC vericinizi açın.
2. Üstteki araç çubuğundan **dişli** simgesini (Vehicle Setup), daha sonra kenar çubuğundan **Flight Modes**'u seçin.
    
    ![Çok kanallı uçuş modları](../../assets/setup/flight_modes_single_channel_px4.jpg)

3. * Uçuş Modu Ayarlarını * özelleştirin:
    
    - ** Modu kanalını ** seçin (yukarıda Kanal 5 olarak gösterilirse de, verici yapılandırmanıza bağlı olacaktır). 
    - Altı adede kadar ** Uçuş Modu ** seçin.
4. *Anahtar Ayarları*'nı özelleştirin: 
    - Belirli eylemlerle eşlemek istediğiniz kanalları seçin - ör. * Dönüş * modu, * Öldürme anahtarı *, * Offboard* modu, vb. (vericinizde fazla anahtarlarınız ve kanallarınız varsa).
5. Modların doğru verici anahtarlarına eşlendiğini test edin: 
    - Her anahatarın istenen kanal için ayarlandığını doğrulamak için *Kanal Monitörü*'nü kontrol edin.
    - Vericinizdeki her bir mod anahtarını sırayla seçerek ve istenen uçuş modunun etkinleştirilip etkinleştirilmediğini kontrol edin (etkin mod metni * QGroundControl * 'de sarıya döner).

Tüm değerler değiştirildikçe otomatik olarak kaydedilir.

#### Video Örneği (Verici Kurulumu dahil)

Verici üzerindeki 2 ve 3'de konumlu bir anahtarın konumlarını 6 uçuş modunu temsil etmek için kullanmak ve her anahtar kombinasyonunu tek bir kanalda gönderilecek mod için belirli bir PWM değerinde kodlamak yaygındır.

Aşağıdaki video, bunun * FrSky Taranis * vericisi (çok popüler ve şiddetle tavsiye edilen bir RC vericisi) ile nasıl yapıldığını göstermektedir. İşlem, iki gerçek anahtarın her bir pozisyon kombinasyonuna bir "mantıksal anahtar" atamayı içerir. Her mantıksal anahtar daha sonra aynı kanal üzerinde farklı bir PWM değerine atanır.

<a id="taranis_setup"></a>
Ardından video, mod kanalını özelleştirmek ve 6 "slot" un her birine modları eşlemek için * QGroundControl * 'ın nasıl kullanılacağını gösterir. {% youtube %} http://www.youtube.com/watch?v=scqO7vbH2jo {% endyoutube %}