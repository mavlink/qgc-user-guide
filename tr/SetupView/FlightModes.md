# Uçuş Modları Kurulumu

* Uçuş Modları * bölümü, uçuş modlarını radyo kanal(lar)ına ve dolayısıyla radyo kontrol vericinizdeki anahtarlara eşlemenize olanak tanır. Hem uçuş modu kurulumu hem de mevcut uçuş modları PX4 ve ArduPilot'ta farklıdır (ve ArduCopter ile ArduPlane arasında bazı farklılıklar vardır).

Bu bölüme erişmek için, araç çubuğunun üstündeki **dişli** simgesini (Vechicle Setup), daha sonra kenar çubuğundan **Flight Modes**'u seçin.

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
2. Üstteki araç çubuğundan **dişli** simgesini (Vechicle Setup), daha sonra kenar çubuğundan **Flight Modes**'u seçin.
    
    ![Flight modes multi-channel](../../assets/setup/flight_modes_single_channel_px4.jpg)
    
    > **Tip** If the screen opens in *Multi Channel Mode* click the **Use Single Channel Mode Selection** button to change screen.

3. Specify *Flight Mode Settings*:
    
    - Select the **Mode channel** (above this shown as Channel 5, but this will depend on your transmitter configuration). 
    - Select up to six **Flight Modes**.
4. Specify *Switch Settings*: 
    - Select the channels that you want to map to specific actions - e.g. *Return* mode, *Kill switch*, *offboard* mode, etc. (if you have spare switches and channels on your transmitter).
5. Test that the modes are mapped to the right transmitter switches: 
    - Check the *Channel Monitor* to confirm that the expected channel is changed by each switch.
    - Select each mode switch on your transmitter in turn, and check that the desired flight mode is activated (the text turns yellow on *QGroundControl* for the active mode).

All values are automatically saved as they are changed.

#### Video Example (including Transmitter Setup)

It is common to use the positions of a 2- and a 3-position switch on the transmitter to represent the 6 flight modes, and encode each combination of switches as a particular PWM value for the mode that will be sent on a single channel.

The video below shows how this is done with the *FrSky Taranis* transmitter (a very popular and highly recommended RC transmitter). The process involves assigning a "logical switch" to each combination of positions of the two real switches. Each logical switch is then assigned to a different PWM value on the same channel.

<span id="taranis_setup"></span>
The video then shows how to use *QGroundControl* to specify the mode channel and map modes to each of the 6 "slots". {% youtube %} http://www.youtube.com/watch?v=scqO7vbH2jo {% endyoutube %}

### Multi-Channel Mode

> **Tip** We recommend you use [Single Channel Flight Mode](#single_channel) selection because the Multi Channel selection user interface can be confusing. If you do choose to use this method, then the best approach is to start assigning channels and take note of information displayed by *QGroundControl* following your selection.

The multi-channel selection UI allows you to map one or more modes to one or more channels. There are some modes (and hence switches) that must always be defined, and the channel to which they must be allocated.

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