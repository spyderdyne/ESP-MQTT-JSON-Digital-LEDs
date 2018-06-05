# ESP MQTT JSON Digital LEDs

This is my version of the NodeMCU LED strip controller, based on bruhAutomation's [project](https://github.com/bruhautomation/ESP-MQTT-JSON-Digital-LEDs), with my own modifications, including:

- Ability to control mutliple strips at once using grouped MQTT topics
- A fix for flickering issues with faster chipsets (FastLED interrupt issue)
- Additional effects written by me (Christmas tree, Sine Wave, Random Stars)
- Making the entire project "production-quality" using a [printed circuit board](https://www.pcbway.com/project/shareproject/NodeMCU_DHT_Sensor_LED_Controller_Breakout_Board_v_1_1.html) to hold the components/wiring together and a [3d printed enclosure](https://www.thingiverse.com/thing:2690563) to make the controller look professional installed around the home.
- Focusing on [openHAB](https://www.openhab.org) as the home automation control suite, since it is what I use.

#### Supported Features Include
- RGB Color Selection
- Brightness 
- Flash
- Fade
- Transitions
- Effects with Animation Speed
- Over-the-Air (OTA) Upload from the ArduinoIDE!

Some of the effects incorporate the currrently selected color (sinelon, confetti, juggle, etc) while other effects use pre-defined colors. You can also select custom transition speeds between colors. The transition variable also functions to control the animation speed of the currently running animation. 

The default speed for the effects is hard coded and is set when the light is first turned on. When changing between effects, the previously used transition speed will take over. If the effects don't look great, play around with the slider to adjust the transition speed (AKA the effect's animation speed). 

#### OTA Uploading
This code also supports remote uploading to the ESP8266 using Arduino's OTA library. To utilize this, you'll need to first upload the sketch using the traditional USB method. However, if you need to update your code after that, your WIFI-connected ESP chip should show up as an option under Tools -> Port -> Porch at your.ip.address.xxx. More information on OTA uploading can be found [here](http://esp8266.github.io/Arduino/versions/2.0.0/doc/ota_updates/ota_updates.html). Note: You cannot access the serial monitor over WIFI at this point.  


#### Demo/Hardware Build Video
[![Demo Video](https://img.youtube.com/vi/WNp4G49tkrQ/0.jpg)](https://youtu.be/WNp4G49tkrQ)

#### Arduino IDE Setup video
[![Tutorial Video](http://img.youtube.com/vi/7dm9OPTRvUQ/0.jpg)](https://youtu.be/7dm9OPTRvUQ)
#### openHAB Configuration Video
[![openHAB Video](https://img.youtube.com/vi/Lnv-2xBhabo/0.jpg)](https://youtu.be/Lnv-2xBhabo)

#### Parts List
- [Digital RGB WS2812 LED Strip](http://amzn.to/2ilIvdf)
- [NodeMCU](http://amzn.to/2hd6RJk)
- [Aluminum Mounting Channel/Diffuser](https://amzn.to/2LoGSI5)
- [Breakout PCB](https://www.pcbway.com/project/shareproject/NodeMCU_DHT_Sensor_LED_Controller_Breakout_Board_v_1_1.html)
- [5V 15amp Power Supply](https://amzn.to/2xHRArn)

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5MDQ0MDk2NzFdfQ==
-->