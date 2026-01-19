# Midterm Laboratory Exam

This project implements a dual-mode light monitoring system. It allows the user to switch between an Automatic Mode, which uses fixed environmental presets, and a Manual Mode, where the user can calibrate sensitivity thresholds in real-time through the Serial Monitor.

**Objective**: To create a flexible light-sensing interface that supports remote configuration and real-time adjustments.

**Hardware Used**:

Arduino Uno R4 WiFi.

Photoresistor (LDR).

3 LEDs (Green, Yellow, Red).

**Key Concepts**:

**State Machine Logic**: Uses a boolean isAutomatic to shift the entire program's behavior between preset and user-defined logic.

**Advanced Serial Command Parsing**: Implements complex string commands like SET LOW XX and MODE AUTO, using startsWith() and substring() to extract numeric parameters from user input.

**Data Normalization**: Maps raw 10-bit analog readings (0–1023) into a more readable 0–100% scale for consistent threshold comparison.

**Input Validation**: Uses the constrain() function to ensure that manual thresholds remain within logical bounds (e.g., the LOW threshold cannot exceed the HIGH threshold).

**Environmental Classification**: Provides "Cloudy" vs. "Clear" status updates based on light intensity levels when in automatic mode.

