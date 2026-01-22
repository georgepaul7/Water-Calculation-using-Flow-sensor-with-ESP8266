1.	Project Name
Title: Water Calculation using Flow Sensor.
Course: IoT Mini Project (CSA3005).
2.	Goal of the Project
To measure water flow rate and total water usage accurately.
To show the data on a small screen attached to the device.
To send the data to the internet (ThingSpeak cloud) so you can see graphs of water usage from anywhere.
3.	Hardware Parts You Need
Node MCU ESP8266: The main Wi-Fi board.
YF-S201 Water Flow Sensor: Measures the water flow (1-30 Liters/minute).
0.96" I2C OLED Display: A small screen to show numbers.
Breadboard & Jumper Wires: To connect everything without soldering.
Software You Need
Arduino IDE: To write and upload the code.
ThingSpeak: The website used to view the data charts online.
4.	Wiring Connections (How to Connect)
Sensor Red Wire: Connect to 3.3V Power (VIN).
Sensor Black Wire: Connect to Ground (GND).
Sensor Yellow Wire: Connect to Pin D2.
OLED Display VCC: Connect to 3.3V Power (VIN).
OLED Display GND: Connect to Ground (GND).
OLED Display SDA: Connect to Pin D2.
5.	Code Settings
Wi-Fi Name (SSID): Change this in the code to "Alexahome" (or your own Wi-Fi name).
Wi-Fi Password: Change this in the code to "loranthus" (or your own password).
API Key: The code uses the key KBD1JSZTUKCXJ15V to talk to ThingSpeak.

