# Plan View

![](../../images/plan/PlanView.jpg)

The Plan View is used to plan autonomous missions for you Vehicle. Once the mission is planned and sent to the vehicle, you switch to the [Fly View](../FlyView/FlyView.md) to fly the mission.

If your Vehicle supports a [GeoFence](PlanGeoFence.md) or [Rally Points](PlanRallyPoints.md) you can also set those up from the Plan View.

The image above shows a simple mission which starts with a takeoff, flies through two waypoints and then lands.

The steps to creating a missions are:

1. Change to Plan View
2. Add waypoints to the mission and edit as needed
3. Upload: Send the mission to the vehicle
4. Change to Fly View and fly your mission

## Plan Tools
On the left edge of the screen you will see the Plan Tools. The order of tools from top to bottom is:

* Add waypoints
* [Pattern](Survey.md)  ---------------------> change this name ?
* Sync
* Center map
* Zoom In
* Zoom Out

 > **Note** **Center map**, **Zoom In**, **Zoom Out** are just map visualisation tools that help user view the Plan view map clearly while planning missions. These tools don't affect the mission commands sent to the vehicle in any way.

### Actual vs Planned Home Position
Home position is the position the vehicle will return to and land on when in Return (to Launch/Home) mode. The actual home position is automatically set to the takeoff position by the autopilot during takeoff. This location can be seen in the Fly view once the user is ready to start the mission. The "Planned Home Position", on the other hand, is merely a virtual home position shown in Plan view to help user plan a mission offline while not connected to the vehicle. "Planned Home Position" only has visual significance in QGC such that the QGC is able to draw waypoint lines correctly to the first actual waypoint. However, when the user goes out on the field and starts the mission, the autopilot uses the actual takeoff position as its home position instead of the "Planned Home Position".


### Add Waypoints
Click to activate the Add Waypoints tool. While active, clicking in the map will add new mission waypoint at the clicked location. The tool will stay active until you click it again. Once you have added a waypoint, you can select it by clicking on it and then drag it around to change its position.

### Sync
The Sync tools allows you to move Missions back and forth to your Vehicle or a file. *Before you fly a mission you must be sure to send your Mission to your vehicle.* The tool will change to have an "!" within it to indicate that you have changes to your Mission which you have not sent to your vehicle. 

The Sync tool provides the following functionality:

* Upload (Send to Vehicle)
* Download (Load from Vehicle)
* Save to File
* Load from File
* Remove All (removes all mission waypoints from Plan view and from vehicle)

### Survey

[Survey](Survey.md) allows you to fly a grid pattern over a polygonal area.

## Mission Command List

On the right edge of the display is the list of mission commands for this mission. You can click on one of these to edit the values for the item. Above are a set of options to switch between editing the Mission, GeoFence and Rally Points.

### Mission Command Editors

Click on a mission command to show its editor which allows you to specify the values for the command. You can also change the type of the command by clicking on the command name, "Waypoint" in this example. This allows you to pick from the set up available commands to build your mission. To the right of the command name is a menu you can open by clicking. This menu provides you access to additional options such as Insert and Delete.


## Mission Display

In the center of the map you will see a visualization of your current mission. You can click on the indicators to select them and then you can also drag them around to reposition them.

## Mission Height Display

At the bottom of the map you will see a representation of the height differences between your mission commands.

