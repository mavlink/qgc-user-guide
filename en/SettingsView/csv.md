# CSV Logging

> **Note** This is a daily build feature (not present in QGC v3.5)

![Csv checkbox](../../assets/settings/general/csv.jpg)

When checked, a CSV (comma-separated value) telemetry file will be created along with the usual .tlog telemetry file.
The file is only created if Save log after each flight is enabled, and is recorded for the same duration.

This CSV file contains the most relevant vehicle telemetry data available for quick analysis such as GPS position, attitude, battery status, and others.
It is populated at 1 Hz and while it is not as detailed as the telemetry log, it is a lot easier to work with and quicker to extract data out of.

The file should be easily opened by any spreadsheets software such as Microsoft Excel, Google Sheets, LibreOffice Calc or OpenOffice Calc.