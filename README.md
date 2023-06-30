# Automatic-Light-Switching
This code is written in arduino which is somewhat similar to C++.

Breakdown of the code:
    
Variable Declarations:
releNO: Represents the output pin number (13) connected to a relay.
inputPir: Represents the input pin number (2) connected to the PIR sensor.
val: Stores the current state of the PIR sensor.
resuldoSensorLDR: Stores the value read from the LDR sensor.
sensorLDR: Represents the analog input pin number (A0) connected to the LDR sensor.
setup() Function:

Sets the releNO pin as an output pin.
Sets the inputPir and sensorLDR pins as input pins.
Begins serial communication at a baud rate of 9600.

loop() Function:
Reads the state of the inputPir pin and stores it in the val variable.
Reads the analog value from the sensorLDR pin and stores it in the resuldoSensorLDR variable.
Checks if the resuldoSensorLDR value is less than 600.
If true, it further checks if val is HIGH (motion detected).
If motion is detected, it sets the releNO pin to HIGH (turns on the relay) and delays for 5 seconds.
If no motion is detected, it sets the releNO pin to LOW (turns off the relay) and delays for 300 milliseconds.
If the resuldoSensorLDR value is greater than or equal to 600, it sets the releNO pin to LOW (turns off the relay), prints the resuldoSensorLDR value to the Serial Monitor, and delays for 500 milliseconds.
