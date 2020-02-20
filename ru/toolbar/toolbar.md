# Панель инструментов

The main menu/tool bar provides access to the different application views, and high level status information for connected vehicles. The menu is the same in all views except for "PlanView" (which has a single icon to take you back to "Fly" view).

## View-select icons

The following icons are used to switch between the main *Views*. These are displayed even if no vehicle is connected.

![Settings view icon](../../assets/toolbar/toolbar_view_select_settings.jpg) **[Настройки](../SettingsView/SettingsView.md)** <br />Настройка *приложения QGroundControl*.

![Setup view icon](../../assets/toolbar/toolbar_view_select_setup.jpg) **[Настройка](../SetupView/SetupView.md)** <br />Настройка и настройка БПЛА.

![Plan view icon](../../assets/toolbar/toolbar_view_select_plan.jpg) **[План](../PlanView/PlanView.md)** <br />Планирование и создание автономных планов полетов.

![Fly icon](../../assets/toolbar/toolbar_view_select_fly.jpg) **[Полет](../FlyView/FlyView.md)** <br />Следите за БПЛА во время полёта, включая потоковое видео.

![Analyze icon](../../assets/toolbar/toolbar_view_select_analyse.jpg) **[Анализ](../analyze_view/README.md)** <br />Скачивание журналов событий, запись географических метаданных в фотографии на основе трека полета, доступ к консоли MAVLink.

## Символы состояния

Символы статуса активны, когда *QGroundControl* подключено к полётному контроллеру. Они сигнализируют об уровнях состояния основных систем необходимых для навигации БПЛА и могут быть нажаты для получения более подробной информации.

![](../../assets/toolbar/toolbar_status_message.jpg) **Сообщения БПЛА** <br />Нажмите, чтобы показать раскрывающийся список сообщений от БПЛА. This will change to a Yield sign if there are critical messages.

![](../../assets/toolbar/toolbar_status_gps.jpg) **GPS Status** <br />Shows you satellite count and curent hdop.

![](../../assets/toolbar/toolbar_status_rc.jpg) **RC RSSI** <br />RS signal strength information.

![](../../assets/toolbar/toolbar_status_telemetry.jpg) **Telemetry RSSI** <br />Telemetry signals strength information.

![](../../assets/toolbar/toolbar_status_battery.jpg) **Battery** <br />Remaining battery percent.

![](../../assets/toolbar/toolbar_status_flight_mode.jpg) **Flight Mode** <br />Current flight mode. Click to change flight mode.

![](../../assets/toolbar/toolbar_status_rtk_gps.jpg) **RTK GPS Survey-In Status** <br />Shows you progress of RTK GPS Survey-In process.