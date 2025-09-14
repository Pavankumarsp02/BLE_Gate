# BLE_Gate

This project focuses on developing a custom PCB using the ESP32 microcontroller to create a Bluetooth Low Energy (BLE)-based automated access system for gates, allowing authorized bikes, cars, and other vehicles to pass through securely and seamlessly.

System Overview:

BLE Transmitter (Vehicle Unit):
•	A custom ESP32-based PCB is installed in each vehicle (bike, car, etc.).
•	The system is activated via a trigger switch or signal, which can be integrated with existing vehicle controls (e.g., horn, headlight, passby ignition, or dedicated button).
•	Once triggered, the BLE transmitter powers on and begins broadcasting its unique MAC address.

BLE Receiver (Gate Unit):
•	A fixed ESP32 receiver module is installed at the gate, powered continuously and always scanning for BLE signals.
•	When it detects a BLE broadcast, it checks the device's MAC address against a predefined list of authorized addresses.
•	If the MAC address is authenticated, the gate reacts based on the vehicle type:
•	Bike / Two-Wheeler: Gate opens partially—just enough for the bike to pass.
•	Car / Large Vehicle: Gate opens fully to allow complete passage.
•	After opening, the gate remains open for a fixed time (e.g., 15 seconds) and then automatically closes.

Key Features:
✅ Vehicle-Type Specific Behavior: Partial or full gate opening based on the authorized MAC address classification (bike vs. car).
✅ Custom ESP32 PCB: Designed for compact integration into vehicle systems with minimal power consumption.
✅ Low Power BLE Operation: Transmitter is powered only when the vehicle switch is triggered, conserving battery.
✅ Secure Access Control: Only vehicles with authorized MAC addresses can activate the gate.
✅ Fully Automated: No need for remotes, RFID cards, or smartphone apps—just a button press.

Possible Integrations:
•	Apartment/residential society gates.
•	Office/industrial parking lots.
•	Private or commercial garages.
•	Gated communities with mixed vehicle types.
