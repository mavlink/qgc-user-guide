# Повтор данных полета

> **Warning** This feature is intended primarily for **autopilot developers**/**vehicle creators**. It is only supported on desktop builds (Windows, Linux, Mac OS).

The *Replay Flight Data* features allows users to replay a telemetry log, enabling review of past or problematic flights. The flight can be started, paused, stopped, restarted etc.

> **Note** *QGroundControl* treats flight replay like an active connection. When you pause/stop playing, the ground station will report "Communication Lost" and wait for disconnection or for more messages.

To replay a flight:

1. Disconnect any active connections.
2. Select **File | Replay Flight Data** to toggle the flight replay bar visibility.
    
    ![Toggle Flight Replay](../../assets/app_menu/flight_replay/flight_replay_toggle.jpg)

3. Select the **Replay Flight Data** button in the bar to display a *file selection* dialog. Choose a log file to replay from the available telemetry logs.
    
    ![Flight Replay bar](../../assets/app_menu/flight_replay/flight_replay_playing.jpg)
    
    *QGroundControl* will immediately start playing the log.

4. Use the **pause/reset** button to control playing. When paused you can move the slider to a new position in the log.

5. You can pause the flight and select **Disconnect** to stop replay. At this point you can select an alternative log to replay.

> **Tip** You can inspect the running replay in more detail using the [MAVLink Inspector](../app_menu/mavlink_inspector.md) or [MAVLink Analyzer (Analyze)](../app_menu/mavlink_analyzer.md).