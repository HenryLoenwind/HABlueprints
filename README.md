# Home Assistant Blueprints

## Day Cycle Blueprints

All these blueprints vary a value based on a half-sine wave between sunrise and sunset. You configure a value for sunrise/sunset and one each for the two times right in the middle between sunrise and sunset. The blueprint will the connect those in a nice wave.

Here's an example how this may look:

![image](https://github.com/HenryLoenwind/HABlueprints/assets/1485873/fbdab516-3764-43a7-bbec-c65509c0315c)

Here, an offset is used (-2 h) to shift the wave so that everything happens two hours later. Also, the midday temperature is set to higher than the maximum temperature, which leads to clipping around midday.

Note that the curve is not smooth around sunrise and sunset as it is purely made up from 2 half-sine waves. Also, at the time the real sunrise/sunset happens (i.e. independent of any offset you configure) there's another bump because HA's sun object only reports the *next* sunrise/sunset, not the previous one. If you need smooth curves, there probably is something on HACS that can do that.

### Day Cycle Light Brightness

Makes a light's brightness follow the day cycle

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FHenryLoenwind%2FHABlueprints%2Fmaster%2Fcycle_brightness.yaml)

### Day Cycle Light Colour Temperature (Percent)

Makes a light's colour temperature follow the day cycle (configured in percent of the light's range)

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FHenryLoenwind%2FHABlueprints%2Fraw%2Fmaster%2Fcycle_colour.yaml)

### Day Cycle Light Colour Temperature (Kelvin)

Makes a light's colour temperature follow the day cycle (configured in Kelvin)

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FHenryLoenwind%2FHABlueprints%2Fraw%2Fmaster%2Fcycle_colour_kelvin.yaml)

### Day Cycle Temperature

Makes a climate controller's temperature follow the day cycle

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FHenryLoenwind%2FHABlueprints%2Fraw%2Fmaster%2Fcycle_temp.yaml)

