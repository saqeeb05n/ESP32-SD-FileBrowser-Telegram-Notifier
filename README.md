# 📂 ESP32 SD File Browser + Telegram IP Notifier

An advanced ESP32 project that combines **SD card file management** with a **web interface** and **Telegram notifications**.  
This project allows you to upload, download, view, and delete files/folders from an SD card connected to an ESP32 board.  
It also supports **dual WiFi credentials, password-protected login, recursive folder deletion, and real-time Telegram IP notifications**.

---

## 🚀 Features
- 🌐 **Dual WiFi** with automatic fallback (WiFiMulti).
- 📲 **Telegram Bot integration** – Sends ESP32 IP address when connected.
- 🔑 **Secure Login** – Password-protected web interface with sessions.
- 📂 **SD File Browser**:
  - View, upload, download, and delete files.
  - Create and delete folders (with recursive delete fix).
  - Displays storage usage (total, used, free).
  - Supports long filenames & emoji rendering.
- 🖥️ **Modern UI** with responsive layout.
- 📑 **File type support** – Proper MIME/content-type handling for most formats (images, docs, audio, video, etc.).

---

## 🛠️ Hardware Setup
**Connections (SPI mode):**
ESP32 -> SD Card

CS -> 5
MOSI -> 23
MISO -> 19
SCK -> 18


---

## 📦 Libraries Required
Make sure you have these installed in the Arduino IDE / PlatformIO:
- `WiFi.h`
- `WiFiMulti.h`
- `WiFiClientSecure.h`
- `WebServer.h`
- `SPI.h`
- `SD.h`

---

## ⚙️ Configuration
Edit the following in the code before uploading:


// WiFi credentials
const char* WIFI_SSID_1 = "YourWiFi1";
const char* WIFI_PASS_1 = "password1";
const char* WIFI_SSID_2 = "YourWiFi2";   // optional
const char* WIFI_PASS_2 = "password2";

// Telegram Bot credentials
const char* BOT_TOKEN = "your_bot_token";
const char* CHAT_ID   = "your_chat_id";

// Web login
const char* HTTP_USER = "admin";
const char* HTTP_PASS = "esp32pass";
