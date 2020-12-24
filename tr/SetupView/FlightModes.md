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

ArduCopter (yalnızca), 7-12. Kanallar için ek * Kanal Seçenekleri * belirlemenize de olanak tanır. Bunlar, bu anahtarlara işlevler atamanıza izin verir (örneğin, bir kamerayı açmak veya başlatmak için geri dönmek için). ArduCopter belgelerinde kanal yapılandırması hakkında ek bilgi bulunmaktadır: [Auxiliary Function Switches]

Uçuş modlarını ayarlamak için:

1. RC vericinizi açın.
2. Üstteki araç çubuğundan **dişli** simgesini (Vechicle Setup), daha sonra kenar çubuğundan **Flight Modes**'u seçin.
    
    ![Flight modes setup - ArduCopter](../../assets/setup/flight_modes_copter_ardupilot.jpg)
    
    > ** Note ** Yukarıdaki görüntü ArduCopter için uçuş modu kurulumunun bir ekran görüntüsüdür.

3. Açılır menülerden 6'ya kadar uçuş modu seçin.

4. ** Yalnızca ArduCopter: ** 7-12. kanallar için ek * Kanal Seçenekleri*ni seçin.
5. ** Yalnızca ArduPlane: ** Açılır menüden mod kanalını seçin.
    
    ![Flight modes setup - ArduPlane](../../assets/setup/flight_modes_plane_ardupilot.jpg)

