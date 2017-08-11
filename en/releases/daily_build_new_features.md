# Daily Build Major Changes

This topic contains a high level and *non-exhaustive* list of new features added to *QGroundControl* since the last [stable release](../releases/release_notes.md). These features are available in [daily builds](../releases/daily_builds.md).

* Plan: Fixed Wing Landing Pattern: You can now adjust the distance from the loiter to land point by either distance or glide slope fall rate.
* Plan: PX4 GeoFence and Rally Point support.
* Fly: Better display of vehicle icons when connected to multiple vehicles.
* Fly: Multi-Vehicle View supports commands which apply to all vehicles.
* Fly: Displays vehicles reported from ADS-B sensor.

## Detailed Notes

### Plan View

#### New MAVLink GeoFence, Rally Point support

   ![](../../images/plan/GeoFenceRally.jpg)
   
QGC supports the new MAVLink GeoFence and Rally Point specification/protocol. This new system supports multiple polygonal and/or circular fences which can be specified as an exclusion or an inclusion fence.

The fence which is currently selected by the "Edit" radio button will show the on screen editing controls such as the drag points for polygon editing.

Note: Only PX4 Pro firmware supports the new specification. ArduPilot does not yet support the new spec. Support for GeoFence/Rally is temporarily disabled in QGC until QGC ArduPilot code is reworked to the new architecture.

### Fly View

#### Multi-Vehicle vehicle indicators

When you are connected to multiple vehicles the vehicle id will be shown below the vehicle icon. The active vehicle will be opaque and the inactive vehicles will be semi-transparent.

   ![](../../images/fly/MultiVehicleIndicators.jpg)

#### Multi-Vehicle View supports batch commands

The multi-vehicle list now supports commands which apply to all vehicles.

   ![](../../images/fly/MultiVehicleList.jpg)
   
The current list of available commands are Pause and Start Mission but that will be exapanded upon with further development.


#### ADS-B sensor vehicle display

Vehicle reported by ADS-B sensor on vehicle are shown on map as smaller blue icons with altitude and callsign below the icon.

   ![](../../images/fly/ADSBVehicle.jpg)

