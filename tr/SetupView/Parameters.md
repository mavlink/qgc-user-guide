# Parametreler

*Parametreler* ekranı, araçla ilişkili parametrelerden herhangi birini bulmanıza ve düzenlemenizi sağlar.

![Parameters Screen](../../assets/setup/parameters_px4.jpg)

> **Note** PX4 Pro ve ArduPilot farklı parametre setleri kullanır, ancak her ikisi de bu bölümde açıklandığı gibi yönetilir.

## Bir Parametreyi Bulma

Parametreler gruplar halinde düzenlenmiştir. Soldaki butonlara tıklayarak görüntülemek için bir parametre grubu seçin (yukarıdaki görüntüde * Pil Kalibrasyonu * grubu seçilir).

Ayrıca * Search* alanına bir terim girerek bir parametre için * arama * yapabilirsiniz. Bu size girilen alt diziyi içeren tüm parametre adlarının ve açıklamalarının bir listesini gösterecektir (aramayı sıfırlamak için ** Clear ** tuşuna basın).

![Parameters Search](../../assets/setup/parameters_search.jpg)

## Bir Parametreyi Değiştirme

Bir parametrenin değerini değiştirmek için bir grup ya da arama listesindeki parametre satırına tıklayın. Bu size değeri güncellemenizi sağlayacak bir yan diyalog açar (bu diyalog ayrıca parametre hakkında ek detaylı bilgilerde gösterir - değişikliğin etki etmesi için yeniden başlatmanın gerekip gerekmediği bilgisi de dahil).

![Changing a parameter value](../../assets/setup/parameters_changing.png)

> **Note** **Save** butonuna basıldığında, parametre sessizce ve otomatik olarak bağlı cihaza yüklenir. Parametreye bağlı olarak, değişikliğin etki etmesi için uçuş kontrolcüsünü yeniden başlatmanız gerekebilir.

## Araçlar

Ekranın sağ üstündeki **Tools** menüsünden ek seçenekler seçebilirsiniz.

![Tools menu](../../assets/setup/parameters_tools_menu.png)

**Refresh** <br /> Tüm parametreleri araçtan tekrar isteyerek yenileyin.

**Reset all to defaults** <br />Tüm parametleri varsayıla değerlerine sıfırlayın.

**Load from file / Save to file** <br />Parametreleri var olan bir dosyadan yükleyin veya mevcut parametre ayarlarınızı bir dosyaya kaydedin.

**Clear RC to Param** <br />Bu, RC verici kontrolleri ve parametreleri arasındaki tüm ilişkileri siler. For more information see: [Radio Setup > Param Tuning Channels](../SetupView/Radio.md#param-tuning-channels-px4).

**Reboot Vehicle** <br />Reboot the vehicle (required after changing some parameters).