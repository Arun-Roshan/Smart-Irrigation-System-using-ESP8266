# Smart Irrigation System using ESP8266 🌱  


## 📖 Project Overview  
This **Smart Irrigation System** automatically waters plants based on soil moisture levels using an **ESP8266 (NodeMCU)**, a **soil moisture sensor**, an **OLED display**, a **buzzer**, and a **relay-controlled water pump**. It helps conserve water and provides automation for home gardens, farms, and indoor plants.

## 🎯 Features  
✔ **Soil Moisture Monitoring** using an analog sensor  
✔ **OLED Display (128x64)** shows moisture level with a **bar animation**  
✔ **Buzzer Alert** when soil is dry  
✔ **Water Pump Control** using a **relay module**  
✔ **Low Power & Cost-Effective**  

## 🛠 Components Required  
1️⃣ **ESP8266 (NodeMCU)**  
2️⃣ **Soil Moisture Sensor** (FC-28 or similar)  
3️⃣ **OLED Display (128x64, SSD1306, I2C)**  
4️⃣ **Buzzer** (Piezo or standard)  
5️⃣ **Relay Module (5V, 1-channel)**  
6️⃣ **Water Pump Motor (DC 5V–12V)**  
7️⃣ **Jumper Wires & Breadboard**  

## ⚡ Circuit Connections  

### **1️⃣ Soil Moisture Sensor → ESP8266**
| Soil Sensor Pin | Connect To (ESP8266) |
|---------------|------------|
| **VCC**      | **3.3V** |
| **GND**      | **GND** |
| **A0**       | **A0** |

### **2️⃣ OLED Display (I2C) → ESP8266**
| OLED Pin | ESP8266 Pin |
|---------|------------|
| **VCC** | **3.3V** |
| **GND** | **GND** |
| **SDA** | **D2 (GPIO4)** |
| **SCL** | **D1 (GPIO5)** |

### **3️⃣ Buzzer → ESP8266**
| Buzzer Pin | ESP8266 Pin |
|------------|------------|
| **+ (VCC)** | **D6 (GPIO12)** |
| **- (GND)** | **GND** |

### **4️⃣ Relay & Water Pump → ESP8266**
| Relay Pin | ESP8266 Pin |
|-----------|------------|
| **VCC**   | **3.3V** |
| **GND**   | **GND** |
| **IN**    | **D7 (GPIO13)** |

**Water Pump Wiring**:  
- **COM (Common)** → Connect to **Pump Negative (-)**  
- **NO (Normally Open)** → Connect to **GND**  
- **Pump Positive (+)** → Connect to **External Power (+5V to 12V)**  

⚠ **Note:** Use an external power supply if the pump requires more than **5V**.

## 💾 Code  
Upload this code to your **ESP8266 (NodeMCU)** using the **Arduino IDE**:  

## 🚀 Getting Started  

### 1️⃣ **Install Required Libraries**  
Open **Arduino IDE**, go to **Sketch → Include Library → Manage Libraries**, and install:  
✔ `Adafruit SSD1306`  
✔ `Adafruit GFX`  

### 2️⃣ **Upload Code**  
1. Connect **ESP8266** to your PC via **USB Cable**  
2. Select **Board: NodeMCU 1.0 (ESP-12E Module)**  
3. Choose **Port** from **Tools → Port**  
4. Click **Upload** ✅  

### 3️⃣ **How It Works**
✔ Reads **soil moisture percentage**  
✔ Displays **moisture level** on **OLED** with a **bar animation**  
✔ **Buzzer alerts** when soil is too dry  
✔ **Water pump turns ON** when moisture is low, then stops after **5 seconds**  

## 🔥 Future Improvements  
🔹 **WiFi Monitoring** (Send data to a web dashboard)  
🔹 **Remote Control** (Turn pump ON/OFF from a mobile app)  
🔹 **Battery/Solar Powered System**  


---

**Made with ❤️ by Arun Roshan** 🚀  
