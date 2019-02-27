# Fly View

The Fly View is the main view you will use while flying your vehicle. 
You can switch between a map view and a video view (if available).

![Fly View](../../assets/fly/fly_view_overview.jpg)


## Map

The map shows the positions of all connected vehicles and the mission for the current vehicle.

You can drag the map to move it around (the map automatically re-centres after a certain amount of time).

Once flying, you can click on the map to set a [Go to](#goto) or [Orbit at](#orbit) location.

## Fly Tools {#fly_tools}

On the left edge of the screen you will see the *Fly Tools*.
You can use these to takeoff, return, pause, or continue/start an action (e.g. a mission).

The default order of tools from top to bottom is:
* Takeoff/Land
* Return To Launch
* Pause
* Action

Additionally a [preflight checklist](#preflight_checklist) may be enabled, which will add a Checklist tool option.

### Pre Flight Checklist {#preflight_checklist}

A preflight checklist tool can be enabled by navigating to [Application Settings > General > Fly View](../SettingsView/General.md) and selecting the **Use preflight checklist** checkbox.

![Pre Flight Checklist](../../assets/fly/pre_flight_checklist.jpg)

Use the checklist to run though standard tests to ensure that the vehicle is configured correctly and it is safe to fly.
Once you have performed each test, click on it in the UI to mark it as complete.  

## Video

At the lower left of the display you will see video output.
*QGroundControl* supports RTP and RTSP video streaming over your vehicles UDP connection. 
It also support directly connected UVC device support. 
More details on QGC Video support can be found on the [Video README](https://github.com/mavlink/qgroundcontrol/blob/master/src/VideoStreaming/README.md).

By clicking on the video you can make it be the main display for the *Fly View*.

## Instrument Panel

To the right is an instrument panel showing you current information on your vehicle. 
By default this displays vehicle telemetry, but you can switch the content using the drop down menu.

The different content is listed below.

### Values (Telemetry)

The values page shows telemetry information.
The displayed information can be configured by clicking on the small gear icon.

![Instrument Page - for values/telemetry](../../assets/fly/instrument_page_values.jpg)


### Camera

The camera page can be used to manually trigger the camera.

![Instrument Page - for Camera](../../assets/fly/instrument_page_camera.jpg)


### Video Stream

This page is used to enable and record video streaming.

![Instrument Page - Video Stream](../../assets/fly/instrument_page_video_stream.jpg)


### Health

This page shows you the health of the systems within your vehicle.
*QGroundControl* will switch to this page automatically if any systems change to unhealthy.

![Instrument Page - Vehicle Health Good](../../assets/fly/instrument_page_health_good.jpg)
![Instrument Page - Vehicle Health Bad](../../assets/fly/instrument_page_health_bad.jpg)


### Vibration

This page shows current vibration levels and clip counts.

![Instrument Page - Vibration Clip](../../assets/fly/instrument_page_vibration.jpg)


## Guided Operations

The vehicle state and movement can controlled from a number of UI elements in the *Fly View*.
Once an operation is requested, *QGroundControl* displays the *Guided bar* at the bottom of the screen.
This can be used confirm (start) or cancel the operation (X).

![Confirmation slider](../../assets/fly/confirmation_slider.jpg)

The available options vary by vehicle and current vehicle state.
Some of the operations are listed below.


### Arm/Disarm/Emergency Stop

### Change Altitude

### Takeoff/Land

### Goto Location {#goto}

After taking off you can specify that you want to fly to a particular location.

1. Click the map where you want the vehicle to move and select **Go to location** on the popup.

  ![Goto or orbit](../../assets/fly/goto_or_orbit.jpg)
  
1. The location will be displayed on the map, along with a confirmation slider.

   ![Goto confirmation](../../assets/fly/goto.jpg)
   
1. When you're ready, drag the slider to start the operation (or click the cross to cancel it).

### Orbit Location {#orbit}

After taking off you can specify that you want to orbit a particular location.

1. Click the map (near the centre of your desired orbit) and select **Orbit at location** on the popup.

  ![Goto or orbit](../../assets/fly/goto_or_orbit.jpg)
  
1. The proposed orbit will be displayed on the map, along with a confirmation sider.

   ![Orbit confirmation](../../assets/fly/orbit.jpg)
   
   - Select and drag the central marker to move the orbit location.
   - Select and drag the dot on the outer circle to change the orbit radius
1. When you're ready, drag the slider to start the operation (or click the cross to cancel it).


### RTL/Return

### Pause

### Resume Mission

<!-- populate from https://docs.qgroundcontrol.com/en/releases/stable_v3.2_long.html#resume-mission -->

