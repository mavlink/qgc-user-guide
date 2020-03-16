# Daily Build Major Changes

This topic contains a high level and *non-exhaustive* list of new features added to *QGroundControl* since the last [stable release](../releases/release_notes.md). These features are available in [daily builds](../releases/daily_builds.md). There is also a [Change Log](https://github.com/mavlink/qgroundcontrol/blob/master/ChangeLog.md) available for viewing.

* [Pattern Presets](../PlanView/PatternPresets.md) - Allows you to save settings for a Pattern item (Survey, Corridor Scan, ...) into a named preset. You can then use this preset over and over again as you create new Pattern.
* ArduPilot:
  * Copter - PID Tuning support ![PID Tuning JPG](../../assets/daily_build_changes/ArduCopterPIDTuning.jpg) 
  * Copter - Additional Basic Tuning options ![Basic Tuning JPG](../../assets/daily_build_changes/ArduCopterBasicTuning.jpg) 
  * Copter/Rover - Frame setup ui ![Setup Frame Copter JPG](../../assets/daily_build_changes/ArduCopterSetupFrame.jpg)
  * Improved support for flashing ChibiOS firmware
  * Improved support for connecting to ChibiOS bootloader boards
  * Support configurable mavlink stream rates. Available from Settings/Mavlink page. ![Stream Rates JPG](../../assets/daily_build_changes/ArduPilotStreamRates.jpg)
* Optional [CSV Logging](../SettingsView/csv.md) of telemetry data for improved accessibility.
