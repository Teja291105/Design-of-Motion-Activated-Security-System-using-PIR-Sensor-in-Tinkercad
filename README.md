# NAME: JANANI V
# REG NO: 212223060099
# Design-of-Motion-Activated-Security-System-using-PIR-Sensor-in-Tinkercad

**AIM:** 

To detect motion using a PIR sensor connected to an Arduino and trigger an LED (using the built-in LED) when motion is sensed. 

**Hardware / Software Tools required:**
- Arduino Uno R3 – 1 No 
- PIR Sensor – 1 No 
- LED (in-built on Arduino pin 13) – 1 No 
- 220-ohm resistor – 1 No (used with external LED if necessary) 
- Breadboard – 1 No 
- Jumper wires – As required 
- USB Cable – 1 No (for uploading code and powering Arduino) 
- Computer with Tinkercad or Arduino IDE installed

**Theory:** 

Passive Infrared (PIR) sensors are electronic devices that detect motion by sensing infrared radiation emitted by objects. Every object with a temperature above absolute zero emits infrared radiation. The PIR sensor detects this radiation and can sense motion when a warm object, such as a human body, passes within its detection range. The sensor contains a pair of pyroelectric sensors housed under a Fresnel lens, which focuses the infrared signals onto the sensor surface. When the infrared levels change rapidly between the two pyroelectric sensors— such as when a person walks by—the sensor outputs a HIGH signal indicating motion detection. PIR sensors are widely used in motion detection systems, security alarms, automatic lighting systems, and smart surveillance. They are popular due to their low power consumption, affordability, and ease of integration with microcontrollers such as the Arduino Uno. The sensor typically has three pins: VCC (power), GND (ground), and OUT (signal). When idle, the output pin remains LOW. Once motion is detected, the sensor sends a HIGH signal to the microcontroller, which can be used to trigger a response such as turning on an LED or activating an alarm. In this experiment, the PIR sensor is connected to an Arduino Uno board. The VCC pin of the sensor is connected to the 5V supply of the Arduino to power the sensor. The GND pin is 48 connected to the Arduino’s ground. The OUT pin is connected to a digital input pin (pin 2 in this case) of the Arduino. The Arduino continuously monitors the state of the signal pin. If the signal pin goes HIGH, it means the sensor has detected motion, and the Arduino is programmed to turn ON the built-in LED on pin 13. If no motion is detected, the signal remains LOW, and the LED is turned OFF.

**Circuit Diagram:**



<img width="1536" height="632" alt="Frantic Inari-Borwo" src="https://github.com/user-attachments/assets/d9bf874f-e338-4725-8165-c95bef6cfe92" />

**Procedure:**

1. Log in to Tinkercad, go to Circuits, and click Create New Circuit.

2. Add the Arduino Uno, PIR sensor, optional LED, 220-ohm resistor (if using LED), and jumper wires.

3. Connect PIR sensor VCC to 5V, GND to GND, and OUT to digital pin 2 on the Arduino.

4. If using an external LED, connect anode to pin 13 through a 220-ohm resistor and cathode to GND.

5. Open the Code editor, switch to Text mode, and write the Arduino program.

6. Start the simulation and test the PIR sensor by moving the virtual motion object near it.

7. If it doesn’t work, check wiring, fix any code errors, and adjust the sensor angle if needed.

8. Stop the simulation and save the circuit.


**Code:**

```
int buttonState = 0; 
void setup() 
{ 
  pinMode(2, INPUT); 
  pinMode(LED_BUILTIN, OUTPUT); 
} 
void loop() 
{ 
  buttonState = digitalRead(2); 
  if (buttonState == HIGH) 
  { 
    digitalWrite(LED_BUILTIN, HIGH); 
  } 
  else 
  { 
    digitalWrite(LED_BUILTIN, LOW); 
  } 
  delay(10); 
}
```

**Output:**


<img width="1024" height="680" alt="OP" src="https://github.com/user-attachments/assets/981dd57e-f3a6-423e-9ec0-639a4b1cd907" />



**Result:**

The PIR sensor successfully detected motion and triggered the Arduino to turn ON the built-in LED. The LED remained OFF when no motion was present, confirming correct circuit and 
code functionality.




