
# 💉 IoT Glucometer – From Electrons to Web Dashboard

A full-stack bio-sensing pipeline that converts raw electron flow from a glucose sensor into live digital readings and visualizations.

This project demonstrates how to safely acquire picoamp–microamp currents, amplify and digitize them, convert to meaningful units, and stream them end-to-end into a web frontend.

Through this work, we aim to explore and devise a non-invasive method for glucose detection, moving closer to practical, safe, and continuous monitoring solutions.


## 🔑 Core Principles

1. ⚡ Currents, not single electrons → Measurements work at scale (pA–µA), using charge → current → voltage → ADC counts.

2. 🔒 Safety first → Always current-limit (< µA to body) and isolate the measurement front-end.

3. 📐 Calibration is king → Without proper protection, filtering, and calibration, numbers are meaningless.


## Roadmap

- Electron to Digital singal:
  ![image alt]() 

- Digital signal to data visualiation
  ![image alt]()


## 🛠️ Hardware → Software Flow
1. Analog front-end: Transimpedance amplifier (TIA) + anti-alias filter.

2. ADC stage: 24-bit Delta-Sigma ADC (e.g., ADS1256) converts voltage to counts.

3. MCU: ESP32 samples ADC, applies calibration, sends JSON packets via MQTT/WebSocket.

4. Backend: Node.js + Express + Socket.io ingests payloads, validates, and stores.

5. Frontend: React (+ Next.js) web app streams live values and graphs in real time.

## Features

- Shows the glucose levels and its history
- Cross platform



## 📊 Example Conversion

![image alt]()

