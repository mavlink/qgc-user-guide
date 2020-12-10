# Replay Flight Data

> **Warning** This feature is intended primarily for **autopilot developers**/**vehicle creators**. It is only supported on desktop builds (Windows, Linux, Mac OS).

The *Replay Flight Data* features allows users to replay a telemetry log, enabling review of past or problematic flights. The flight can be started, paused, stopped, restarted etc.

> **Note** *QGroundControl* treats flight replay like an active connection. When you pause/stop playing, the ground station will report "Communication Lost" and wait for disconnection or for more messages.

To replay a flight:
1. Disconnect any active connections.
1. Select **Application Settings > General > Fly View**
1. Check **Show Telemetry Log Replay Status Bar** to toggle the flight replay bar at the bottom of the screen.

   ![Toggle Flight Replay](../../assets/fly/flight_replay/flight_replay_toggle.jpg)
1. Select the **Load Telemetry Log** button in the bar to display a *file selection* dialog.
   - Choose a log file to replay from the available telemetry logs.
   - *QGroundControl* will immediately start playing the log.
1. When a log is loaded you can use the:
   - **Pause/Play** button to pause and restart playing.
   - *Slider* to drag to a new position in the log.
   - *Rate* selector to choose how quickly the log is run.
1. To stop relay (i.e. to load a new file to replay), first pause the flight, and then select **Disconnect** (when it appears). After disconnecting the **Load Telemetry Log** button will be displayed.

> **Tip** You can inspect the running replay in more detail using the [MAVLink Inspector](../analyze_view/mavlink_inspector.md).