6. Vericinizdeki her bir mod anahtarını sırayla seçerek modların doğru verici anahtarlarıyla eşleştirildiğini test edin ve istenen uçuş modunun etkinleştirilip etkinleştirilmediğini kontrol edin (etkin mod metni * QGroundControl * 'de sarıya döner).

Tüm değerler değiştirildikçe otomatik olarak kaydedilir.

> **Note** Yukarıdaki ArduCopter ekran görüntüsü, kanal 7 anahtarında ek bir RTL seçeneği bulunan üç konumlu uçuş modu anahtarı için tipik bir kurulumu göstermektedir. Ayrıca iki anahtar ve vericinizde miks kullanarak 6 uçuş modu kurabilirsiniz. Bunun nasıl yapılacağına ilişkin eğitimler için bu [ sayfanın ](http://ardupilot.org/copter/docs/common-rc-transmitter-flight-mode-configuration.html#common-rc-transmitter-flight-mode-configuration) orta bölümüne gidin.

## PX4 Pro Uçuş Modu Kurulumu

* PX4 * (* QGroundControl *) uçuş modlarını verici anahtarları/kadranlarıyla eşleştirmek için iki modu destekler:

- ** Tek Kanallı Mod Seçimi: ** Tek bir kanalda kodlanmış konumları değiştirmek için 6'ya kadar uçuş modu atayın. 
- ** Çok Kanallı Mod Seçimi: ** Bir veya daha fazla kanalda kodlanmış konumların değiştirilmesi için modlar atayın. Bazı modlar, kanalları paylaşmak için kodlanmıştır veya diğer mod seçimlerine göre otomatik olarak tanımlanır / ayarlanır (çok kanallı mod seçiminin davranışı bazen kafa karıştırıcı olabilir). 

> **Tip** Önerilen yaklaşım * Tek Kanallı Mod Seçimi * 'i kullanmaktır çünkü anlaşılması ve yapılandırılması kolaydır. ArduPilot tarafından kullanılan yaklaşıma benzer.

### Tek Kanal Modu {#single_channel}

Tek kanallı seçim modu, bir "mod" kanalı belirlemenize ve kanalın PWM değerine bağlı olarak etkinleştirilecek en fazla 6 uçuş modu seçmenize olanak tanır. Ayrıca, kapatma anahtarı, kalkış moduna geri dönmek ve offboard modu için kanalları ayrı ayrı belirtebilirsiniz.

> **Note** Yaklaşımı kullanmak için, önce * vericinizi*, mod anahtar(lar)ınızın fiziksel konumlarını tek bir kanala kodlayacak şekilde yapılandırmanız gerekir. [ aşağıda ](#taranis_setup) popüler * Taranis * vericisi için bunun nasıl yapıldığına dair bir video kılavuzuna erişebilirsiniz(farklı bir verici kullanıyorsanız belgelerinizi kontrol edin).

Tek kanallı uçuş modu seçimini yapılandırmak için:

1. RC vericinizi açın.
2. Üstteki araç çubuğundan **dişli** simgesini (Vehicle Setup), daha sonra kenar çubuğundan **Flight Modes**'u seçin.
    
    ![Flight modes multi-channel](../../assets/setup/flight_modes_single_channel_px4.jpg)
    
    > **Tip** Ekran * Çok Kanallı Mod * 'da açılırsa, ekranı değiştirmek için ** Tek Kanallı Mod Seçimini Kullan ** düğmesine tıklayın.

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

<span id="taranis_setup"></span>
Ardından video, mod kanalını özelleştirmek ve 6 "slot" un her birine modları eşlemek için * QGroundControl * 'ın nasıl kullanılacağını gösterir. {% youtube %} http://www.youtube.com/watch?v=scqO7vbH2jo {% endyoutube %}

### Çok Kanallı Mod

> **Tip** Çok Kanallı seçim kullanıcı arayüzü kafa karıştırıcı olabileceğinden [ Tek Kanallı Uçuş Modu ](#single_channel) seçimini kullanmanızı öneririz. Bu yöntemi kullanmayı seçerseniz, en iyi yaklaşım kanalları atamaya başlamak ve seçiminizi takiben * QGroundControl * tarafından görüntülenen bilgileri not almaktır.

Çok kanallı mod seçimi kullanıcı arayüzü, bir veya daha fazla modu bir veya daha fazla kanalla eşlemenize olanak tanır. Her zaman tanımlanması gereken bazı modlar (ve dolayısıyla anahtarlar) ve bunların tahsis edilmesi gereken kanal vardır.

To configure flight modes using the multi-channel UI:

1. Turn on your RC transmitter.
2. Select the **Gear** icon (Vehicle Setup) in the top toolbar and then **Flight Modes** in the sidebar.
    
    ![Flight modes multi-channel](../../assets/setup/flight_modes_multi_channel_px4.jpg)
    
    > **Tip** If the screen opens in *Single Channel Mode* click the **Use Multi Channel Mode Selection** button to change screen.

3. Select the modes you want to assign to your switches and select the associated channel (selected modes will *move* in the UI to be grouped by channel). There are a number of complications on the mode to channel assignments:
    
    - Some modes will have a grayed out channel selector because they cannot be disabled and you cannot directly set the value. For example: 
        - *Mission* mode - Has the same channel number as *Hold* (if it is defined), or otherwise the same channel as *Stabilized/Main* mode.
        - *Altitude* mode - Has the same channel number as *Position Control* (if it is defined), or otherwise the same channel as *Stabilized/Main* mode.
    - *Assist* mode - This mode is added to the same channel as *Stabilized/Main* mode if (and only if) *Position Control* is enabled and defined on a different channel than *Stabilized/Main*.
4. Click the **Generate Thresholds** button. 
    - This will automatically create threshold values for all modes, spread evenly across each channel for its assigned modes. For example, in the mode assignment shown above, most modes are assigned to mode 5, and you can see that the channel thresholds for each mode are spread evenly across the channel. 

This mode is demonstrated in the [PX4 setup video @6m53s](https://youtu.be/91VGmdSlbo4?t=6m53s) (youtube).

> **Note** This flight mode selection mechanism is relatively complicated due to the way that PX4 works out which mode should be selected. You may be able to gain some insight from this [flow chart](https://dev.px4.io/en/concept/flight_modes.html#flight-mode-evaluation-diagram) (PX4 Developer Guide).