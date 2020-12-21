# Gözlem (Plan Şablonu)

Gözlem modu, poligonal bir alan üzerinde bir ızgara uçuş modeli oluşturmanıza olanak sağlar. İstediğiniz şekli, ızgaranın açısını ve diğer özelliklerini ve coğrafi etiketli görüntüler oluşturmak için uygun kamera ayarlarını belirtebilirsiniz.

> **Important** Eğer gözlemlenecek alanda önemli yükseklik farkları varsa [Terrain Following](#terrain)'i devreye almayı gözönüne alın.
> 
> Kamera özelliklerini kullanan bir Gözlem planlanırken, gözlem alanınızın zeminin düz olduğu varsayılır - ör. kalkış/rv konumuyla aynı yükseklik. Eğer araştırma alanınızın zemin yüksekliği ev konumunuzdan daha yüksek veya daha alçaksa, görüntülerinizdeki etkili örtüşme hesaplanandan daha az veya daha fazla (sırasıyla) olacaktır. Araştırma alanınızın zemin yüksekliği ev konumunuzdan *önemli* ölçüde daha yüksekse, yanlışıla aracın zemin seviyesindeki engellere çarpmasına neden olacak bir görev planlayabilirsiniz.
> 
> Terrain Following'in kullanılması, araştırmanın arazi üzerinde istenen irtifaya daha yakın olmasını sağlar ve yer seviyesine çok yakın bir görev planlanması olasılığını azaltır.

![Survey](../../assets/plan/survey/survey.jpg)

## Gözlem Görevi Oluştuma

Bir gözlem görevi oluşturmak için:

1. [PlanView](../PlanView/PlanView.md)'den *Plan Tools*'u açın.
2. *Plan Tools* 'dan *Pattern Tool*'u seçin ve *Survey*'e tıklayın.
  
  ![Survey Menu](../../assets/plan/survey/survey_menu.jpg)
  
  Bu haritaya bir gözlem alanı ve görev listesine (sağda) bir *Survey* öğesi ekleyecektir.

3. Haritada köşeleri sürükleyerek çokgenin şeklini değiştirebilirsiniz.

4. Yeni bir köşe noktası oluşturmak için var olan köşelerin ortalarındaki `(+)` semboüne tıklayın. Yeni köşe, yeni pozisyonlara çekilebilir.

Gözlem modu ayarları bir sonraki bölümde ele alınmıştır.

## Ayarlar

Gözlem görevi, ilişkili görev öğesinde (*Plan View*'in sağ tarafındaki görev öğesi listesinde) daha da yapılandırılabilir.

### Kamera

Kamera başlatma davranışı, kamera/kamera ayarlarına bağlıdır. Var olan veya özel bir kamerayı seçebilir ya da ayarları manuel olarak girebilirsiniz. Mevcut kameraların listesi (QGC 3.4) aşağıda verilmiştir.

![Survey - Camera Select](../../assets/plan/survey/survey_camera_select.jpg)

#### Bilinen Kamera {#known_camera}

Seçenekler açılır listesinden bilinen bir kamerayı seçmek, kameranın özelliklerine göre bir ızgara deseni oluşturur.

![Survey - Camera Sony](../../assets/plan/survey/survey_camera_sony.jpg)

Varsayılan ayarlar, yapılandırma seçenekleri kullanılarak gözleminiz için ayarlanabilir:

- **Landscape/Portrait** - Aracın "normal" yönüne göre kamera yönü.
- **Overlap** - Yakalanan her görüntü arasında örtüşme. Bu, ızgara hatları boyunca uçarken veya bu hatların üzerinden geçerken olmak üzere ayrı ayrı yapılandırılabilir.
- Birini Seçin: 
  - **Altitude** - Tarama yüksekliği (bu yükseklik için zemin çözünürlüğü hesaplanacak/görüntülenecektir).
  - **Ground resolution** - Her görüntü için zemin çözünürlüğü (bu çözünürlüğü sağlamak için gerekli yükseklik hesaplanacak/görüntülenecektir).

#### Özel Kamera {#custom_camera}

Özel kamera seçeneğinin seçilmesi, yeni bir kamera için ayarları bilinen bir kameraya benzer şekilde belirlemenize olanak tanır.

![Survey - Custom Camera](../../assets/plan/survey/survey_camera_custom.jpg)

Özel kameraya özgü ayarlar şunlardır:

- **Sensor width/height** - Kameranın fotoğraf sensörünün boyutu.
- **Image width/height** - Kameranın çektiği görüntünün çözünürlüğü.
- **Focal Length** - Kamera lensinin odak uzaklığı.

Geri kalan ayarlar [bilinen kamera](#known_camera) ile aynıdır.

#### Manuel Kamera

Manuel kamera seçeneği, kameranız için istenen tarama yüksekliğini, deklanşör aralığını ve uygun ızgara aralığını belirlemenize olanak tanır.

![Survey - Manual Camera Settings](../../assets/plan/survey/survey_camera_manual.jpg)

Ayarlanabilir seçenekler şunlardır:

- **Altitude** - Tüm rotayı uçmak için gözlem irtifası.
- **Trigger Distance** - Her bir kamera çekimi arasındaki zemin üzerinde alınan mesafe.
- **Spacing** - Rota boyunca bitişik ızgara (uçuş yolu) çizgileri arasındaki mesafe.

### Kesitler

*Transects* sekmesi kameradan bağımsız olan ızgara ayarları için kullanılır.

![Survey - Transects](../../assets/plan/survey/survey_transects.jpg)

Ayarlanabilir seçenekler şunlardır:

- **Angle** - Kuzeye göre, ızgara çizgilerinin açısı. ![Survey - Angle](../../assets/plan/survey/survey_transects_angle.jpg)
- **Turnaround dist** - Aracın geri dönmesi için tarama alanının dışına eklenecek olan mesafe miktarı.
- **Rotate entry point** - Gözlem görevinin başlangıç ve bitiş noktasını birbirleriyle değiştirmek için butona basın.
- **Hover and capture image** - Görüntü yakalamak için havada durmak (sadece multikopterler).
- **Refly at 90 degree offset** - Tüm görevi% 90 farkla yeniden gözden geçirmek için işaretleyin. ![Survey - Fly Offset](../../assets/plan/survey/survey_transects_offset.jpg)
- **Images in turnarounds** - Dönüşlerde fotoğraf çekilmesi için işaretleyin
- **Relative altitude** - Check to ... TBD.

### Terrain

By default, a flying vehicle will follow the survey path at a fixed altitude. Enabling *Terrain Following* makes the vehicle maintain a constant height relative to ground.

![Survey - Terrain Following Settings](../../assets/plan/survey/survey_terrain.jpg)

> **Note** Terrain following uses terrain heights queried from *AirMap* servers.

The configurable options are:

- **Vehicle follows terrain** - Check to enable terrain following (and display the following options). 
  - **Tolerance** - The accepted deviation in altitude from the target altitude.
  - **Max Climb Rate** - Maximum climb rate when following terrain.
  - **Max Descent Rate** - Maximum descent rate when following terrain.

### Statistics

The *Statistics* section shows the calculated survey area, photo interval, photo spacing and planned photo count.

![Survey - Statistics](../../assets/plan/survey/survey_statistics.jpg)