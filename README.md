# 🍓 StrawberryWatchOS

> `StrawberryOS != (WatchOS || Money)`  
> `StrawberryOS = (Helping && Brotherhood && OpenSource)`

An open-source smartwatch operating system built on ESP32, designed to be hackable, extensible, and free for everyone.

---

## 🧠 What is StrawberryWatchOS?

StrawberryWatchOS is a full smartwatch OS built from scratch for the XIAO ESP32-C6, running on a 0.96" SSD1306 OLED display. It is part of the broader **Strawberry ecosystem** — an open-source platform for embedded devices.

This is not a commercial product. It is a platform — built so that hobbyists, engineers, and makers are never bottlenecked by budget, time, or closed ecosystems.

---

## ⚙️ Hardware

| Component | Details |
|---|---|
| MCU | Seeed XIAO ESP32-C6 (RISC-V 160MHz, WiFi 6, BLE 5.3) |
| Display | 0.96" SSD1306 OLED (128×64) |
| RTC | DS3231 |
| Battery | 1500mAh LiPo |
| Buttons | 5× tactile (UP, DOWN, LEFT, RIGHT, CENTER) |
| PCB | Custom 6-layer ENIG |
| Enclosure | 52×32mm ASA |

> Dev board: ESP32-C3 SuperMini (pin-compatible for development)

---

## ✨ Features

### Currently Implemented
- ⌚ Watch face with real-time clock (DS3231 RTC)
- 📅 Date and day of week display
- ⏱️ Stopwatch (MM:SS:ms)
- ⏲️ Countdown Timer with alert
- 📡 Radio app (WiFi, BLE, ESP-NOW stubs)
- 🌐 WiFi scanning, credential saving (up to 5 networks)
- 🕐 NTP time sync over WiFi
- 🔋 Display timeout + power management
- 🎞️ Smooth slide animations between screens
- ⌨️ On-screen keyboard (lower, upper, symbol modes)
- 🔘 FreeRTOS button input task

### Planned
- 📲 BLE phone notifications
- 🏓 ESP-NOW multiplayer (Pong, named device discovery)
- 🤖 Groq AI assistant (on-device chat via WiFi)
- 🌦️ Weather app
- 💬 WhatsUp P2P messaging
- 💀 BSOD heap watchdog
- 🔁 Daily 3AM silent reboot
- 📁 LittleFS chat history
- 😴 Light sleep eco mode (~31 days battery)

---

## 🏗️ Architecture

```
StrawberryOS (Universal Core)
├── WiFi stack
├── BLE stack
├── ESP-NOW stack
├── Power management
└── App layer (device specific)
    └── StrawberryWatchOS (this repo)
```

StrawberryOS is designed to be ported. The core is hardware-agnostic — build your own app layer for your own device.

---

## 🔋 Power Modes

| Mode | Description | Battery Life |
|---|---|---|
| Normal | All radios active, full brightness | ~1.5 days |
| Eco | Display off, light sleep, wake on button | ~31 days |

---

## 🚀 Getting Started

### Requirements
- Arduino IDE or PlatformIO (AntiGravity IDE recommended)
- ESP32 Arduino Core
- Libraries:
  - `Adafruit SSD1306`
  - `Adafruit GFX`
  - `RTClib`
  - `ArduinoJson`
  - `LittleFS`

### Flash
1. Clone this repo
2. Open `Smartwatch.ino` in your IDE
3. Select board: `XIAO ESP32-C6` (or `ESP32-C3` for dev)
4. Upload

---

## 📁 File Structure

```
StrawberryWatchOS/
├── Smartwatch.ino       # Main OS file
├── README.md
└── (PCB files coming soon)
```

---

## 🤝 Contributing

StrawberryOS is open to everyone.

- Found a bug? Open an issue
- Want a feature? Fork and PR
- Porting to another device? Document it and share

No experience required. If you're a hobbyist who got stuck — this project exists because the developer got stuck too.

---

## 📜 License

MIT License — For customising the OS to your own needs. Just keep it open source too :)

---

## 👤 Author

**Ashutosh** — Student, maker, and an average guy who wants to build complex stuff on his own...

---
