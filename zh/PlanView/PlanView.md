# Plan View

The *Plan View* is used to plan autonomous missions for your vehicle, and upload them to the vehicle. Once the mission is [planned](#plan_mission) and sent to the vehicle, you switch to the [Fly View](../FlyView/FlyView.md) to fly the mission.

It is also use to configure the [GeoFence](PlanGeoFence.md) and [Rally Points](PlanRallyPoints.md) if these are supported by the firmware.

<span id="plan_screenshot"></span>
![Plan View](../../assets/plan/PlanView.png)

## UI Overview {#ui_overview}

The [screenshot above](#plan_screenshot) shows a simple mission plan that starts with a takeoff at the [Planned Home](#planned_home) position (H), flies through three waypoints, and then lands on the last waypoint (i.e. waypoint 3).

The main elements of the UI are:

- **Map:** Displays the numbered indicators for the current mission, including the [Planned Home](#planned_home). Click on the indicators to select them (for editing) or drag them around to reposition them. 
- **Plan Toolbar:** Status information for the currently selected waypoint relative to the previous waypoint, as well as statistics for the entire mission (e.g. horizontal distance and time for mission). 
  - `Max telem dist` is the distance between the [Planned Home](#planned_home) and the furthest waypoint. 
  - When connected to a vehicle it also shows an **Upload** button, can be used to upload the plan to the vehicle.
- **[Plan Tools](#plan_tools):** Used to create and manage missions.
- **[Mission Command List/Overlay](#mission_command_list):** Displays the current list of mission items (select items to [edit](#mission_command_editors)).
- **Terrain Altitude Overlay:** Shows the relative altitude of each mission command.

It shows you information related to the currently selected waypoint as well as statistics for the entire mission.

## Planning a Mission {#plan_mission}

At very high level, the steps to create a mission are:

1. Change to *Plan View*.
2. Add waypoints or commands to the mission and edit as needed.
3. Upload the mission to the vehicle.
4. Change to *Fly View* and fly the mission.

The following sections explain some of the details in the view.

## Planned Home Position {#planned_home}

The *Planned Home* shown in *Plan View* is used to set the approximate start point when planning a mission (i.e. when a vehicle may not even be connected to a vehicle). It is used by QGC to estimate mission times and to draw waypoint lines.

![Planned Home Position](../../assets/plan/MissionSettingsPlannedHome.jpg)

You should move/drag the planned home position to roughly the location where you plan to takeoff. The altitude for the planned home position is set in the [Mission Settings](#mission_settings) panel.

<img src="../../assets/plan/MissionSettingsPlannedHomePositionSection.jpg" style="width: 200px;" />

> **Tip** The Fly View displays the *actual* home position set by the vehicle firmware when it arms (this where the vehicle will return in Return/RTL mode).

## Plan Tools {#plan_tools}

The plan tools are used for adding individual waypoints, easing mission creation for complicated geometries, uploading/downloading/saving/restoring missions, and for navigating the map. The main tools are described below.

> **Note** **Center map**, **Zoom In**, **Zoom Out** tools help users better view and navigate the *Plan view* map (they don't affect the mission commands sent to the vehicle).

### Add Waypoints

Click on the **Add Waypoint** tool to activate it. While active, clicking on the map will add new mission waypoint at the clicked location. The tool will stay active until you select it again. Once you have added a waypoint, you can select it and drag it around to change its position.

### Sync

The *Sync tools* are used to move missions between the ground station and vehicle, and to save/restore them from files. The tool displays an `!` to indicate that there are mission changes that you have not sent to the vehicle.

> **Note** Before you fly a mission you must upload it to the vehicle.

The *Sync tools* provides the following functionality:

- Upload (Send to vehicle)
- Download (Load from vehicle)
- Save to File
- Load from File
- Remove All (removes all mission waypoints from *Plan view* and from vehicle)

### Pattern

The [Pattern](Pattern.md) tool simplifies the creation of missions for flying complex geometries, including [surveys](../PlanView/pattern_survey.md) and [structure scans](../PlanView/pattern_structure_scan.md).

## Mission Command List {#mission_command_list}

Mission commands for the current mission are listed on the right side of the view. You can select individual items to edit their values. Above are a set of options to switch between editing the mission, GeoFence and rally points.

![Mission Command List](../../assets/plan/mission_command_list.png)

### Mission Command Editors {#mission_command_editors}

Click on a mission command in the list to display its editor (in which you can set/change the command attributes).

You can change the type of the command by clicking on the command name (for example: "Waypoint"). This will display the *Select Mission Command* dialog shown below. To the right of each command name is a menu that you can click to access to additional options such as *Insert* and *Delete*.

<img src="../../assets/plan/MissionCommands.png" style="width: 200px;" />

The list of commands displayed in the dialog can be filtered by category. For example, to see all commands, choose **All commands** from **Category** drop down menu.

> **Note** The list of available commands will depend on firmware and vehicle type. Examples may include: Waypoint, Start image capture, Jump to item (to repeat mission) and other commands.

### Mission Settings {#mission_settings}

The *Mission Start* panel is the first item that appears in the [mission command list](#mission_command_list). It may be used to specify a number default settings that may affect the start or end of the mission.

![Mission Command List - showing mission settings](../../assets/plan/mission_start.png)

![Mission settings](../../assets/plan/MissionSettings.png)

#### Mission Defaults

##### Waypoint alt

Set the default altitude for the first mission item added to a plan (subsequent items take an initial altitude from the previous item). This can also be used to change the altitude of all items in a plan to the same value; you will be prompted if you change the value when there are items in a plan.

##### Flight speed

Set a flight speed for the mission that is different than the default mission speed.

#### Mission End

##### Return to Launch after mission end

Check this if you want your vehicle to Return/RTL after the final mission item.

#### Planned Home Position

The [Planned Home Position](#planned_home) section allows you to simulate the vehicle's home position while planning a mission. This allows you to view the waypoint trajectory for your vehicle from takeoff to mission completion.

![MissionSettings Planned Home Position Section](../../assets/plan/MissionSettingsPlannedHomePositionSection.jpg)

> **Note** This is only the *planned* home position and you should place it where you plan to start the vehicle from. It has no actual impact on flying the mission. The actual home position of a vehicle is set by the vehicle itself when arming.

The section allows you to set the **Altitude** and **Set Home to Map Centre** (you can move it to another position by dragging it on the map).

#### Camera

The camera section allows you to specify a camera action to take, control the gimbal and set your camera into photo or video mode.

![MissionSettings Camera Section](../../assets/plan/MissionSettingsCameraSection.jpg)

The available camera actions are:

- No change (continue current action)
- Take photos (time)
- Take photos (distance)
- Stop taking photos
- Start recording video
- Stop recording video

#### Vehicle Info

The appropriate mission commands for the vehicle depend on the firmware and vehicle type.

If you are planning a mission while you are *connected to a vehicle* the firmware and vehicle type will be determined from the vehicle. This section allows you to specify the vehicle firmware/type when not connected to a vehicle.

![MissionSettings VehicleInfoSection](../../assets/plan/MissionSettingsVehicleInfoSection.jpg)

The additional value that can be specified when planning a mission is the vehicle flight speed. By specifying this value, total mission or survey times can be approximated even when not connected to a vehicle.

## Further Info

- New Plan View features for [QGC release v3.2](../releases/stable_v3.2_long.md#plan_view)
- New Plan View features for [QGC release v3.3](../releases/stable_v3.3_long.md#plan_view)