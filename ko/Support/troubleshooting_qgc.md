# QGC Installation/Configuration Problems

This topic lists troubleshooting information related to **running** *QGroundControl* on the host computer (e.g. QGC setup and configuration issues).

> **Tip** Problems when **using** *QGroundControl* to interact with a vehicle are covered in: [QGC/Vehicle Interaction Problems](../Support/CommonProblems.md).

## 64-bit Windows: Audio in Unexpected Language

On Windows 64-bit machines *QGroundControl* may sometimes play audio/messages in a language that does not match the *Text-to-speech* setting in **Control Panel > Speech** (e.g. audio spoken in German on an English machine).

This can occur because 64-bit Windows only displays 64-bit voices, while *QGroundControl* is a 32-bit application (on Windows) and hence can only run 32-bit voices.

The solution is to set the desired *32-bit voice* for your system:

1. Run the control panel application: **C:\Windows\SysWOW64\Speech\SpeechUX\sapi.cpl**.
2. Make your desired *Voice selection* and then click **OK** at the bottom of the dialog. ![Windows 32-bit Text-To-Speech Control Panel](../../assets/support/windows_text_to_speech.png)

> **Note** Additional information about the Windows speech APIs can be found [here](https://www.webbie.org.uk/blog/microsoft-speech/).

## Windows: UI Rendering/Video Driver Issues {#opengl_troubleshooting}

If you experience UI rendering issues or video driver crashes on Windows, this may be caused by "flaky" OpenGL drivers. *QGroundControl* provides 3 shortcuts that you can use to start *QGroundControl* in "safer" video modes (try these in order):

- **QGroundControl:** QGC uses OpenGL graphics drivers directly.
- **GPU Compatibility Mode:** QGC uses ANGLE drivers, which implement OpenGL on top of DirectX.
- **GPU Safe Mode:** QGC uses a software rasterizer for the UI (this is very slow).

## Windows: Waiting For Vehicle Connection over WiFi {#waiting_for_connection}

If *QGroundControl* sits forever *Waiting For Vehicle Connection* when trying to connect to the vehicle over Wifi, a possible cause is that IP traffic is being blocked by firewall software (e.g. Windows Defender, Norton, etc.).

![Waiting for connection](../../assets/support/waiting_for_connection.jpg)

The solution is to allow the *QGroundControl* app through the firewall.

If using *Windows Defender*:

- In the **Start** bar, enter/select: *Firewall & Network Protection* (System Settings).
- Scroll to and select the option: *Allow an app through firewall*.
- Select *QGroundControl* and change the *Access* selector to **Allow**. > **Tip** Programs are listed in alphabetical order by description (not filename). You'll find QGC under **O**: *Open source ground control app provided by QGroundControl dev team*

## Ubuntu: Video Streaming Fails {#waiting_for_connection}

On Ubuntu you must install *Gstreamer* components in order to see video streams. If these are not installed *QGroundControl* is unable to create the gstreamer nodes and fails with:

```sh
VideoReceiver::start() failed. Error with gst_element_factory_make(‘avdec_h264’)
```

The [download/install instructions for Ubuntu](../getting_started/download_and_install.md#ubuntu) include *GStreamer* setup information.