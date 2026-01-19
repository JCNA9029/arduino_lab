# Laboratory Activity#3: Working with Sensors

This activity involves the creation of a simulated safety system that monitors environmental conditions in real-time. The system integrates a thermistor for temperature sensing and a photoresistor (LDR) to detect sudden brightness, such as a flame.

**Objective**: To develop a multi-condition alert system that triggers a high-frequency alarm only when both temperature and light thresholds are exceeded.

**Hardware Used**:

Arduino Uno R4 WiFi 

Thermistor (NTC) 

Photoresistor (LDR) 

Buzzer/LED for Alert 

**Key Concepts**:

**Steinhart-Hart Equation**: Implements complex math to convert raw analog resistance into a precise Celsius temperature reading.

**Data Mapping & Constraining**: Normalizes raw LDR values into a specific range (100–220) for consistent threshold comparison.

**Modular Programming**: Uses dedicated functions like readTemperatureC(), readLDRValue(), and triggerAlert() to keep the loop() clean and organized.

**Dynamic Alert Frequency**: The alarm's pulse speed (delay) changes based on the severity of the detected temperature, providing an audible cue of the danger level.






