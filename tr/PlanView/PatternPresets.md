# Plan Ekranı - Mod Ön Ayarları

Yaygın olarak kullanılan ayarları adlandırılmış bir ön ayar olarak kaydetmenize olanak sağlar.

> **Note** Şuan için sadece Gözlem modu tarafından desteklenmektedir. Diğer modların desteği için geliştirme devam etmektedir.

## Ön Ayarları Yönetme

![Preset Combo](../../assets/plan/pattern/PatternPresetCombo.jpg)

Mod öğelerinin üst kısmında ön ayarları yönetmenize izin veren bir seçenek vardır:

* **Custom (specify all settings)** Bu bir ön ayar *kullanmamanıza* ve tüm ayarları manuel ayarlamanıza olanak verir.
* **Save Settings As Preset** Mevcut ayarları adlandırılmış bir ön ayar olarak kaydeder.
* **Delete Current Preset** Seçili olan ön ayarı siler.
* **Presets:** Bu öğenin altında bu mod için mevcut ön ayarlar listelenecektir.

## Ön Ayar Oluşturma/Güncelleme

![Preset Save](../../assets/plan/pattern/PatternPresetSave.jpg)

**Save Settings As Preset**'i seçtiğinizde sizden ön ayar için isim istenecektir. Varolan bir ön ayara yeni ayarlar kaydetmek için ön ayar seçiliyken **Save Settings As Preset**'i seçin.

Ayrıca o anda seçili olan kamerayı da ön ayara kaydetmek isteyip istemediğinizi de belirtebilirsiniz. Kamerayı ön ayar ile kaydetmemeyi seçerseniz, ön ayar yüklenirken mevcut kamera kullanılacaktır. Ayrıca ön ayarı kullanırken farklı bir kameraya da geçebilirsiniz. Aracınızı aynı ön ayarla farklı zamanlarda farklı kameralarla uçurmadığınız sürece, kamerayı ön ayara kaydetmeyi seçmelisiniz.

## Ön Ayar Ayarlarını Görüntüleme

If you want to view what the exact settings are for a Preset switch back to **Custom (specify all settings)** which will show you all the settings. Then you can switch back to using the named preset when done.

## Presets In A Plan File

The currently selected Preset is also saved in the Plan file such that when you load the Plan back the preset will once again be selected. Keep in mind that presets are specific to your version of QGroundControl. If you share a Plan file with a preset with another user incorrect behavior may occur if that other user also have a preset of the same name but different settings.