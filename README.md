# Industrial Temperature & Humidity Control System (I2C Simulation)

The Smart Thermal-Climate Controller is an automated system designed to maintain specific environmental conditions in enclosed spaces. 
Unlike standard hobbyist projects, this implementation focuses on low-level optimization and protocol simulation.
The project solves the "Tinkercad Component Gap" by emulating an AM2320 sensor via a secondary microcontroller, creating a realistic I2C Master-Slave environment.

To reduce GPIO consumption, the system uses a Time-Division Multiplexing (TDM) strategy.

- The Problem: Driving two 7-segment displays normally requires 14 pins.
- The Solution: Shared data lines with NPN transistor-based cathode switching.
- The Result: Flicker-free 2-digit display using only 9 pins, leveraging the human eye's persistence of vision.

Custom I2C Sensor Emulation (Slave-Mode)

- Since physical AM2320 modules aren't in Tinkercad, a dedicated Arduino acts as the sensor.
- Register-Level Requests: The Slave responds to specific memory-address requests from the Master.
- Analog-to-Digital Mapping: Real-time potentiometer data is mapped to 10-bit temperature/humidity packets.

## Installation & Simulation

Setup Tinkercad:

- [Open the Tinkercad link right here](https://www.tinkercad.com/things/gFadaWyQrgL-proiect-isca-final)
- Import the `master.ino` and `slave.ino` files into their respective controllers.
- Mirror the wiring shown in the `docs/schematic.png`.

## Contributing

This is an open-source project. Contributions regarding PID control implementation or OLED display support are welcome. 
