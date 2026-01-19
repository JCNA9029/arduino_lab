# Laboratory Activity #4: Arduino Serial Connection

This activity demonstrates a more interactive approach to microcontroller programming by allowing a user to communicate with the Arduino via the Serial Monitor. It also introduces the millis() function to handle "multi-tasking" without freezing the program.

**Objective**: To create a system where a light-triggered alert can be manually overridden and stopped by typing a command into the computer.

**Hardware Used**:

Arduino Uno R4 WiFi

Photoresistor (LDR) 

LED 

**Key Concepts**:

**Serial Communication**: Uses Serial.available() and Serial.readStringUntil() to listen for specific text commands like "stop" from the user.

**Non-blocking Timing**: Instead of using delay(), which pauses the entire processor, this code uses millis() to track time intervals for blinking the LED. This allows the sensor to keep reading data even while the LED is flashing.

**String Manipulation**: Implements .trim() and .toLowerCase() to ensure user input is parsed correctly regardless of extra spaces or capitalization.

**Conditional State Management**: Uses a boolean flag (blinkingActive) to toggle the system's behavior based on both sensor input and serial commands.


