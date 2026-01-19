# Laboratory Activity#5: Receiving Serial Connection using Arduino from Python

This project showcases the integration of Python and Arduino to create a desktop-controlled hardware interface. It utilizes a modular approach by separating hardware logic into a C++ header file and providing a user-friendly menu through a Python script.

**Objective**: To build a system where a user can control multiple LEDs (Red, Green, Blue) from their computer keyboard using a custom Python interface.

**Hardware Used**:

Arduino Uno R4 WiFi

Red, Green, and Blue LEDs 

Resistors and Breadboard

**Key Concepts**:

**Modular Programming (.h files)**: Hardware-specific functions like initLEDs() and processInput() are encapsulated in a header file to keep the main .ino file clean and readable.

**Python pyserial Library**: Used to establish a connection between the PC and the Arduino over a COM port.

**Switch-Case Logic**: Efficiently handles multiple single-character commands ('R', 'G', 'B', 'A', 'O') to toggle LED states.

**Robust Serial Handling**: The Arduino code is designed to ignore newline (\n) and carriage return (\r) characters, ensuring command stability.

**User Experience (UX)**: The Python script features a "Clear Screen" function and a visual menu to provide a professional CLI experience.



