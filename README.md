# esp32_cleargrass_gateway
Build a esp32 wifi gateway that collects cleargrass thermometer data

This is a gateway that uses an esp32 for collecting bluetooth data of the cleargrass e-ink thermometer (https://qingping.co/cg_temp_rh_monitor/overview). The collected data can be retrieved via a wifi webinterface as json data structure which makes the integration to other systems (smarthome / etc.) quite simple.


# example
The ESP32 automatically collects the bluetooth messages sent by the ClearGrass Thermometer(s).

Following data is captured:<br>
- Mac address<br>
- Temperature<br>
- Humidity<br>
- Battery Level<br>
- Temperature Date<br>
- Humidity Date<br>
- Battery Level Date<br><br>

The last 3 values contain a timestamp indicating the date and time when the last update for the corresponding value was retrieved.
<br><br>
There are 2 Webinterface URLs:<br>
ip_of_esp_32 => show the main webinterface<br>
![Alt text](webinterface_main.JPG?raw=true "Webinterface Main")
<br><br>
ip_of_esp_32/json => get the collected data as json structure<br>
![Alt text](webinterface_json.JPG?raw=true "Webinterface Json")

# installation
- Just take a ESP32 microprocessor (https://en.wikipedia.org/wiki/ESP32) and deploy the code to the device. Don't forget to change your wifi credentials first!

# notes
- Parts of the code are taken from this great project: http://educ8s.tv/esp32-xiaomi-hack/ Check it out!<br>
- The code for sure is not perfect, feel free to share your ideas and improvements<br>
