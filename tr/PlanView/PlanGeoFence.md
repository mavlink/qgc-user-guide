# Plan Ekranı - Coğrafi Sınır

Coğrafi Sınırlar, aracınızın içinde uçmasına izin verilen ya da *izin verilmeyen* sanal bölgeler oluşturmanıza olanak sağlar. Ayrıca eğer izin verilen alanın dışına çıkıldığında yaplıacak eylemi de ayarlayabilirsiniz.

![Coğrafi Sınır'a geneş bakış](../../assets/plan/geofence/geofence_overview.jpg)

> **Note** **ArduPilot users:** Coğrafi Sınır sadece Rover 3.6 ve Copter3.7 ve üzeri sürümlerde desteklenir. Ek olarak günlük sürümlerin ya da stabil 3.6 sürümünün (erişilebilir olduğunda) kullanılmasını gerektirir. Eğer bağlanan cihaz tarafından Coğrafi Sınır seçeneği desteklenmiyorsa *QGroundControl* seçeneği göstermeyecektir.

## Coğrafi Sınır Oluşturma

Coğrafi Sınır Oluşturmak için:

1. Plan Ekranı'na gidin
2. Görev Komutları Listesi'nin üstünden *Geofence*'i seçin
    
    ![Coğrafi Sınır butonunu seç](../../assets/plan/geofence/geofence_select.jpg)

3. **Circular Fence** ya da **Polygon Fence** butonlarına basarak, sırasıyla dairesel ya da çokgen bölgeler ekleyin. Haritaya yeni bir bölge ve butonların altına sınırlarla ilgili yeni bir liste eklenecektir.
    
    > **Tip** Butonlara birden çok kez basarak birden çok bölge oluşturabilirsiniz, böylece karmaşık coğrafi sınırlar oluşturulabilir.

- Dairesel Bölge:
    
    ![Dairesel Coğrafi Sınır](../../assets/plan/geofence/geofence_circular.jpg)
    
    - Merkezi noktayı kaydırarak bölgeyi haritada hareket ettirin
    - Dairenin sınırındaki noktayı sürükleyerek boyutunu ayarlayın (veya sınırlar panelindeki yarıçapı değiştirebilirsiniz).

- Çokgen Bölge:
    
    ![Çokgen Coğrafi Sınır](../../assets/plan/geofence/geofence_polygon.jpg)
    
    - İçi dolu noktaları sürükleyerek köşeleri hareket ettirin
    - İçi dolu noktaların arasındaki içi boş noktalara basarak yeni köşeler oluşturun. 
        1. Varsayılan olarak, *inclusion* bölgeleri olarak yeni bölgeler oluşturulur (araçlar bölge içinde kalmalıdır). Sınır panelindeki *Inclusion* onay kutusunun tikini kaldırarak, exclusion bölgelerine (aracın içinde uçamayacağı) dönüştürebilirsiniz.

## GeoFence Düzenleme/Silme

Coğrafi Sınır panelinde *Edit* butonunu seçerek düzenlemek için bir coğrafi sınır bölgesi seçebilirsiniz. Daha sonra, önceki bölümde anlatıldığı gibi haritadaki bölgeyi düzenleyebilirsiniz.

Bölgeler, **Del** düğmesine basılarak silinebilir

## Coğrafi Sınır Yükleme

GeoFence bir görevle aynı şekilde yüklenir, [Plan tools](../PlanView/PlanView.md)'dan **File**'ı kullanarak.

## Diğer Araçlar

Araçların geri kalanı, bir Görevi düzenlerken olduğu gibi çalışır.