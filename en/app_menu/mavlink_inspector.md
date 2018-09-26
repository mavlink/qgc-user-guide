# MAVLink Inspector Widget

> **Warning** This feature is intended primarily for **autopilot developers**/**vehicle creators**. 
  It is only supported on desktop builds (Windows, Linux, Mac OS).

The *MAVLink Inspector* widget provides information about MAVLink traffic received by *QGroundControl*.
For every vehicle it lists all received messages (including their update frequency and command number).
You can drill down into any vehicle message to see the content of the last received message.

<!-- ![MAVLink inspector](../../assets/app_menu/mavlink_inspector/mavlink_inspector.jpg) -->

To use the *MAVLink Inspector*:
1. Select **Widgets | MAVLink Inspector** on any screen.

   ![MAVLink inspector menu](../../assets/app_menu/mavlink_inspector/mavlink_inspector_menu.jpg)

   The widget will open displaying all vehicles (for which messages have been received).

   ![MAVLink inspector vehicle](../../assets/app_menu/mavlink_inspector/mavlink_inspector_vehicle.jpg)

1. Expand the vehicle toggle to see its messages. 
   
   ![MAVLink inspector](../../assets/app_menu/mavlink_inspector/mavlink_inspector_message.jpg)
1. Expand a message to see its latest (dynamically updating) value:

   ![MAVLink inspector](../../assets/app_menu/mavlink_inspector/mavlink_inspector_message_details.jpg)
1. You can reset the view by pressing the **Clear** button. 
   The widget will repopulate from new messages.
