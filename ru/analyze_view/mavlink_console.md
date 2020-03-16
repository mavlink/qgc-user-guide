# Консоль MAVLink (Экран Анализа)

Консоль MAVLink (**Анализ > Консоль MAVLink**) позволяет вам подключаться к PX4 [nsh оболочке](https://dev.px4.io/en/debug/system_console.html) и передавать команды.

> **Примечание** консоль работает только при подключении к *оборудованию* полетного контроллера *PX4*. PX4 SITL и ArduPilot не поддерживаются.

<span></span>

> **Совет** Это очень полезная функция для разработчиков, так как она предоставляет глубокий доступ к системе. В частности, если вы подключены через Wifi, вы можете иметь такой же уровень доступа во время полета БПЛА.

![Экран Анализа Консоль MAVLink](../../assets/analyze/mavlink_console.jpg)

The view does not display any output except in response to commands. Once the vehicle is connected, you can enter commands in the bar provided (for a full list of available commands enter: `?`).

Command output is displayed in the view above the command bar. Click **Show Latest** to jump to the bottom of the command output.