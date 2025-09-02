# ESP32_MQTT_SERVER_
This project demonstrates how to use the ESP32-S3 Dev Module as an MQTT client to connect to a public MQTT broker and exchange messages with MQTT Explorer

---

```markdown
# ESP32-S3 MQTT Project

This project demonstrates how to use the **ESP32-S3 Dev Module** as an MQTT client to connect to a public MQTT broker and exchange messages with **MQTT Explorer**.

---

## 🔹 Features
- Connects ESP32-S3 to Wi-Fi (2.4 GHz).
- Connects to a public MQTT broker (`broker.hivemq.com` or `test.mosquitto.org`).
- Publishes a message every 5 seconds to the topic:
```

esp32s3/test

```
- Subscribes to the same topic and prints received messages in the **Serial Monitor**.
- Can be extended to control peripherals (e.g., onboard LED) via MQTT commands like `LED ON` / `LED OFF`.

---

## 🔹 Hardware Requirements
- ESP32-S3 Dev Module
- USB-C cable for programming
- Wi-Fi network (2.4 GHz)

---

## 🔹 Software Requirements
- [Arduino IDE](https://www.arduino.cc/en/software)
- ESP32 board package installed via Board Manager  
Add this URL in Arduino IDE → Preferences → Additional Board Manager URLs:
```

[https://espressif.github.io/arduino-esp32/package\_esp32\_index.json](https://espressif.github.io/arduino-esp32/package_esp32_index.json)

````
- Libraries:
- **WiFi.h** (comes with ESP32 package)
- **PubSubClient** (for MQTT)

---

## 🔹 Setup Instructions
1. Clone this repository or copy the code into Arduino IDE.
2. Update Wi-Fi credentials in the code:
 ```cpp
 const char* ssid = "YOUR_WIFI_SSID";
 const char* password = "YOUR_WIFI_PASSWORD";
````

3. Select **ESP32S3 Dev Module** in `Tools → Board`.
4. Upload the sketch to your ESP32-S3.
5. Open **Serial Monitor** (115200 baud) to see connection logs.

---

## 🔹 Testing with MQTT Explorer

1. Install [MQTT Explorer](https://mqtt-explorer.com/).
2. Create a new connection:

   * Host: `broker.hivemq.com`
   * Port: `1883`
   * No username/password
3. Subscribe to the topic:

   ```
   esp32s3/test
   ```
4. You will see messages from ESP32-S3 updating every 5 seconds.
5. Publish messages to the same topic (e.g., `"Hello ESP32"`) and view them in the Arduino Serial Monitor.

---

## 🔹 Example Serial Monitor Output

```
WiFi connected!
IP Address: 192.168.1.50
Connecting to MQTT... connected
Published: Hello from ESP32-S3: 5s
Message received [esp32s3/test]: Hello ESP32
```

---

## 🔹 Future Improvements

* Add LED control (`LED ON` / `LED OFF`) via MQTT commands.
* Connect sensors (temperature, humidity, etc.) and publish readings.
* Secure communication using MQTT over TLS.

---

⚡ With this project, you can use the ESP32-S3 to build **IoT applications** that communicate over MQTT — ideal for home automation, sensor networks, and real-time monitoring.

```

---

✅ This will give your GitHub repo a professional look.  

Do you also want me to add a **folder structure section** (like `src/`, `docs/`, etc.) so it looks even more like a production-ready repo?
```
