# Plan View - Mission

![](PlanView.jpg)

The Plan View is used to plan autonomous missions for you Vehicle. Once the mission is planned and sent to the vehicle, you switch to the [Fly View](FlyView.md) to fly the mission.

The image above shows a simple mission which starts with a takeoff, flies through two waypoints and then lands.

The steps to creating a missions are:
1. Change to Plan View
2. Add commands to the mission and edit as needed
3. Send the mission to the vehicle
4. Change to Fly View and fly your mission

### Plan Tools
On the left edge of the screen you will see the Plan Tools. The order of tools from top to bottom is:
* Add Commands
* Sync
* Center map
* Map Type
* Zoom In/Out

##### Add Commands
Click to activate the Add Commands tool. While active, clicking in the map will add new mission commands at the clicked location. The tool will stay active until you click it again.

##### Sync
The Sync tool allows you to send the mission you created to your vehicle and/or read a mission from your vehicle. It also allows you to save mission to/from a file. Before you fly a mission you must be sure to send your mission to your vehicle. The Sync tool will change to have an "!" within it to indicate that you have changes to your mission which you have not sent to your vehicle.

##### Center Map
The Center Map tool allow you to center the map around various points such as home position, vehicle and so forth.

##### Map Type
This tool allows you to change the current map type. Keep in mind that changing the map provider (Bing, Google, ...) is only allowed through Settings.

### Mission Command List
On the right edge of the display is the list of mission commands for this mission. You can click on one of these to edit the values for the item.

You can also change the type of the command by clicking on the command name, "Waypoint" in this example. This allows you to pick from the set up available commands to build your mission.

The currently selected command in the list also has a menu which you can access by clicking the menu on the right. This menu provides you access to additional options such as Insert and Delete.

### Mission Display
In the center of the map you will see a visualization of your current mission. You can click on the inicators to select then and then you can also drag them around to move them.

### Mission Height Display
At the bottom of the map you will see a representation of the height differences between your mission commands. To the left of that is information for the currently selected command relative to the previous command. For example: Distance from previous waypoint.