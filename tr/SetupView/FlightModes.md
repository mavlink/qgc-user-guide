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
    
    ![Uçuş Modları Kurulumu - Arducopter](../../assets/setup/flight_modes_copter_ardupilot.jpg)
    
    > ** Note ** Yukarıdaki görüntü ArduCopter için uçuş modu kurulumunun bir ekran görüntüsüdür.

3. Açılır menülerden 6'ya kadar uçuş modu seçin.

4. ** Yalnızca ArduCopter: ** 7-12. kanallar için ek * Kanal Seçenekleri*ni seçin.
5. ** Yalnızca ArduPlane: ** Açılır menüden mod kanalını seçin.
    
    ![Uçuş Modları Kurulumu - Arduplane](../../assets/setup/flight_modes_plane_ardupilot.jpg)

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
    
    ![Çok kanallı uçuş modları](../../assets/setup/flight_modes_single_channel_px4.jpg)
    
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

> **Tip** Çok Kanallı mod seçim kullanıcı arayüzü kafa karıştırıcı olabileceğinden [ Tek Kanallı Uçuş Modu ](#single_channel) seçimini kullanmanızı öneririz. Bu yöntemi kullanmayı seçerseniz, en iyi yaklaşım kanalları atamaya başlamak ve seçiminizi takiben * QGroundControl * tarafından görüntülenen bilgileri not almaktır.

Çok kanallı mod seçimi kullanıcı arayüzü, bir veya daha fazla modu bir veya daha fazla kanalla eşlemenize olanak tanır. Her zaman tanımlanması gereken bazı modlar (ve dolayısıyla anahtarlar) ve bunların tahsis edilmesi gereken kanal vardır.

Çok kanallı mod kullanıcı arayüzünü kullanarak uçuş modlarını yapılandırmak için:

1. RC vericinizi açın.
2. Üstteki araç çubuğundan **dişli** simgesini (Vehicle Setup), daha sonra kenar çubuğundan **Flight Modes**'u seçin.
    
    ![Çok kanallı uçuş modları](../../assets/setup/flight_modes_multi_channel_px4.jpg)
    
    > **Tip** Ekran * Tek Kanal Modu * 'nda açılırsa, ekranı değiştirmek için ** Çok Kanallı Mod Seçimini Kullan ** düğmesine tıklayın.

3. Anahtarlarınıza atamak istediğiniz modları ve ilgili kanalı seçin (seçilen modlar, kanala göre gruplanacak kullanıcı arayüzüne * taşınır*). Modu kanala atamada bir takım karmaşıklıklar vardır:
    
    - Bazı modlarda devre dışı bırakılamayacakları ve değerleri doğrudan ayarlayanayacakları için gri bir kanal seçicisi olacaktır. Örneğin: 
        - *Mission* Modu - * Hold * (tanımlanmışsa) ile aynı kanal numarasına veya * Stabilized/Main* moduyla aynı kanala sahiptir.
        - *Altitude* modu: * Position Control * (tanımlanmışsa) ile aynı kanal numarasına veya * Stabilized/Main * moduyla aynı kanala sahiptir.
    - *Assist* modu - Bu mod, ancak (ve ancak) * Position Control * *Stabilized/Main*'den farklı bir kanalda etkinleştirilir ve tanımlanırsa,* Stabilized/Main * modu ile aynı kanala eklenir.
4. ** Generate Thresholds**'a tıklayın. 
    - Bu, tüm modlar için otomatik olarak eşik değerleri oluşturacak ve atanmış modlar için her kanala eşit olarak yayacaktır. Örneğin, yukarıda gösterilen mod atamasında, çoğu mod mod 5'e atanır ve her mod için kanal eşiklerinin kanal boyunca eşit olarak dağıldığını görebilirsiniz. 

Bu mod [ PX4 kurulum videosunda @ 6m53s ](https://youtu.be/91VGmdSlbo4?t=6m53s) (youtube) içinde gösterilir.

> ** Note ** Bu uçuş modu seçim mekanizması, PX4'ün hangi modun seçilmesi gerektiğini belirleme yöntemi nedeniyle nispeten karmaşıktır. Bu [ akış şemasından ](https://dev.px4.io/en/concept/flight_modes.html#flight-mode-evaluation-diagram) (PX4 Geliştirici Kılavuzu) biraz fikir edinebilirsiniz.