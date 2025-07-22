# GPS-Tracking-System

# Embedded GPS Landmark Navigation System

## Project Overview
An embedded system that reads real-time GPS coordinates and displays proximity to predefined landmarks on an LCD, with visual (LED) and audible (buzzer) feedback. Developed for TM4C123G LaunchPad as part of CSE 211s (Introduction to Embedded Systems) course.

*Key Features:*
- Real-time GPS coordinate acquisition
- Nearest landmark detection from predefined database
- LCD display of landmark information
- Visual feedback using RGB LEDs
- Audible alerts when approaching specific landmarks
- Autonomous operation with battery power

## Hardware Components
| Component               | Connection           |
|-------------------------|---------------------|
| TM4C123G LaunchPad      | Base microcontroller |
| GPS Module (UART)       | PB0 (RX), PB1 (TX)  |
| 16x2 LCD Display        | Multiple GPIO pins  |
| RGB LED                 | PF1 (R), PF2 (B), PF3 (G) |
| Buzzer                  | PE3                 |

## Software Architecture
```plaintext
Project Root/
├── HAL/
│   ├── LCD.c           # LCD driver
│   ├── LCD.h
│   ├── GPS.c           # GPS parser
│   └── GPS.h
├── MCAL/
│   ├── GPIO.c          # Port initialization
│   ├── GPIO.h
│   ├── UART.c          # GPS communication
│   └── UART.h
├── Utilities/
│   ├── bit_ops.h       # Bit manipulation macros
│   └── tm4c123gh6pm.h  # MCU registers
└── main.c              # Application logic
