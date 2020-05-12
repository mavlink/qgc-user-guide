# Панель инструментов

The main toolbar provides access to select the different application views, and high level status information for connected vehicles. The toolbar is the same in all views except for "PlanView" (which has a single icon to take you back to "Fly" view).

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

![](../../assets/toolbar/toolbar_status_gps.jpg) **Статус GPS** <br />Показывает количество спутников и текущее HDOP (Horizontal Dilution of Precision) — снижение точности в горизонтальной плоскости.

![](../../assets/toolbar/toolbar_status_rc.jpg) **RSSI радиоуправления** <br />Информация об уровне сигнала радиоуправления.

![](../../assets/toolbar/toolbar_status_telemetry.jpg) **RSSI Телеметрии ** <br />Информация об уровене сигнала канала телеметрии.

![](../../assets/toolbar/toolbar_status_battery.jpg) **Батарея** <br />Информация об остаточной емкости батарее (в процентах).

![](../../assets/toolbar/toolbar_status_flight_mode.jpg) **Режимы полета** <br />Текущий режим полета. Нажмите, чтобы изменить режим полета.

![](../../assets/toolbar/toolbar_status_rtk_gps.jpg) **RTK GPS Survey-In Status** <br />Shows you progress of RTK GPS Survey-In process.