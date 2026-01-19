# Laboratory Activity#6: Bidirectional Control using Arduino and Python

This project demonstrates a sophisticated full-duplex communication system between Python and Arduino. It implements a feedback loop where physical hardware inputs (buttons) trigger software logic in Python, which subsequently controls hardware outputs (LEDs).

**Objective**: To create a synchronized system where pressing a physical button sends a specific character to a Python script, which then "echoes" a corresponding command back to the Arduino to toggle an LED.

**Hardware Used**:

Arduino Uno R4 WiFi 

3 LEDs (Red, Green, Blue) 

3 Push Buttons 

Internal Pull-up Resistors 

**Key Concepts**:

**Software Debouncing**: Implements a debounceDelay of 50ms to filter out mechanical noise from the buttons, ensuring each press is only registered once.

**Input Pull-up Logic**: Utilizes INPUT_PULLUP to simplify the circuit, allowing buttons to be connected directly to GND without external resistors.

**Serial Buffer Management**: Uses Serial.setTimeout(10) and input.trim() to ensure rapid, clean reading of incoming serial strings without blocking the main loop.

**Strict Protocol Validation**: The Arduino code performs a "length check" to only process commands that are exactly one character long, preventing errors from malformed data.

**Python Integration**: The Python script monitors ser.in_waiting to asynchronously read button signals ('R', 'G', 'B') and translate them into numeric commands ('1', '2', '3') for the Arduino.

