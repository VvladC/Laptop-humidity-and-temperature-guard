# CoolPi
Arduino-based system for laptop cooling based on temperature and humidity sensors


![coolpi](https://github.com/user-attachments/assets/302af53b-119a-4fd6-a91d-eaf8d1c70e06)


Overheating can damage internal components.​
Users often resort to:​
  Lifting the laptop​
  Placing notebooks underneath to improve airflow​
  Reducing CPU performance to lower heat output​

What if we could automate and optimize this process?​

The solution? Smart Monitoring and Cooling System​

Automatically checks and reacts to environmental conditions​
Helps protect the laptop and ensure optimal performance​

Components Used​  
  
Arduino Uno board​  
Breadboard for wiring connections​  
Male-to-male jumper wires​  
DHT11 sensor (temperature & humidity)  ​
MG996R servo motor​  
LED’s​  
 Extra's ( optional )  ​
Phone charger cable​  

Wiring setup

DHT11 Sensor:​

Connected to Breadboard at slots A9–A6​  
Jumper from C9 → Breadboard (-)​  
Jumper from C7 → Arduino Pin 2​  
Jumper from C6 → Breadboard (+)​  

MG996R Servo Motor:​  

Yellow wire → Arduino Pin 9​  
Red wire → Breadboard (+)​  
Brown wire → Breadboard (–)​  


Power:​

Arduino 5V → Breadboard (+)​  
Arduino GND → Breadboard (–)​  

The sensor reads temperature and humidity every 10 seconds​

If values are within safe limits:​
No action is taken​

If values exceed set thresholds:​
Corresponding LEDs light up​
The motor activates a small propeller (mini fan)​

If values are dangerously high:​
The system performs a forced shutdown to protect the laptop​

Used libraries: Servo, DHT, Arduino.h​
