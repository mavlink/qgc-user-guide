# Plan View - Rally Points

Rally Points are alternative landing or loiter locations.

They are typically used to provide a safer or more convenient destination than the home position in RETURN TO LAUNCH (RTL) mode.

![](../../assets/plan/RallyPoints.jpg)

> **Note** Not all vehicle firmwares support Rally Points, and even if supported the Rally Point capabilities vary. Rally Point docs for ArduPilot [can be found here](http://ardupilot.org/copter/docs/common-rally-points.html). PX4 does not support rally points at time of writing (April 2017).

## Rally Point Setup

The steps to creating a GeoFence are:

1. Change to Plan View
2. Select the Rally button (top right of view)
3. Click in the map to add Rally Points

### Rally Points Tools

On the left edge of the screen you will see the Plan Tools. The order of tools from top to bottom is:

* Sync
* Center map
* Map Type
* Zoom In/Out

#### Sync

The Sync tools allows you to move Rally Points back and forth to your Vehicle or a file. *Before you fly you must be sure to send your Rally Points to your vehicle.* The tool will change to have an "!" within it to indicate that you have changes to your GeoFence which you have not sent to your vehicle.

The Sync tool provides the following functionality:

* Send to Vehicle
* Load from Vehicle
* Save to File
* Load from File
* Remove All

#### Remaining tools

The rest of the tools work exactly as they do while editing a Mission.