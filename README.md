# Convert your Freshdew/JOWSET AP302 Air Purifier to ESPHome

Convert your [Freshdew/JOWSET AP302 Air Purifier](https://www.amazon.com/dp/B0C52YV63X) to ESPHome

## Prerequisites

* ESP12F module -- I used one from a Wemos D1 Mini after programming
* Programmer for ESP12F -- Optional if you program it on Wemos D1 Mini first
* Soldering/Desoldering skills
* (Optional) Hot air gun/hot air rework station
* 10k ohm resistor

## Instructions

Flash your ESP12F module using a programmer with ESPHome using the config included in this repo. In my case, I simply flashed a Wemos D1 mini and then desoldered the ESP12F off of the board

!! IMPORTANT !!
Flash your ESP12F module first and confirm that you can access it in Home Assistant or IP address before soldering it into place

Disassemble the air purifier first by gently prying off the grey cap

![Assembled Freshdew air purifier](https://github.com/matthewbadeau/airpurifier-ap302-esphome/assets/641764/4dfcdbc7-73d3-4049-8867-6fa19301ed85)

Remove the 4 screws and gently lift the interface assembly off of the top being careful not to tug too hard on the wires.

![Cap pried off](https://github.com/matthewbadeau/airpurifier-ap302-esphome/assets/641764/949314e5-3e1e-4c4d-aef6-bee73eb8a684)

Remove the 3 wires taking note of their positions

![Internal PCB](https://github.com/matthewbadeau/airpurifier-ap302-esphome/assets/641764/ec1ca80a-98ae-4503-81d6-503c83ed3d64)

Desolder the WBR3 module using [this Blakadder guide](https://blakadder.com/replace-tuya-esp12/)

![Desoldered module](https://github.com/matthewbadeau/airpurifier-ap302-esphome/assets/641764/1a79babc-6228-47a4-b3a6-b400da80439f)

Solder the ESP12F module into place and solder a 10K ohm resistor between pins GPIO15 and GND

![ESP12F module soldered into place](https://github.com/matthewbadeau/airpurifier-ap302-esphome/assets/641764/a5aaffe6-887f-4942-b2c9-6768aa5b4bb1)

Reassemble!

Remember to test everything works before putting the screws back into place!


## In home assistant

![Home Assistant screenshot](https://github.com/matthewbadeau/airpurifier-ap302-esphome/assets/641764/7a46ccda-8a50-4dde-91c3-54416ecde9ac)
