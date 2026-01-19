# Laboratory Activity#1: Working with Digital Signals

This activity demonstrates the use of arrays and for-loops to manage multiple output components efficiently. Instead of defining each pin individually, the program iterates through an integer array to initialize and toggle five LEDs in sequence.

**Objective**: To create a "chase" effect where LEDs turn on one by one and then turn off in the same order.

**Hardware Used**: * Arduino Uno R4 WiFi

5 LEDs

Resistors and Breadboard

**Key Concepts**:

**Arrays**: Used to store pin numbers {12, 11, 10, 9, 8} for cleaner code management.

**Iteration**: A for loop is utilized in the setup() function to set all pins to OUTPUT mode.

**Timing**: The delay(1000) function creates a 1-second interval between each LED state change.
