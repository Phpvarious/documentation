# Changelog plugin powerFlow

>**IMPORTANT**
>
>As a reminder, if there is no information on the update, it is because it concerns only the updating of documentation, translation or text.

# 24/06/2025

### Improvement

  - added a trim to remove spaces in units, which allows to continue to escape the core unit conversion for the original command while maintaining compatibility for the plugin.

# 18/06/2025

### Bugfix

Added uid for multiple use in a scenario..

# 17/06/2025

### Improvement

  - It is now possible to change category colors using a new command (Color Change) available in the plugin; this will modify the configured color.<br>
  If the widget is displayed, it will modify the colors sent directly (in JavaScript) without needing to refresh it.<br>

  >**IMPORTANT**
  >
  > If you use this new command multiple times in a scenario, please insert a sleep between each execution.

### Bugfix

  - Décimales sur les persos.

# 14/06/2025

### Improvement

  - Ability to add empty spaces in loads and Pvs.<br>Simply add an item (Activate) without power command.

  ### Bugfix

  - Decimals on daily buy and daily sell of the grid.
  - Default unit in calculations (load and solar)

# 13/06/2025

### Bugfix

  - Alert on receivers on initialization.

# 12/06/2025

### Improvement

- Now all the "power" have :
  - Max : allows the management of gauges.
  - Alert : allows the management of alerts based on power.

- Possibility of duplicating equipment.

### Bugfix

  - Unit of "daily" receivers (kWh which converts to Wh).

# 11/06/2025

### Improvement

- Dead Link Control (deadCmd) visible from the page Analysis > Equipments > Orphan commands.

- Using a variable in all "Max" fields (Use the button to search for a variable).

- Ability to disable unit conversions.

- Choice of the number of decimal places after the decimal point.

# 09/06/2025

### Improvement

- All "power" commands are automatically converted to W to simplify calculations and avoid unit errors.
- All "power" uses a unit conversion (identical to the core).<br><i>eg : 1000 W -> will display 1 kW.</i>
- Possibility to reorganize the "custom" (Sortable).

### Bugfix

- The color of the "total power" now follows the color set in the plugin (Color if value = 0 or Hide if value = 0)<br>
<i>(Unless you use the instantaneous total power command)</i>
- Added a "min" of 7px for text sizes in "customs".

# 03/06/2025

- Official presentation.