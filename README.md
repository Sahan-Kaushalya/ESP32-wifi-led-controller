# ESP32 WiFi Dual LED Controller

A simple HTTP web server built with ESP32 to control two LEDs (Red and Green) using HTTP GET requests.

## 🚀 Features
- Status indication during WiFi connection (Blinking Red LED).
- Green LED turns ON once connected to WiFi.
- HTTP API Endpoints to toggle individual or both LEDs.

## 🛠️ Hardware Required
- ESP32 Development Board
- 1x Red LED
- 1x Green LED
- 2x 220Ω Resistors
- Breadboard & Jumper Wires

## 📌 Circuit Pinout
| Component | ESP32 Pin |
| :--- | :--- |
| **Red LED** | GPIO 12 |
| **Green LED** | GPIO 14 |

## 🌐 API Endpoints

Once connected, find the IP address from the Serial Monitor (e.g., `192.168.1.50`) and send HTTP requests:

| Endpoint | Action |
| :--- | :--- |
| `http://<ESP32_IP>/on` | Green LED **ON**, Red LED **OFF** |
| `http://<ESP32_IP>/off` | Green LED **OFF**, Red LED **ON** |
| `http://<ESP32_IP>/on/both` | Both LEDs **ON** |
| `http://<ESP32_IP>/off/both` | Both LEDs **OFF** |

## 💻 Getting Started
1. Clone this repository.
2. Open the `.ino` sketch in Arduino IDE.
3. Select your ESP32 board (`Tools > Board > ESP32 Dev Module`).
4. Update `SSID` and `PASSWORD` with your WiFi credentials.
5. Upload the code and open Serial Monitor at `115200` baud rate.
