# Панель инструментов

Основная панель инструментов предоставляет доступ к выбору видов приложения и информацию о состоянии подсоединенных БПЛА. Панель инструментов одинакова во всех видах, за исключением "План" (который имеет одну иконку, чтобы вернуть вас обратно в режим "Полет").

## Выбор

Используйте иконки для переключения между *видами*. Показываются, даже если БПЛА не подключен.

![Settings view icon](../../assets/toolbar/toolbar_view_select_settings.jpg) **[Настройки](../SettingsView/SettingsView.md)** <br />Настройка *приложения QGroundControl*.

![Setup view icon](../../assets/toolbar/toolbar_view_select_setup.jpg) **[Настройка](../SetupView/SetupView.md)** <br />Настройка и настройка БПЛА.

![Plan view icon](../../assets/toolbar/toolbar_view_select_plan.jpg) **[План](../PlanView/PlanView.md)** <br />Планирование и создание автономных планов полетов.

![Fly icon](../../assets/toolbar/toolbar_view_select_fly.jpg) **[Полет](../FlyView/FlyView.md)** <br />Мониторинг БПЛА во время полёта, включая потоковое видео.

![Analyze icon](../../assets/toolbar/toolbar_view_select_analyse.jpg) **[Анализ](../analyze_view/README.md)** <br />Скачивание журналов событий, запись географических метаданных в фотографии на основе трека полета, доступ к консоли MAVLink.

## Символы состояния

Символы статуса активны, когда *QGroundControl* подключено к полётному контроллеру. Они сигнализируют об уровнях состояния основных систем необходимых для навигации БПЛА и могут быть нажаты для получения более подробной информации.

![](../../assets/toolbar/toolbar_status_message.jpg) ![yield](../../assets/toolbar/toolbar_status_critical.jpg) **Сообщения БПЛА** <br />Нажмите, чтобы раскрыть список сообщений БПЛА. Внимание! Версия справа отображается при критических сообщениях!

![](../../assets/toolbar/toolbar_status_gps.jpg) **Статус GPS** <br />Количество спутников и надежность HDOP.

![](../../assets/toolbar/toolbar_status_rc.jpg) **RC RSSI** <br />Информация о надежности сигнала RC.

![](../../assets/toolbar/toolbar_status_telemetry.jpg) **RSSI Телеметрия** <br />Уровень сигнала канала телеметрии.

![](../../assets/toolbar/toolbar_status_battery.jpg) **Батарея** <br />Информация об остаточной емкости батарее (в процентах).

![](../../assets/toolbar/toolbar_status_flight_mode.jpg) **Режимы полета** <br />Текущий режим полета. Нажмите, чтобы изменить режим полета.

![](../../assets/toolbar/toolbar_status_rtk_gps.jpg) **RTK GPS Survey-In Status** <br />Показывает прогресс процесса RTK GPS Survey-In.