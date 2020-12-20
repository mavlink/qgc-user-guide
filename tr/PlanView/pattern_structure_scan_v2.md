# Yapı Taraması (Plan Şablonu)

*Structure Scan*, çok köşeli (veya dairesel) zemin ayak izine sahip bir yapının *dikey yüzeyleri* üzerinde (ör. duvarlar) görüntüler yakalayabilmek için ızgara şeklinde bir uçuş şablonu oluşturmanıza olanak sağlar. Yapı Taraması genellikle görsel inceleme ya da yapıların 3 boyutlu modellemesi için kullanılır.

*Yapı Taramaları*, Plan ekranında **Pattern > Structure Scan** aracı kullanılarak bir görevin içine yerleştirilebilir.

> **Note** *Structure Scan*'ın yeni versiyonu, eski *Structure Scan* planlarını okuyamaz. Eskilerin tekar oluşturulmaları gerekir.

<span></span>

> **Warning** Bu özellik henüz ArduPilot yazılımı tarafından desteklenmemektedir. PX4'de desteklenir.

## Genel Bakış

Aşağıdaki resim, yapı taramasının bir ekran görüntüsünü göstermektedir. Yeşil çokgen, yapının zemin ayak izini işaretlemek için kullanılırken, etrafındaki beyaz çizgi aracın uçuş yolunu gösterir. Uçuş yolundaki yeşil numaralı daire, taramaya giriş/çıkış noktasıdır (taramanın başladığı yer).

![Structure Scan](../../assets/plan/structure_scan_v2/StructureScan.jpg)

Tarama, yapıyı eşit olarak katmanlara ayırır; araç, yapının çevresinde belirli bir irtifada ve yapıya * scan distance*'den uçar, ardından tüm yüzey taranana kadar işlemi her katmanda tekrarlar.

![Layer JPG](../../assets/plan/structure_scan_v2/layers.jpg)

Kullanıcılar, yapının altındaki engellerden kaçınmak için *scan bottom altitude* ve araç taramaya / taramaya giderken engellerden kaçınmak için *entrance/exit altitude* ayarlayabilir.

## Tarama Oluşturma

Tarama oluşturmak için:

1. **Plan View**'den **Pattern tool > Structure Scan**'ı seçin.
  
  ![Create Scan JPG](../../assets/plan/structure_scan_v2/create_scan.jpg)

2. Bu haritada basit kare bir yapı taraması oluşturacaktır.
  
  ![Initial Polygon](../../assets/plan/structure_scan_v2/initial_polygon_scan.jpg)
  
  Yeşil bölge, yapıyı kaplayacak şekilde düzenlenmelidir.
  
  - Haritadaki opak köşeleri yapının kenarlarına sürükleyin (yukarıda leylak rengi daire içine alınmış köşeler). 
  - Yapının kapladığı alan basit bir kareden fazlaysa, yeni bir köşe noktası oluşturmak için köşeler arasındaki yarı saydam dairelere tıklayabilirsiniz.

3. Ayrıca merkezdeki "daire"ye (kırmızı ile işaretlenmiş) tıklayarak ve açılır menüden *Circle* 'ı seçerek dairesel bir alana geçebilirsiniz.
  
  ![Circle Scan](../../assets/plan/structure_scan_v2/circle_scan.jpg).
  
  - Açılır menüden çokgen alana geri dönebilir ve taramanın yarıçapını ve/veya konumunu değiştirebilirsiniz.
  - Çemberin merkezini konumlandırmak için merkezdeki daireyi sürükleyin. 

4. Geri kalan düzenlemeler, ekranın sağındaki *Structure Scan* editörü kullanılarak halledilir. İlk olarak manuel tarama, belirli bir kamera kullanarak tarama veya özel bir kamera tanımı kullanarak tarama seçeneklerinden hangisini istediğinizi seçin.
  
  > **Note** Modlar arasındaki temel fark, önceden tanımlanmış kameraların etkili bir katman yüksekliğini ve deklanşör mesafesini doğru bir şekilde hesaplamak için zaten ayarlanmış olmasıdır.
  
  Farklı modlar için seçenekler aşağıda gösterilmiştir.
  
  ![Structure Scan editor](../../assets/plan/structure_scan_v2/editor_options.jpg)

Kullanıcı her zaman aşağıdaki ayarları yapılandırabilir:

- **Start scan from top/bottom:** Katmanların taranma yönü.
- **Structure height:**Taranan nesnenin yüksekliği.
- **Scan distance:**Uçuş yolunun yapıya olan mesafesi.
- **Entrance/Exit Alt:** Son/sonraki hedef noktası ile taranacak yapı arasındaki engellerden kaçınmak için bu ayarı kullanın. 
  - Araç, bu irtifada *Entrance/Exit* noktasına yükselecek ve ardından taramayı başlatmak için ilk katmana alçalacaktır. 
  - Araç, taramayı tamamladıktan sonra bu irtifaya yükselecek ve ardından bir sonraki hedef noktaya geçecektir.
- **Scan Bottom Alt:**Yapının tabanı etrafındaki engellerden kaçınmak için bu ayarı kullanın. Bu ayar, yapının altını yerden yukarıda olacak şekilde ayarlar ve bu nedenle ilk tarama uçuşu yolunun yüksekliği (en alt katmanın yüksekliği) tarama istatistiklerinde *Bottom Layer Alt* olarak gösterilir.
- **Rotate Entry Point:** Başlangıç/bitiş noktasını uçuş yolundaki bir sonraki köşeye/konuma taşıyın.

Kalan ayarlar *camera mode*'a bağlıdır:

- *Manuel Mod* şunları ayarlamanıza olanak verir: 
  - **Layer height:** Her katmanın yüksekliğini.
  - **Trigger Distance:** Her kamera çekimi arasındaki mesafe. Kamera sadece katman yolunda uçarken çekim yapar. Bir katmandan diğerine geçerken görüntü çekmez.
  - **Gimbal Pitch** - Gimbal pitch you want to use for the scan.

- *Known/pre-defined cameras* automatically calculates layer heights and image triggering from required image overlap, and allows you to trade off scan distance and require image resolution. It also ensures that the camera is always pointed directly at the right angles to the surface which it is capturing images. The settings are:
  
  - **Camera Orientation:** Portrait or Landscape
  - *Overlap*: 
    - **Front Lap:** Image overlap from top to bottom (increasing shrinks layer height and increases layer count).
    - **Side Lap:** Image overlap at sides (increasing takes more images in each lap/layer scan).
  - **Scan distance:** Distance from the structure of the flight path.
  - **Ground Res:** Required image resolution/sample quality of surface.

- *Custom camera* selection allows you to enter your own camera characteristics, but otherwise behaves the same as a predefined camera.