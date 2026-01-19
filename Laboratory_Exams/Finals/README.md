# Finals Laboratory Exam

This project implements an IoT Gateway model where an Arduino acts as an edge device, sending signals to a Python client that serves as a bridge to a remote web server. This architecture is fundamental to modern Internet of Things systems where low-power devices interact with cloud-based services.

**Objective**: To trigger a remote API endpoint (specifically toggling a group of LEDs) via a physical button press on an Arduino.

**Hardware Used**:

Arduino Uno.

Push button (Active LOW).

Internal Pull-up Resistor.

**Key Concepts**:

**IoT Gateway Logic**: The Python client (iot_client.py) monitors the serial port for a "Group Number" and dynamically constructs a RESTful API URL to perform a network request using the requests library.

**Single-Shot Triggering**: The Arduino firmware is designed to send the group number only on the "push" action (transition to LOW), preventing repeated network requests if the button is held down.

**Robust Network Communication**: The Python client includes comprehensive error handling for serial communication loss, timeout exceptions, and non-200 HTTP responses.

**Advanced Debouncing**: Uses a time-based debounce algorithm with millis() to filter mechanical noise and ensure signal integrity.
