

# 💧 Water Calculation using Flow Sensor with ESP8266

This project measures **water flow rate and total water usage** using a **flow sensor** and an **ESP8266** microcontroller. It displays readings on a small OLED screen and also uploads data to the **ThingSpeak cloud** for remote visualization. ([GitHub][1])

---

## 📌 Overview

The aim of this project is to:

* Accurately measure water flow rate in a pipe.
* Calculate total water consumed over time.
* Display readings live on an OLED display.
* Push data to the internet (ThingSpeak) for remote monitoring. ([GitHub][1])

---

## 📦 Components

You’ll need the following hardware:

* **NodeMCU ESP8266** — Wi-Fi enabled microcontroller
* **YF-S201 Flow Sensor** — Measures flow rate (typically 1–30 L/min)
* **0.96″ I2C OLED Display** — Shows real-time readings
* Breadboard & jumper wires for connections ([GitHub][1])

---

## 🔌 Wiring Connections

Connect the hardware as follows:

| Component                   | Pin on ESP8266 |               |
| --------------------------- | -------------- | ------------- |
| Flow Sensor Red (VCC)       | 3.3V (VIN)     |               |
| Flow Sensor Black (GND)     | GND            |               |
| Flow Sensor Yellow (Signal) | D2 (GPIO4)     |               |
| OLED VCC                    | 3.3V (VIN)     |               |
| OLED GND                    | GND            |               |
| OLED SDA                    | D1 (GPIO5)     |               |
| OLED SCL                    | D2 (GPIO4)     | ([GitHub][1]) |

*(Adjust the pins if needed based on your board/layout.)*

---

## 🛠 Software Setup

1. **Install Arduino IDE**
   Download and install the Arduino IDE (or VS Code with PlatformIO) if not already installed.

2. **Add ESP8266 Board Support**

   * In Arduino IDE → *File → Preferences → Additional Boards Manager URLs*
   * Add: `http://arduino.esp8266.com/stable/package_esp8266com_index.json`
   * Then install **ESP8266** from Boards Manager.

3. **Install Required Libraries**
   Make sure you include libraries for:

   * `ESP8266WiFi.h`
   * `Adafruit_SSD1306.h` / `Adafruit_GFX.h` *(for OLED)*
   * ThingSpeak library *(if uploading data)*

4. **Edit Code Settings**

   * **Wi-Fi SSID & password**
   * **ThingSpeak API Key** (for cloud upload)
   * Set correct pins for display & sensor.

   *(These are typically at the top of the sketch in `Arduino_code`.)* ([GitHub][1])

---

## 🚀 How It Works

* The **flow sensor** emits electrical pulses as water flows through it.
* The **ESP8266** counts these pulses to calculate **flow rate** and **total volume**.
* The OLED display shows values in real time.
* Data can be sent periodically to **ThingSpeak** for online charts and logging.

📊 Typical formula for flow rate based on pulse count will be included in the Arduino sketch.

---

## 🖥 ThingSpeak Cloud Integration

To visualize data online:

1. Create a ThingSpeak channel.
2. Copy the Write API Key.
3. Paste the key into your sketch variable.
4. Upload the sketch to the ESP8266.
5. View live flow/volume data on ThingSpeak dashboard.

This enables anywhere access to water usage trends.

---

## 📸 Example Output

An example output snapshot (`Output.jpeg`) shows how readings appear on the OLED or in the serial monitor. ([GitHub][1])

---

## 🧩 Potential Enhancements

* Add **Blynk** or **MQTT** dashboard support.
* Store data on **local SD card**.
* Implement **flow alerts** when usage exceeds a threshold.
* Add **calibration** feature for more accurate measurements.



If you’d like, I can also **generate badges** (build, license, cloud status) and **a complete wiring diagram** for this project!

[1]: https://github.com/georgepaul7/Water-Calculation-using-Flow-sensor-with-ESP8266 "GitHub - georgepaul7/Water-Calculation-using-Flow-sensor-with-ESP8266"
