# Aquaponic-System-MCU-Firmware

Just a prototype project I did myself during my Internship which mainly used Arduino IDE and Node-Red, This is My Very first project using Node-Red :)

The aquaponics system Arduino firmware consists of both source code for Arduino Nano board and ESP 8266 board which communicates through serial port

## What you need

1. Arduino JSON Library https://github.com/bblanchon/ArduinoJson.git
2. TDS Sensor Library https://github.com/DFRobot/GravityTDS.git
3. MQTT Pubsub client library https://github.com/knolleary/pubsubclient.git

### What you need to do 

#### ESP 8266

1. Change the credentials at the top of the ESP 8266 Firmware 

~~~

const char* ssid     = "YOUR SSID"; // ESP32 and ESP8266 uses 2.4GHZ wifi only
const char* password = "YOUR PASSWORD"; 
const char* mqttuser     = "YOUR MQTT USERNAME"; // ESP32 and ESP8266 uses 2.4GHZ wifi only
const char* mqttpass = "YOUR MQTT PASSWORD"; 

~~~

2. Once you changed the credentials upload the code into the ESP 8266 board
3. Please ensure that the ESP 8266 board manager is installed on Arduino IDE, otherwise it will not detect ESP 8266 default libraries such as ESP8266WIFI.h
4. Select your ESP 8266 model and upload the firmware and you're good to go!

#### Arduino 

1. For the Arduino side, I use Arduino Nano but Arduino UNO R1 can also be used
2. No need to configure anything just upload as it is since the Arduino only acts as a slave


### How does it work ?

1. The 
