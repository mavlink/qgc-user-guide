# Video Overlay

QGroundControl bir video akışını dosyaya kaydederken, aynı zamanda oynatma sırasında video üzerinde telemetriyi göstermek için kullanılabilen, telemetri verilerini içeren bir altyazı dosyasını da dışa aktarır. Telemetri [değerleri widget](FlyView.md#values-telemetry)ında gösterilmesi için hangi telemetri değerleri seçilirse seçilsin, onlar da overlaye aktarılacaktır. Overlay değerleri 1Hz hızla güncellenecektir.

![Values Widget](../../assets/fly/overlay_widget.png)

Seçilen değerler ekran kullanımını optimize etmek için 3 sütun halinde düzenlenmiştir. ![Overlay in action](../../assets/fly/overlay_capture.png)

## Oynatma

Overlay, [SubStation Alpha](https://en.wikipedia.org/wiki/SubStation_Alpha#Players_and_renderers) altyazı formatını destekleyen tüm oynatıcılarla birlikte kullanılabilir. Most players will open both files together when you try to play the video. They need to be in the same folder and with the same name, which is how they are created by QGC.

## Permanent Video Subtitles using Handbrake

Subtitles can be permanently added to a video file using [HandBrake](https://handbrake.fr/). This will make the subtitles permanently visible on any video player.

Open **HandBrake**, you should see its main interface. Click **Open** and select the video file.

![Handbrake UI showing how to open video file](../../assets/fly/videoOverlay/1-open.png)

With the video file loaded, switch to the subtitles tab. Click **Add** to load the subtitle file.

![Handbrake UI screenshot showing how to add subtitles](../../assets/fly/videoOverlay/2-subtitles.png)

Choose **import SSA** ([ASS](https://en.wikipedia.org/wiki/SubStation_Alpha#Advanced_SubStation_Alpha) is an extension of SSA).

![Import SSA file](../../assets/fly/videoOverlay/3-ssa.png)

Load the **.ass** file corresponding to your video and tick the **Burn into video** checkbox.

![burn](../../assets/fly/videoOverlay/4-openandburn.png)

Choose where you want to save the new file and click **Start**.

![Start burning new file](../../assets/fly/videoOverlay/5-start.png)

This will start burning the subtitle and video to a new file.