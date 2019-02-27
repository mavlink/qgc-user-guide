# Fly View

The Fly View is the main view you will use while flying your vehicle. 
You can switch between a map view and a video view (if available).

![Fly View](../../assets/fly/fly_view_overview.jpg)


## Map

The map shows the positions of all connected vehicles and the  mission for the current vehicle.

You can drag the map to move it around (the map automatically recentres after a certain amount of time).

Once flying, you can click on the map to set a GoTo position.


## Fly Tools {#fly_tools}

On the left edge of the screen you will see the *Fly Tools*.
You can use these to takeoff, return, pause, or continue/start an action (e.g. a mission).

The order of tools from top to bottom is:

* Takeoff/Land
* Return To Launch
* Pause
* Action

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