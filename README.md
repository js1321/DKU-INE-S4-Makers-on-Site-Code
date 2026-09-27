# DKU-INE-S4-Makers-on-Site-Code
Source code for DKU INE Lab Session 4 Makers on Site project.
This repository contains ESP32 firmware for a campus pond freshwater ecosystem assessment and ecological protection prototype.

## Project Overview
This embedded system collects multi-dimensional environmental data for on-site freshwater monitoring:
- **TDS sensor**: Measure total dissolved solids for water quality evaluation with temperature compensation
- **MPU6050 IMU**: Detect probe tilt angle and calculate acceleration variance to evaluate surface water turbulence, filtering unreliable readings caused by shaking
- **Light sensor**: Capture ambient light intensity
- **RGB 1602 LCD**: Real-time local display of sensor readings and warning messages. RGB backlight turns green for normal status and red for abnormal alerts.

## 3D Print
![Appearence](https://github.com/js1321/DKU-INE-S4-Makers-on-Site-Code/blob/704a1b6a3a34a3878e6d1c153ac84323729c66ec/assests/3D_printing_boat.jpg)


## Hardware List
- ESP32 DevKit
- TDS water quality sensor (UART)
- MPU6050 6-axis accelerometer & gyroscope
- Analog light sensor
- DFRobot RGB LCD1602
- MSP20 pressure sensor (hardware mounted, pressure alarm logic commented out)

## Core Features
1. Periodically read TDS value with temperature compensation algorithm
2. Monitor probe inclination and water surface fluctuation to reduce measurement error
3. Comprehensive environment status judgment, automatic alarm when threshold exceeded
4. Local visual feedback via LCD + RGB backlight
5. Serial port output all sensor data for logging and post analysis

## Source File
`pond_freshwater_monitor.ino`: Main ESP32 Arduino firmware. Contains all sensor acquisition, tilt & turbulence calculation, threshold checking and screen display logic.

## How to Compile & Upload
Platform: Arduino IDE / PlatformIO
Required Libraries:
- Wire
- DFRobot_RGBLCD1602
- Adafruit_MPU6050
- Adafruit_Sensor

## Notes
This project was built for INE Lab Makers on Site activity at Duke Kunshan University.

