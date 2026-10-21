# 🏔️ SENTINEL — Smart Hiking Stick

> **One foldable pole. Nine integrated safety systems. Built for the moments a hiker is completely alone.**

Sentinel is an AI-powered, off-grid connected smart trekking pole designed for solo and group trekkers in remote wilderness environments (e.g., Himalayan and Western Ghats circuits).

---

## 🌟 Key Features & Core Technology

- **Off-Grid SOS via LoRa + GPS:** 868/915 MHz long-range transceiver (10–15 km range) sends compressed digital telemetry (GPS, altitude, battery level, timestamp) with zero cellular signal.
- **On-Device AI (TinyML):** 
  - *Fall Detection & Auto-SOS:* Fuses IMU sensor data to distinguish normal stumbles from real falls; sends an auto-SOS over LoRa if unresponsive.
  - *Altitude-Aware Weather Alerts:* Uses BMP280 barometric pressure + GPS altitude to accurately predict storms without false alarms during ascents.
  - *Wildlife Classification:* Classifies approaching targets using thermal/PIR sensors to trigger appropriate deterrents.
- **Defense Systems:**
  - *Dual-Mode Acoustic Deterrent:* 18–25 kHz ultrasonic sweep + 85+ dB audible siren.
  - *Electric Defense Tip:* Low-current, high-voltage pulse circuit gated by a grip safety switch.
  - *Pre-Contact Thermal/PIR Sensor:* Handle vibration alert for warm bodies 5–10 m away.
- **Biometric Health Tracking:** Heart rate, SpO2 (MAX30102), and cuffless blood pressure estimation (PPG + Pulse Transit Time).
- **Kinetic Self-Charging:** Piezoelectric/magnetic induction charges an internal 18650 Li-ion cell on every footstep.
- **Field Utilities:** Retractable water quality probe (TDS/turbidity) and an integrated high-intensity LED torch.

---

## 🛠️ Hardware Stack & Estimated BOM

| Component Category | Key Hardware Used |
| :--- | :--- |
| **Microcontroller (MCU)** | ESP32-S3 / nRF52840 (TinyML enabled) |
| **Sensors** | MPU6050 (IMU), BMP280 (Barometer), MAX30102 (HR/SpO2), PIR / Thermal Array (AMG8833) |
| **Connectivity** | SX1276 / SX1262 LoRa Transceiver + GPS Module |
| **Power** | 18650 Li-ion cell, Piezo/Induction Generator, BMS, Bridge Rectifier |
| **Defense & Output** | Piezoelectric Siren (Ultrasonic/Audible), Pulse Generator, 0.96" OLED Display |

---

## 📂 Repository Structure
