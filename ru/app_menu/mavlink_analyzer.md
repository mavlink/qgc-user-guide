# MAVLink Analyzer Widget (Analyze)

> **Предупреждение** Эта функция предназначена главным образом для **разработчиков**. Она поддерживается только в операционных системах:Windows, Linux, Mac OS. Обратите внимание, что это отличается от [Экрана Анализ](../analyze_view/README.md).

The *MAVLink Analyzer* widget can be used to show *trend* information for MAVLink traffic received by *QGroundControl*.

For every vehicle it lists all the fields for every received MAVLink message. You can select any set of fields to graph them (using their associated checkbox) and see the trend by time.

To use the *MAVLink Analyzer*:

1. Select **Widgets | Analyze** on any screen.
    
    ![Analyze menu](../../assets/app_menu/mavlink_analyzer/analyze_menu.jpg)
    
    The widget will open displaying all message fields on left, and a graph on the right.
    
    ![MAVLink Analyzer](../../assets/app_menu/mavlink_analyzer/analyze_plot.jpg)

2. Toggle the checkbox to the left of each field to display/hide it on the dynamic plot.

3. Expand the left pane to show values, means and variances.
    
    ![Analyze table](../../assets/app_menu/mavlink_analyzer/analyze_table.jpg)
    
    The **Short names** and **Show units** checkboxes can be used to modify information in the table.