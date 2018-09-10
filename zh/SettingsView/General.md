# General Settings (Settings View)

The general settings (**SettingsView > General Settings**) are the main place for application-level configuration. Settable values include: display units, autoconnection devices, video display and storage, RTK GPS, brand image, and other miscellaneous settings.

> **Note** Values are settable even if no vehicle is connected. Settings that require a vehicle restart are indicated in the UI.

![SettingsView - Full General Tab](../../assets/settings/settings_view_general.jpg)

## Units

This section defines the display units used in the application.

![Units settings](../../assets/settings/settings_view_general_units.jpg)

The settings are:

- **Distance**: Meters | Feet
- **Area**: SquareMetres | SquareFeet | SquareKilometers | Hectares | Acres |SquareMiles
- **Speed**: Metres/second | Feet/second | Miles/hour | Kilometres/hour | Knots
- **Temperature**: Celsius | Fahrenheit

## Miscellaneous

This section defines a number of miscellaneous settings, related to (non exhaustively): font sizes, colour schemes, map providers, map types, telemetry logging, audio output, low battery announcement levels, default mission altitude, [virtual joysticks](../SettingsView/VirtualJoystick.md), mission autoloading, default application file load/save path etc.

![Miscellaneous settings](../../assets/settings/settings_view_general_miscellaneous.jpg)

The settings are:

- <span id="colour_scheme"></span>**Color Scheme**: Indoor (Dark) | Outdoor (Light)
- **Map Provider**: Bing | Google | Statkart | Eniro
- **Map Type**: Hybrid | Street | Satellite
- **Stream GCS Position**: Never | Always | When in Follow Me flight mode.
- **Font Size**: Font size across app (Requires restart)
- **Mute all audio output**: Turns off all audio output. 
- <span id="autosave_log"></span>**Save telemetry log after each flight**: Logs automatically saved to the *File Save Path* ([below](#file_save_path)) after flight. 
- **Save telemetry log even if vehicle was not armed**: Logs when a vehicle connects to *QGroundControl*. Stops logging when the last vehicle disconnects.
- **Use preflight checklist**: Enable pre-flight checklist.
- **Virtual Joystick**: Enable [virtual joysticks](../SettingsView/VirtualJoystick.md) (PX4 only)
- <span id="autoload_missions"></span> **Autoload Missions**: If enabled, automatically upload a plan to the vehicle on connection. 
  - The plan file must be named **AutoLoad#.plan**, where the `#` is replaced with the vehicle id. 
  - The plan file must be located in the [Application Load/Save Path(#load_save_path).
- **Clear all settings on next start**: Resets all settings to the default (including this one) when *QGroundControl* restarts.
- **Announce battery lower than**: Specify battery level at which *QGroundControl* will start low battery announcements.
- **Default Mission Altitude**: The default altitude used for the first waypoint (subsequent new waypoints are seeded with the altitude value of the preceding waypoint).
- <span id="load_save_path"></span>**Application Load/Save Path**: Default location for loading/saving application files, including: parameters, telemetry logs, and mission plans.

## RTK GPS

This section specifies the RTK GPS "Survey-in" settings.

![RTK GPS Settings](../../assets/settings/settings_view_general_rtk_gps.jpg)

> **Note** The *Survey-In* process is a startup procedure required by RTK GPS systems to get an accurate estimate of the base station position. The process takes measurements over time, leading to increasing position accuracy. Both of the setting conditions must met for the Survey-in process to complete. For more information see [RTK GPS](https://docs.px4.io/en/advanced_features/rtk-gps.html) (PX4 docs) and [GPS- How it works](http://ardupilot.org/copter/docs/common-gps-how-it-works.html#rtk-corrections) (ArduPilot docs).

The settings are:

- **Survey-in accuracy:** The minimum position accuracy for the RTK Survey-in process to complete.
- **Minimum observation duration:** The minimum time that will be taken for the RTK Survey-in process. 

## AutoConnect to the following devices {#auto_connect}

This section defines the set of devices to which *QGroundControl* will auto-connect.

![Device autoconnect settings](../../assets/settings/settings_view_general_autoconnect_devices.jpg)

Settings include:

- **Pixhawk**: Autoconnect to Pixhawk-series device
- **SiK Radio**: Autoconnect to SiK (Telemetry) radio
- **PX4 Flow**: Autoconnect to PX4Flow device
- **Libre Pilot**: Autoconnect to Libre Pilot autopilot
- **UDP**: Autoconnect to UDP
- **RTK GPS**: Autoconnect to RTK GPS device
- **NMEA GPS Device / Baudrate**: If detected, GPS information will be used for ground station location and follow me support.

## Video {#video}

The *Video* section is used to define the source and connection settings for video that will be displayed in *Fly View*.

![Video settings](../../assets/settings/settings_view_general_video_udp.jpg)

> **Note** The values displayed in this setting depend on the video source. If no video source is specified then no other video or *video recording* settings will be displayed (above we see the settings when UDP source is selected).

## Video Recording

The *Video Recording* section is used to specify the file format and maximum allocated file storage for storing video. Videos are saved to a sub-directory ("Video") of the [Application Load/Save Path](#load_save_path).

![Video - without auto deletion](../../assets/settings/settings_view_general_video_recording.jpg)

![Video - auto deletion](../../assets/settings/settings_view_general_video_recording_auto_delete.jpg)

The settings are:

- **Auto-delete Files**: If checked, files are auto deleted when the specified amount of storage is used.
- **Max Storage Usage**: Maximum video file storage before video files are auto deleted.
- **Video file format**: File format for the saved video recording.

## Brand Image

This setting specifies the *brand image* used for indoor/outdoor colour schemes.

The brand image is displayed in place of the icon for the connected autopilot in the top right corner of the toolbar. It is provided so that users can easily create screen/video captures that include a company logo/branding.

![Brand Image](../../assets/settings/settings_view_general_brand_image.jpg)

The settings are:

- **Indoor Image**: Brand image used in [indoor color scheme](#colour_scheme)
- **Outdoor Image**: Brand image used in [outdoor color scheme](#colour_scheme)
- **Reset Default Brand Image**: Reset the brand image back to default.