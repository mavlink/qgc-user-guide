# Motorların Kurulumu (ArduSub)

ArduSub'un düzgün çalışması için motorların doğru şekilde kurulması gerekir.

ROV'nuzu yeni monte ettiyseniz, önce ** Manuel Test ** bölümünde iticilerin doğru çıkışlara bağlandığından emin olun. Her kaydırıcıyı sürükleyin ve görüntülenen gövdeye göre * doğru motorun * döndüğünden emin olun.

İticilerinin uygun çıkışlara bağlandığından emin olduktan sonra,* doğru yönü * (ileri / geri) kontrol etmek için [ otomatik yön algılama ](#automatic) (ArduSub 4.0'dan iibaren tavsiye edilir) veya [ manuel test](#manual) seçeneklerinden birini kullanabilirsiniz.

> ** Note ** [ Manuel Test ](#manual) ArduSub tarafından 3.5 sürümüne kadar desteklenirken, ArduSub 4.0 hem [ Manuel Testi ](#manual) hem de [ otomatik yön algılamayı ](#automatic) destekler.

## Manuel Test {#manual}

ArduSub motor kurulumu, motorları teker teker test etmenize olanak sağlar. Kaydırıcılar, her motorun ileri veya geri modda döndürülmesine izin verir ve kaydırıcıların altındaki onay kutuları, tek tek iticilerin çalışmasını tersine çevrilmesine olanak tanır.

Sağdaki resim, her bir iticinin konumu ve yönü ile birlikte şu anda kullanımda olan gövdeyi gösterir. Eğer gövde seçimi aracınıza uymuyorsa, önce [Frame ](../SetupView/airframe_ardupilot.md#ardusub) sekmesinden doğru gövdeyi seçin.

Motorları manuel olarak kurmak ve test etmek için sayfadaki talimatları okuyun ve uygulayın.

> **Warning** Aracı devreye almak ve testi etkinleştirmek için anahtarı kaydırmadan önce motorların ve pervanelerin engellerden uzak olduğundan emin olun!

![Ardusub Motors Test](../../assets/setup/motors-sub.jpg)

## Otomatik Yön Algılama {#automatic}

Ardusub 4.0 ve daha yeni sürümler, motor yönlerinin otomatik olarak algılanmasını destekler. This works by applying pulses to each motor, checking if the frame reacts as expected, and reversing the motor if necessary. The process takes around one minute.

To perform the automatic motor direction detection, navigate to **Vehicle Setup->Motors** tab, click the **Auto-Detect Directions** button and wait. Additional output about the process will be shown next to the button as it runs.

> **Warning** This procedure still requires that the motors are connected to the *correct outputs* as shown in the frame view!

![Ardusub Motors Auto-Setup](../../assets/setup/motors-sub-auto.jpg)
