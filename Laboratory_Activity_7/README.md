# Laboratory Activity #7: Controllling Arduino using FastAPI

This project transforms the Arduino into an IoT-capable device. It uses a FastAPI backend to expose hardware controls as web endpoints, allowing the LEDs to be toggled via HTTP requests (e.g., through a web browser or Postman).

**Objective**: To build a web-serviced control system where hardware states are managed via FastAPI while maintaining manual physical control through buttons.

**Hardware Used**:

Arduino Uno.

3 LEDs (Red, Green, Blue).

3 Push Buttons.

**Key Concepts**:

**FastAPI Backend**: Implements GET routes like /led/on, /led/off, and dynamic paths like /led/{color} to handle hardware commands.

**Multi-threading**: Uses the Python threading library to run a background serial reader, ensuring the API stays responsive while simultaneously listening for button press notifications from the Arduino.

**Serial Protocol**: The Arduino logic is designed to parse single-character commands ('1', '2', '3', 'o', 'f') and use tolower() to ensure case-insensitive communication.

**Hardware Interrupt Simulation**: The Arduino code uses while(digitalRead(btn) == HIGH); loops to act as a "busy-wait," ensuring a single button press only triggers a state change once.

**Error Handling**: The Python script includes a try-except block to manage connection states and raises HTTPException (Status 500) if the API is called without an active Arduino connection.
