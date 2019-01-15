# Audio Problems


## 64-bit Windows: Audio in Unexpected Language

On Windows 64-bit machines *QGroundControl* may sometimes play audio/messages in a language that does not match the *Text-to-speech* setting in **Control Panel > Speech** (e.g. audio spoken in German on an English machine).

This can occur because 64-bit Windows only displays 64-bit voices, while *QGroundControl* is a 32-bit application (on Windows) and hence can only run 32-bit voices.

The solution is to set the desired *32-bit voice* for your system:
1. Run the control panel application: **C:\Windows\SysWOW64\Speech\SpeechUX\sapi.cpl**.
2. Make your desired *Voice selection* and then click **OK** at the bottom of the dialog.
   ![Windows 32-bit Text-To-Speech Control Panel](../../assets/support/windows_text_to_speech.png)

> **Note** Additional information about the Windows speech APIs can be found [here](https://www.webbie.org.uk/blog/microsoft-speech/).