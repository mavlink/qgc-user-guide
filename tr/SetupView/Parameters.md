# Parametreler

*Parametreler* ekranı, araçla ilişkili parametrelerden herhangi birini bulmanıza ve düzenlemenizi sağlar.

![Parameters Screen](../../assets/setup/parameters_px4.jpg)

> **Note** PX4 Pro ve ArduPilot farklı parametre setleri kullanır, ancak her ikisi de bu bölümde açıklandığı gibi yönetilir.

## Bir Parametreyi Bulma

Parametreler gruplar halinde düzenlenmiştir. Soldaki butonlara tıklayarak görüntülemek için bir parametre grubu seçin (yukarıdaki görüntüde * Pil Kalibrasyonu * grubu seçilir).

Ayrıca * Search* alanına bir terim girerek bir parametre için * arama * yapabilirsiniz. This will show you a list of all parameter names and descriptions that contain the entered substring (press **Clear** to reset the search).

![Parameters Search](../../assets/setup/parameters_search.jpg)

## Changing a Parameter

To change the value of a parameter click on the parameter row in a group or search list. This will open a side dialog in which you can update the value (this dialog also provides additional detailed information about the parameter - including whether a reboot is required for the change to take effect).

![Changing a parameter value](../../assets/setup/parameters_changing.png)

> **Note** When you click **Save** the parameter is automatically and silently uploaded to the connected vehicle. Depending on the parameter, you may then need to reboot the flight controller for the change to take effect.

## Tools

You can select additional options from the **Tools** menu on the top right hand side of the screen.

![Tools menu](../../assets/setup/parameters_tools_menu.png)

**Refresh** <br />Refresh the parameter values by re-requesting all of them from the vehicle.

**Reset all to defaults** <br />Reset all parameters to their original default values.

**Load from file / Save to file** <br />Load parameters from an existing file or save your current parameter settings to a file.

**Clear RC to Param** <br />This clears all associations between RC transmitter controls and parameters. For more information see: [Radio Setup > Param Tuning Channels](../SetupView/Radio.md#param-tuning-channels-px4).

**Reboot Vehicle** <br />Reboot the vehicle (required after changing some parameters).