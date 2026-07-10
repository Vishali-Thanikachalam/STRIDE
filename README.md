# STRIDE – EV ADAS System

**STRIDE (STM32 Telemetry & Responsive Intelligent Driving Environment)** is a real-time Electric Vehicle Advanced Driver Assistance System (ADAS) built on the **STM32F103C8T6 (Blue Pill)**. It combines vehicle telemetry, obstacle detection, fault management, and a live Python dashboard for monitoring and visualization.

![Platform](https://img.shields.io/badge/Platform-STM32F103C8T6-03234B?logo=stmicroelectronics&logoColor=white)
![Framework](https://img.shields.io/badge/STM32-HAL-green)
![Simulator](https://img.shields.io/badge/Simulator-PICSimLab-blue)
![Dashboard](https://img.shields.io/badge/Dashboard-Python-yellow)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## Features

- Real-time EV telemetry
- Forward collision warning
- Blind-spot detection
- Parking assist
- Vehicle state machine
- Fault detection and recovery
- UART telemetry & command interface
- Live Python dashboard

---

## System Architecture

```
HC-SR04 Sensors
        │
        ▼
 STM32F103C8T6
  (STM32 HAL)
        │
   UART @115200
        │
        ▼
 Python Dashboard
```

---

## Hardware

| Component | Description |
|-----------|-------------|
| MCU | STM32F103C8T6 (Blue Pill) |
| Sensors | 3 × HC-SR04 Ultrasonic |
| Communication | UART |
| Output | PWM, LEDs, Buzzer |

---

## Repository Structure

```
stride/
├── docs/
├── firmware/
├── dashboard/
├── simulation/
└── tests/
```

---

## Getting Started

### Firmware

```bash
Open firmware/ev-adas.ioc
Build with STM32CubeIDE
Run in PICSimLab or flash to STM32
```

### Dashboard

```bash
cd dashboard
pip install -r requirements.txt
python main.py --port COMx --baud 115200
```


---

## Tech Stack

- C
- STM32 HAL
- STM32CubeIDE
- PICSimLab
- Python
- matplotlib
- pyserial

---
