# Video Overlay

QGroundControl bir video akışını dosyaya kaydederken, aynı zamanda oynatma sırasında video üzerinde telemetriyi göstermek için kullanılabilen, telemetri verilerini içeren bir altyazı dosyasını da dışa aktarır. Telemetri [değerleri widget](FlyView.md#values-telemetry)ında gösterilmesi için hangi telemetri değerleri seçilirse seçilsin, onlar da overlaye aktarılacaktır. Overlay değerleri 1Hz hızla güncellenecektir.

![Değerler Widgetı](../../assets/fly/overlay_widget.png)

Seçilen değerler ekran kullanımını optimize etmek için 3 sütun halinde düzenlenmiştir. ![Overlay in action](../../assets/fly/overlay_capture.png)

## Oynatma

Overlay, [SubStation Alpha](https://en.wikipedia.org/wiki/SubStation_Alpha#Players_and_renderers) altyazı formatını destekleyen tüm oynatıcılarla birlikte kullanılabilir. Çoğu oynatıcı videoyu oynatmayı denediğinizde iki dosyayı birden açacaktır. QGC tarafından oluşturuldukları gibi, iki dosyanında aynı dosyada aynı isimle olması gerekmektedir.

## Handbrake'i Kullanarak Kalıcı Video Altyazıları

Altyazılar [HandBrake](https://handbrake.fr/)'i kullanarak kalıcı olarak video dosyalarına eklenebilir. Bu, altyazıları tüm oynatıcılar için kalıcı olarak görünür yapacaktır.

**HandBrake**'i açın, ana arayüzünü göreceksiniz. **Open**'a tıklayın ve video dosyasını seçin.

![Handbrake UI showing how to open video file](../../assets/fly/videoOverlay/1-open.png)

Video dosyası yüklenirken, subtitles sekmesine geçin. Altyazı dosyasını yüklemek için **Add**'e tıklayın.

![Handbrake UI screenshot showing how to add subtitles](../../assets/fly/videoOverlay/2-subtitles.png)

**import SSA**'ı seçin ( [ASS](https://en.wikipedia.org/wiki/SubStation_Alpha#Advanced_SubStation_Alpha) SSA'nın bir uzantısıdır).

![Import SSA file](../../assets/fly/videoOverlay/3-ssa.png)

Videonuza karşılık gelen **.ass** dosyasını videonuza yükleyin ve **Burn into video**'u işaretleyin.

![burn](../../assets/fly/videoOverlay/4-openandburn.png)

Yeni dosyanın nereye kaydedilmesini istediğinizi seçin ve **Start**'a tıklayın.

![Start burning new file](../../assets/fly/videoOverlay/5-start.png)

Bu, altyazıyı ve videoyu yeni bir dosyaya yazmaya başlayacaktır.