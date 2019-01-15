# Mission Upload/Download failures

Although the protocol for uploading and download Plans (Mission, GeoFence, Rally Points) to a vehicle includes retry logic it can still fail over a communication link which is running at a high loss rate.

You can see the loss rate for your link from the [Settings View > MAVLink](../SettingsView/MAVLink.md) page. Even a loss rate in the high single digits can lead to intermittent failures of the plan protocols. Higher loss rates could leads to 100% failure.

There is also the more remote possibility of either firmware or QGC bugs. To see the details of the back and forth message traffic of the protocol you can turn on [Console Logging](../SettingsView/console_logging.md) for Plan upload/download.