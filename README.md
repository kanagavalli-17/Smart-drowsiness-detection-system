# Smart-drowsiness-detection-system

Project Description : 
• This project detects driver drowsiness using ESP32
• Eye closure is simulated using a push button in Wokwi
• If eyes remain closed for more than 3 seconds, alarm is triggered
• Buzzer and LED are used as alert system

Objective : 
• To prevent road accidents caused by driver fatigue
• To detect eye closure using embedded system
• To alert driver using sound and light indicators
• To build a low-cost safety system

Components Used : 
• ESP32 DevKit V1
• Push Button (Eye Blink Simulation)
• Buzzer
• LED
• 220Ω Resistor
• Jumper Wires

circuit connection: 
ESP32 DevKit
│
├── Eye Blink Sensor (Push Button in Wokwi) → Detect Eye Status
│      ├── VCC → 3.3V
│      ├── GND → GND
│      └── OUT → GPIO 15
│
├── Buzzer → Alert System
│      ├── + → GPIO 18
│      └── - → GND
│
├── LED → Warning Indicator
│      ├── Anode (+) → GPIO 2 (via 220Ω resistor)
│      └── Cathode (-) → GND
│
└── Power Supply (USB / 3.3V from ESP32)

Working Principle : 
• Eye open → system remains normal
• Eye closed (button pressed) → timer starts
• If closed for more than 3 seconds → alarm activates
• LED and buzzer turn ON as warning signal
• Helps detect driver drowsiness effectively

Code Explanation :
• ESP32 reads digital input from GPIO 15
• Detects eye open or closed state
• If signal stays LOW for 3 seconds
• Activates buzzer on GPIO 18
• Turns ON LED on GPIO 2
• Resets when eye opens again

Tools Used :
• Wokwi Simulator
• Arduino IDE
• GitHub

Future Improvements:
• Add camera-based eye detection system
• Integrate GSM for SMS alerts
• Connect to IoT cloud platform
• Add OLED display for real-time status

Conclusion:
• This project improves road safety
• Detects driver fatigue in real-time
• Provides instant alert using buzzer and LED
• Simple and low-cost embedded system solution
