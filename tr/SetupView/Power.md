# Güç Kurulumu

*Power Setup* ekranı batarya parametrelerini düzenlemek için kullanılır ve ayrıca pervaneler hakkında gelişmiş ayarlar sunar.

![Battery Calibration](../../assets/setup/PX4Power.jpg)

## Batarya Voltaj/Akım Kalibrasyonu

Batarya/güç modülünüz için veri sayfasından verileri girin: hücre sayısı, hücre başına tam voltaj, hücre başına boş voltaj. Eğer varsa, voltaj bölücü ve volt başına amper bilgilerini de girin.

*QGroundControl*, ölçümlerden uygun voltaj bölücü ve volt başına amper değerlerini hesaplamak için kullanılabilir:

1. Bir multimetre kullanarak pilden gelen voltajı ölçün.
2. *Voltage divider*'ın yanındaki **Calculate** butonuna tıklayın. Gelen pencerede: 
    1. Ölçülen voltajı girin.
    2. **Calculate**'e tıklayarak yeni bir voltaj bölücü değeri oluşturun.
    3. Değeri ana forma kaydetmek için **Close**'a tıklayın. 
3. Bataryadaki akımı ölçün.
4. *Amps per volt*'un yanındaki **Calculate** butonuna tıklayın. Gelen pencerede: 
    1. Ölçülen akımı girin.
    2. **Calculate**'e tıklayarak yeni bir *volt başına akım* değeri oluşturun.
    3. Değeri ana forma kaydetmek için **Close**'a tıklayın. 

## Gelişmiş Güç Ayarları

Gelişmiş güç ayarlarını özelleştirmek için **Show Advanced Settings** onay kutusuna tıklayın.

### Tam Yükte Voltaj Düşüşü

Bataryalar yüksek motor yüklemelerinde daha az voltaj gösterir. Motorlar boştayken ve tam kapasitede çalışırkenki volt farkını batarya hücrelerinin sayısına bölerek girin. Emin değilseniz varsayılan değer kullanılmalıdır!

> **Warning** If the value is too high the battery may be deep-discharged and damaged.

## ESC PWM Minimum and Maximum Calibration

To calibrate the ESC max/min PWM values:

1. Remove the propellers. 
2. Connect the vehicle to QGC via USB (only). 
3. Click the **Calibrate** button.

> **Warning** Never attempt ESC calibration with props on.
> 
> Motors should not spin during ESC calibration. However if an ESC doesn't properly support/detect the calibration sequence then it will respond to the PWM input by running the motor at maximum speed.

## Other Settings

Select the **Show UAVCAN Settings** checkbox to access additional settings for UAVCAN Bus Configuration and motor index and direction assignment.