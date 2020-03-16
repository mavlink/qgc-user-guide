# Экран "Полет"

Экран "Полет" используется для управления и мониторинга БПЛА в полете.

Вы можете использовать его для:

- Запустите автоматизированный контрольный список [перед полетом](#preflight_checklist).
- Контрольные задачи: [start](#start_mission), [continue](#continue_mission), [pause](#pause), и [возобновление](#resume_mission).
- Направлять автомобиль на [руку](#arm)/[disarm](#disarm)/[аварийную остановку](#emergency_stop), [взлет](#takeoff)/[земля](#land), [изменить высоту](#change_altitude), [перейти к](#goto) или [орбита](#orbit) конкретное местоположение и [вернуться/RTL](#rtl).
- Переключение между отображением карты и видео (если доступно)
- Отображение видео, миссии, телеметрии и другой информации для текущего транспортного средства, а также переключение между подключенными автомобилями.

![Экран "Полет"](../../assets/fly/fly_view_overview.jpg)

## Обзор

На скриншоте выше показаны основные элементы вида полета:

- **Карта:** Отображает положение всех подключенных транспортных средств и миссию для текущего транспортного средства. 
  - Вы можете перетащить карту, чтобы переместить ее по карте (карта автоматически перестает по центру через определенное время).
  - После полета, вы можете нажать на карту, чтобы установить [Перейти к](#goto) или [Орбит на](#orbit) местоположения.
- **Панель инструментов:** Информация о ключевом статусе датчиков (GPS, аккумулятора, управления РК) и состояния транспортного средства (режим полета, состояние "Армян/разоружен"). 
  - Выберите индикаторы датчика для более подробного просмотра.
  - Нажмите *Режим полета* текст (например, "Задержать") для выбора нового режима. Не каждый режим может быть доступен.
  - Нажмите *Armed/Disarmed* текст для переключения вооруженного состояния. При полете вы можете нажать этот текст на *аварийная остановка*.
- **Панель управление полетом:** Вы можете использовать его для: 
  - Переключение между взлет/посадка.
  - Пауза/перезапуск текущую операцию (например, посадку или миссию).
  - Возврат в исходное положение (также известен как RTL или возврат).
  - Кнопка *Действия* предлагает другие соответствующие опции для текущего состояния (вызывая окно со *Слайдером подтверждения*). Эти действия включают в себя изменение высоты или продолжение миссии.
  - Включите список [preflight checklist](#preflight_checklist) (утилита отключена по умолчанию).
- **[Панель инструментов](#instrument_panel):** многостраничный виджет с информацией о БПЛА, включающий в себя: телеметрию, камеру, видео, общее состояние системы и вибрацию.
- **[Video/Switcher](#video_switcher):** Переключение между видео или картой в окне. 
  - Нажмите на элемент для переключения *Видео* и *Карта* для переключения на передний план.
  - *QGroundControl* supports RTP and RTSP video streaming over your vehicles UDP connection. Также поддерживается поддержка устройств UVC. Поддержка видео QGC обсуждается в [Видео README](https://github.com/mavlink/qgroundcontrol/blob/master/src/VideoStreaming/README.md).
  - A [Telemetry Overlay](../FlyView/VideoOverlay.md) is automatically generated as a subtitle file
- **Confirmation Slider:** Context sensitive slider to confirm requested actions. Проведите для начала операции. Нажмите **X** для отмены.

Некоторые элементы отображаются только в определенных условиях и не отображаются по умолчанию. Например, селектор с выбора БПЛА, отображается только в том случае, если у вас их несколько , и кнопка предполетного контрольного списка отображается только при включенной соответствующей настройке.

## Панель инструментов {#instrument_panel}

Это многостраничный виджет с информацией о БПЛА, включающий в себя: телеметрию, камеру, видео, общее состояние системы и вибрацию.

По умолчанию отображается телеметрия БПЛА - используйте выпадающее меню справа для выбора других параметров.

### Значения (Телеметрия)

The values page shows telemetry information; by default the altitude (relative to the home location) and the ground speed.

![Страница Инструментов - значения/телеметрия](../../assets/fly/instrument_page_values.jpg)

You can configure what information is display by pressing the small gear icon on the top left of the panel. Each value can be displayed in normal or "large" size (large size shows just one value per row in the page, while normal shows 2).

![Instrument Page - values settings](../../assets/fly/instrument_page_values_settings.jpg)

### Камера {#camera_instrument_page}

The camera page is used to configure and control the camera. For a camera connected directly to the Flight Controller the only available option is camera triggering:

![Страница Инструментов - камера](../../assets/fly/instrument_page_camera.jpg)

When connected to camera that supports the [MAVLink Camera Protocol](https://mavlink.io/en/services/camera.html) you can additionally configure and use other camera services that it makes available. For example, if your camera supports video mode you will be able to switch between still image capture and video mode, and start/stop recording.

![Instrument Page - Camera MAVLink Settings](../../assets/fly/instrument_page_camera_mavlink.jpg)

Advanced settings can be changed via the gear icon at the top left of the page.

![Instrument Page - Camera MAVLink Settings](../../assets/fly/instrument_page_camera_mavlink_settings.jpg)

> **Note** Most of the settings that are displayed depend on the camera (they are defined in its [MAVLink Camera Definition File](https://mavlink.io/en/services/camera_def.html)). A few common settings at the end are hard-coded: Photo Mode (Single/Time Lapse), Photo Interval (if Time Lapse), Reset Camera Defaults (sends a reset command to the camera), Format (storage)

### Видеопоток {#video_instrument_page}

The video page is used to enable/disable video streaming. When enabled, you can start/stop the video stream, enable a grid overlay, change how the image fits the screen, and record the video locally with QGC.

![Страница Инструментов - видео поток](../../assets/fly/instrument_page_video_stream.jpg)

### Health

The health page shows you the health of the systems within your vehicle. *QGroundControl* will switch to this page automatically if any systems change to unhealthy.

![Страница Инструментов - хорошее состояние БПЛА ](../../assets/fly/instrument_page_health_good.jpg) ![Страница Инструментов - плохое состояние БПЛА ](../../assets/fly/instrument_page_health_bad.jpg)

### Вибрация

The vibration page shows current vibration levels and clip counts.

![Страница Инструментов - вибрация](../../assets/fly/instrument_page_vibration.jpg)

## Действия / Задачи

The following sections describe how to perform common operations/tasks in the Fly View.

> **Note** Many of the available options depend on both the vehicle type and its current state.

### Предполетный чек-лист {#preflight_checklist}

An automated preflight checklist can be used to run through standard checks that the vehicle is configured correctly and it is safe to fly.

To you the checklist, first enable the tool by navigating to [Application Settings > General > Fly View](../SettingsView/General.md) and selecting the **Use preflight checklist** checkbox. The tool will then be added to the *Flight Tools*. Press it to open the checklist:

![Предполетный чек-лист](../../assets/fly/pre_flight_checklist.jpg)

Once you have performed each test, select it on it in the UI to mark it as complete.

### Arm {#arm}

> **Tip** Generally *QGroundControl* does not require you to arm the vehicle explicitly; this is done for you if you start a mission or takeoff.

Arming a vehicle starts the motors in preparation for takeoff.

To arm the vehicle, select **Disarmed** in the *Fly Toolbar* and then use the confirmation sider.

![Arm](../../assets/fly/arm.jpg)

> **Note** Vehicles usually disarm automatically if you do not take off after a few seconds.

### Disarm {#disarm}

Disarming the vehicle stops the motors (making the vehicle safe). To disarm the vehicle select **Armed** in the *Fly Toolbar* when the vehicle is **landed**.

![Disarm](../../assets/fly/disarm.jpg)

> **Note** Disarming the vehicle while it is flying is called an [Emergency Stop](#emergency_stop)

### Emergency Stop {#emergency_stop}

Emergency stop is effectively the same as disarming the vehicle while you are flying. Your vehicle will crash!

To disarm the vehicle select **Armed** in the *Fly Toolbar* when the vehicle is flying.

![Аварийная остановка](../../assets/fly/emergency_stop.jpg)

### Взлет {#takeoff}

> **Tip** If you are starting a mission for a multicopter *QGroundControl* will automatically perform the takeoff step.

To takeoff (when landed):

1. Press the **Takeoff** button in the *Fly Tools* (this will toggle to a **Land** button after taking off).
2. Optionally set the takeoff altitude in the right-side vertical slider.
3. Confirm takeoff using the slider.

![взлет](../../assets/fly/takeoff.jpg)

### Посадка {#land}

You can land at the current position at any time while flying:

1. Press the **Land** button in the *Fly Tools* (this will toggle to a **Land** button when landed).
2. Confirm landing using the slider.

![посадка](../../assets/fly/land.jpg)

### RTL/Возврат

Return to the home position at any time while flying:

1. Press the **RTL** button in the *Fly Tools*.
2. Confirm RTL using the slider.

![посадка](../../assets/fly/land.jpg)

> **Note** The vehicle may also land at the home position, depending on its type and configuration.

### Смена высоты {#change_altitude}

You can change altitude while flying, except when in a mission:

1. Press the **Action** button on the *Fly Tools*
2. Select the *Change Altitude* action from the dialog.
  
  ![Продолжение полётного задания/изменение высоты](../../assets/fly/continue_mission_change_altitude_action.jpg)

3. Move the vertical slider to the desired altitude, then drag the confirmation slider to start the action.
  
  ![Смена высоты](../../assets/fly/change_altitude.jpg)

### Двигаться к местоположению {#goto}

After taking off you can specify that you want to fly to a particular location.

1. Press the map where you want the vehicle to move and select **Go to location** on the popup.
  
  ![Goto or orbit](../../assets/fly/goto_or_orbit.jpg)

2. The location will be displayed on the map, along with a confirmation slider.
  
  ![Подтверждение перехода](../../assets/fly/goto.jpg)

3. When you're ready, drag the slider to start the operation (or press the **X** icon to cancel it).

> **Note** Goto points must be set within 1 km of the vehicle (hard-coded in QGC).

### Orbit Location {#orbit}

After taking off you can specify that you want to orbit a particular location.

1. Press on the map (near the centre of your desired orbit) and select **Orbit at location** on the popup.
  
  ![Goto or orbit](../../assets/fly/goto_or_orbit.jpg)

2. The proposed orbit will be displayed on the map, along with a confirmation sider.
  
  ![Orbit confirmation](../../assets/fly/orbit.jpg)
  
  - Select and drag the central marker to move the orbit location.
  - Select and drag the dot on the outer circle to change the orbit radius
3. When you're ready, drag the slider to start the operation (or press the **X** icon to cancel it).

### Пауза

You can pause most operations, including taking off, landing, RTL, missions, Orbit at location. The vehicle behaviour when paused depends on the vehicle type; typically a multicopter will hover, and a fixed wing vehicle will circle.

> **Note** You cannot pause a *Goto location* operation.

To pause:

1. Press the **Pause** button in the *Fly Tools*.
2. Optionally set a new altitude using the right-side vertical slider.
3. Confirm the pause using the slider.

![пауза](../../assets/fly/pause.jpg)

### Полётные задания

#### Начало полетного задания {#start_mission}

You can start a mission when the vehicle is landed (the start mission confirmation slider is often displayed by default).

To start a mission from landed:

1. Press the **Action** button on the *Fly Tools*
2. Select the *Start Mission* action from the dialog.
  
  ![Подтверждение начала полетного задания](../../assets/fly/start_mission_action.jpg)
  
      (to display the confirmation slider)
      

3. When the confirmation slider appears, drag it to start the mission.
  
  ![Начало полетного задания](../../assets/fly/start_mission.jpg)

#### Продолжение полетного задания {#continue_mission}

You can *continue* mission from the *next* waypoint when you're flying (the *Continue Mission* confirmation slider is often displayed by default after you takeoff).

> **Note** Continue and [Resume mission](#resume_mission) are different! Continue is used to restart a mission that has been paused, or where you have taken off, so you've already missed a takeoff mission command. Resume mission is used when you've used a RTL or landed midway through a mission (e.g. for a battery change) and then wish to continue the next mission item (i.e. it takes you to where you were up to in the mission, rather than continuing from you place in the mission).

You can continue the current mission while (unless already in a mission!):

1. Press the **Action** button on the *Fly Tools*
2. Select the *Continue Mission* action from the dialog.
  
  ![Продолжение полётного задания/изменение высоты](../../assets/fly/continue_mission_change_altitude_action.jpg)

3. Drag the confirmation slider to continue the mission.
  
  ![Продолжение полетного задания](../../assets/fly/continue_mission.jpg)

#### Возобновление полетного задания {#resume_mission}

*Resume Mission* is used to resume a mission after performing an [RTL/Return](#rtl) or [Land](#land) from within a mission (in order, for example, to perform a battery change).

> **Note** If you are performing a battery change, **do not** disconnect QGC from the vehicle after disconnecting the battery. After you insert the new battery *QGroundControl* will detect the vehicle again and automatically restore the connection.

After landing you will be prompted with a *Flight Plan complete* dialog, which gives you the option to remove the plan from the vehicle, leave it on the vehicle, or to resume the mission from the last waypoint that was traveled through.

![Возобновление полетного задания](../../assets/fly/resume_mission.jpg)

If you select to resume the mission, then *QGroundControl* will rebuild the mission and upload it to the vehicle. Then use the *Start Mission* slider to continue the mission.

The image below shows the mission that was rebuilt after the Return shown above.

![Возобновление измененного полетного задания](../../assets/fly/resume_mission_rebuilt.jpg)

> **Note** A mission cannot simply resume from the last mission item that the vehicle executed, because there may be multiple items at the last waypoint that affect the next stage of the mission (e.g. speed commands or camera control commands). Instead *QGroundControl* rebuilds the mission, starting from the last mission item flown, and automatically prepending any relevant commands to the front of the mission.

#### Remove Mission Prompt After Landing {#resume_mission_prompt}

You will be prompted to remove the mission from the vehicle after the mission completes and the vehicle lands and disarms. This is meant to prevent issues where stale missions are unknowingly left on a vehicle, potentially resulting in unexpected behavior.

### Показ видео {#video_switcher}

When video streaming is enabled, *QGroundControl* will display the video stream for the currently selected vehicle in the "video switcher window" at the bottom left of the map. You can press the switcher anywhere to toggle *Video* and *Map* to foreground (below we show the video in the foreground).

![Запись видео потока](../../assets/fly/video_record.jpg)

> **Note** Video streaming is configured/enabled in [Application Settings > General tab > Video](../SettingsView/General.md#video).

You can further configure video display using controls on the switcher:

    ![Video Pop](../../assets/fly/video_pop.jpg)
    

- Resize the switcher by dragging the icon in the to right corner.
- Hide the switcher by pressing the toggle icon in the lower left.
- Detach the video switcher window by pressing on the icon in its top left corner (once detached, you can move and resize the window just like any other in your OS). If you close the detached window the switcher will re-lock to the QGC Fly view.

### Запись видео

If supported by the camera and vehicle, *QGroundControl* can start and stop video recording on the camera itself. *QGroundControl* can also record the video stream and save it locally.

> **Tip** Video stored on the camera may be of much higher quality, but it is likely that your ground station will have a much larger recording capacity.

#### Запись видео потока (на наземную станцию)

Video stream recording is controlled on the [video stream instrument page](#video_instrument_page). Press the red circle to start recording a new video (a new video file is created each time the circle is pressed); the circle will change into a red square while recording is in progress.

![Запись видео потока](../../assets/fly/video_record.jpg)

Video stream recording is configured in the [Application Settings > General tab](../SettingsView/General.md):

- [Video Recording](../SettingsView/General.md#video-recording) - specifies the recording file format and storage limits. > **Note** Videos are saved in Matroska format (.mkv) by default. This format is relatively robust against corruption in case of errors.
- [Miscellaneous](../SettingsView/General.md#miscellaneous) - Streamed video is saved under the **Application Load/Save Path**. 

> **Tip** The stored video includes just the video stream itself. To record video with QGroundControl application elements displayed, you should use separate screen recording software.

#### Записать видео (на камеру)

Start/stop video recording *on the camera itself* using the [camera instrument page](#camera_instrument_page). First toggle to video mode, then select the red button to start recording.

![Страница Инструментов - Настройка MAVLink камеры](../../assets/fly/instrument_page_camera_mavlink.jpg)