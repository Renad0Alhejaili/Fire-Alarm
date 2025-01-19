# Fire Alarm System Using Arduino  

## Overview  
This project is about creating a fire alarm system using an Arduino board. The goal is to detect fire through temperature and smoke sensors and trigger an alarm using a buzzer and an LED. The system is simple and provides a basic fire safety solution.  

---

## Features  
- Fire Detection: Continuously monitors temperature and smoke levels.  
- Buzzer Alarm: Produces a loud sound when fire is detected.  
- LED Indicator: Lights up to warn about danger.  
- Real-Time Alert: Responds immediately to any fire hazard.  

---

## Components Used  
1. Arduino Uno: The main controller of the system.  
2. Temperature Sensor (LM35): Measures the temperature.  
3. Smoke Sensor (MQ-2): Detects smoke in the environment.  
4. Buzzer: Emits the alarm sound.  
5. LED: Lights up when fire is detected.  
6. Resistors and Jumper Wires: For connecting the components.  
7. Power Supply: To power the Arduino and sensors.  

---

## Installation and Setup  
1. Connect all the components based on the circuit diagram.  
2. Upload the Arduino code to the board using the Arduino IDE.  
3. Power the Arduino with a USB cable or a 9V battery.  
4. Test the system by introducing smoke or increasing the temperature.  

---

## How It Works  
1. The temperature and smoke sensors monitor the surroundings.  
2. When the temperature exceeds a certain limit or smoke is detected:  
   - The buzzer turns on.  
   - The LED lights up.  
3. When the environment is safe again, the system resets itself.  

---

## Applications  
- Homes and Apartments
- Offices
- Small Warehouses
- Classrooms or Labs

---

## Future Improvements  
- Adding wireless connectivity (Wi-Fi or Bluetooth) for remote monitoring.  
- Sending SMS alerts using a GSM module.  
- Using more sensitive sensors for better detection.  
