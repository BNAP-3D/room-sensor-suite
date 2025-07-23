# 🏠 Room Sensor Suite

> An open, hackable, and modular smart home sensor suite – built for tinkerers, makers, and automation enthusiasts.  
> **Currently in development – we’re actively seeking feedback to shape the final product.**

---

## 📌 Core Principles

1. **Hackable by Design**  
   Built to encourage tinkering, customization, and extensibility. Open pin headers, modular firmware, and community-friendly design.

2. **ESPHome Compatibility**  
   Every component integrates smoothly with ESPHome and Home Assistant for YAML-based configuration and automation.

3. **Ease of Assembly**  
   Minimal soldering, through-hole or pre-soldered components where possible, and documentation tailored for DIYers. Supports ESP32/ESP8266 boards.

4. **Modular & Affordable**  
   A minimal, functional base unit with optional upgrades. The goal: keep costs low while offering flexibility for advanced users.

---

## 🧩 Core Features (Initial Implementation)

The following features will be implemented in the first version of the Room Sensor Suite:

- **Presence Sensor (mmWave-based)**  
  Highly sensitive human presence detection for room automation, occupancy awareness, and security.

- **Temperature & Humidity Sensor**  
  Real-time room climate tracking for comfort and smart HVAC routines.

- **IR Blaster**  
  Control TVs, ACs, fans, and other IR-enabled devices. Fully programmable via Home Assistant.

- **Ambient Light Sensor**  
  Detects brightness for adaptive lighting control and time-of-day behavior logic.

---

## 🔌 Optional Add-ons (May Become Core)

The features below are optional for now – **but** based on community demand and practical use-cases, we may **promote them to core features** in future releases. Share your thoughts to help us decide!

- **CO₂ Sensor** (e.g., MH-Z19B)  
  For air quality monitoring and triggering ventilation.

- **TVOC / eCO₂ Sensor** (e.g., CCS811, SGP30)  
  Detects harmful volatile organic compounds and freshness levels of indoor air.

- **Air Pressure Sensor** (e.g., BMP280)  
  Enables weather-based automations and barometric trend detection.

- **Noise Level Detection**  
  Use a microphone to detect activity, presence, or noise alerts.

- **PIR Sensor**  
  Fast motion trigger, ideal as a wake-up complement to mmWave sensors.

- **Buzzer**  
  Audible alerts for timers, door status, alarms, and more.

🙋 *Have strong opinions about which of these should be core? [Tell us](https://github.com/BNAP-3D/room-sensor-suite/issues)!*

---

## 🤪 Experimental Ideas (Up for Debate)

These features are fun, but may not be practical for most installations. Still, if they excite you – let us know!

- **Control Interfaces** (Buttons, rotary encoders, etc.)  
  Could be used to control lighting, music, or scenes — but may conflict with optimal sensor placement.

- **OLED Display**  
  Can display useful info like time, temperature, or status — but must be visible, which can interfere with presence detection positioning.

---

## 🧠 Built-In Software Features

- **Bluetooth Proxy**  
  ESP32 devices double as BLE presence proxies in Home Assistant (e.g., detect phones, watches).

- **ESPHome YAML Templates**  
  Clean, modular templates for core + optional features. Easily extendable.

- **Room-Aware Naming**  
  Automatically assigns device names based on room location for easy integration.

- **OTA & Failsafe Behavior**  
  Support for over-the-air updates and graceful Wi-Fi fallback behavior.

---

## 📡 Presence Sensor Options

| Sensor    | Description         | Pros                      | Notes                 |
|-----------|---------------------|---------------------------|------------------------|
| LD2450    | High-performance    | Multi-zone, very accurate | Larger footprint       |
| LD2410C   | Compact alternative | Affordable, precise       | Best for small enclosures |

---

## ⚠️ Known Design Risks

- **Temperature Reading Distortion**  
  MCU or mmWave components may affect nearby temperature/humidity sensors.  
  _Mitigation:_ Distance or sleep-mode placement.

- **IR Blaster vs Sensor Placement Conflict**  
  Ideal IR line-of-sight might differ from optimal mmWave placement.  
  _Mitigation:_ IR extender or second IR node.

- **Ambient Light Readings Skewed by Artificial Lighting**  
  Lux readings may fluctuate unnaturally.  
  _Mitigation:_ Calibration logic or time-based fallback in automation.

---

## 🔄 Feature Finalization Process

🧪 *Note: The features currently listed under [Optional Add-ons](#-optional-add-ons) are not final.*  
We are actively gathering feedback from the community to understand which features matter most. Based on this input, some optional features may be **promoted to Core Features**.

🚧 For the **initial release**, only the finalized **Core Features** will be implemented.

📢 Please help us decide — [open an issue](https://github.com/BNAP-3D/room-sensor-suite/issues) or [submit a pull request](#-contributing) with your ideas!

---

## 🛣️ Roadmap (No Timeline)

- [ ] Finalize BOM for core features
- [ ] Create PCB and enclosure design
- [ ] Build and test core feature prototype
- [ ] Publish ESPHome YAML templates
- [ ] Document assembly and configuration steps
- [ ] Get community feedback on optional features
- [ ] Iterate on design and hardware enclosure
- [ ] Decide which optional features to promote
- [ ] Prepare for small-batch production or dev-kit preorders
- [ ] Launch v1 documentation and build guide

---

## 💬 We Need Your Input!

We're designing this product *with* the community – and your voice matters.

Whether you're:
- An automation enthusiast building a smarter home
- A maker looking to tinker and extend
- A developer with thoughts on ESPHome/YAML structure
- A user with feature requests or ideas

💡 Please share your input via [GitHub issues](https://github.com/BNAP-3D/room-sensor-suite/issues) or better yet, a [pull request](#-contributing)!

---

## 🤝 Contributing

We welcome contributions of all kinds:

1. Fork this repo
2. Add your suggestion (docs, features, examples, corrections)
3. Open a pull request

Pull requests suggesting changes to the direction or feature set are especially appreciated during this early stage.

---

## 📄 License

MIT – free to use, modify, and redistribute with attribution.  
Built by and for the community ❤️

---

> Made with solder, YAML, and a lot of late-night coffee ☕  