# Laboratory Activity#2: Working with Analog Signals

This activity explores Pulse Width Modulation (PWM) to control the brightness of LEDs, creating a smooth fading effect rather than a simple on/off state. The code utilizes nested while loops and the map() function to translate abstract steps into analog voltage levels.

Objective: To sequentially fade five LEDs from 0% to 100% brightness and back down, highlighting the hardware differences between the Arduino R3 and R4.

Hardware Used:

Arduino Uno R4 WiFi 
5 LEDs 
Resistors and Breadboard

Key Concepts:
PWM (Pulse Width Modulation): Used via analogWrite() to simulate variable voltage for LED brightness control.

Hardware Specifics: Unlike the Arduino R3, the R4 supports PWM on all digital pins, allowing for greater flexibility in circuit design.

The map() Function: Scales a "step" value (0–100) to the required 8-bit analog range (0–255) for the microcontroller.

Nested Loops: Employs while loops to manage both the selection of the LED and the incremental change in brightness.

