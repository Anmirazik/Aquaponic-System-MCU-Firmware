# Aquaponic-System-MCU-Firmware

This project consist of two branches , the main branches which is the firmware and the node-red branch 

Just a prototype project I did myself during my Internship which mainly used Arduino IDE and Node-Red, This is My Very first project using Node-Red :)

The aquaponics system Arduino firmware consists of both source code for Arduino Nano board and ESP 8266 board which communicates through serial port




## Project Demo & Picture 

This is the Final Product and how it looks, btw I'm not the one in charge of the structural design , another person is in charge of the structural design  

I was only involved with the design of the system functionality :) 

Great project to be involved in, I'm grateful to be a part of the team 

![WhatsApp Image 2023-11-30 at 00 29 42_d5e561bf](https://github.com/Anmirazik/Aquaponic-System-MCU-Firmware/assets/113960675/2e702fb3-cb3b-4902-8d7b-9184047a7f92)

This is how the circuit within the control panel looks like, incomplete version btw 

I lost the picture for the complete version, will update if I find the final picture!

![WhatsApp Image 2023-11-30 at 00 29 42_eae80a6c](https://github.com/Anmirazik/Aquaponic-System-MCU-Firmware/assets/113960675/d57b731c-68dc-4d40-baf9-f292b4773ddf)

Our Node-red Prototype dashboard 

<img width="955" alt="image" src="https://github.com/Anmirazik/Aquaponic-System-MCU-Firmware/assets/113960675/862a96ad-d4c9-40ca-ae53-978b17de76cc">

## What you need

1. Arduino JSON Library https://github.com/bblanchon/ArduinoJson.git
2. TDS Sensor Library https://github.com/DFRobot/GravityTDS.git
3. MQTT Pubsub client library https://github.com/knolleary/pubsubclient.git

### What you need to do 

#### ESP 8266

1. Change the credentials at the top of the ESP 8266 Firmware 

~~~
const char* ssid     = "YOUR SSID"; // ESP32 and ESP8266 uses 2.4GHZ wifi only
const char* password = "YOUR PASSWORD"; //Your WI-FI Password
const char* mqttuser = "YOUR MQTT USERNAME"; // ESP32 and ESP8266 uses 2.4GHZ wifi only
const char* mqttpass = "YOUR MQTT PASSWORD"; //Your MQTT Password
~~~

2. Once you changed the credentials upload the code into the ESP 8266 board
3. Please ensure that the ESP 8266 board manager is installed on Arduino IDE, otherwise it will not detect ESP 8266 default libraries such as ESP8266WIFI.h
4. Select your ESP 8266 model and upload the firmware and you're good to go!

#### Arduino 

1. For the Arduino side, I use Arduino Nano but Arduino UNO R1 can also be used
2. No need to configure anything just upload as it is since the Arduino only acts as a slave


### How does it work ?

1. Arduino acts as a slave and ESP 8266 acts as a master
2. The Arduino (Slave) reads and writes the incoming and outgoing data from ESP 8266 (Master)
3. The Arduino communicates with ESP 8266 through Serial Port 0


