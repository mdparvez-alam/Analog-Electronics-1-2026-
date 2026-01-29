# Assignment 2.6 – Diode Selection for a Real Application

## Application
A simple 12 V DC input protection circuit was designed to protect electronic components from reverse polarity connection.

## Selected Diode
**1N5819 Schottky Diode**

## Justification

### Voltage Rating
The 1N5819 has a reverse voltage rating of 40 V, which is safely above the required 12 V DC input. This provides sufficient margin for voltage spikes.

### Current Rating
The diode supports up to 1 A average forward current, which is suitable for low to moderate power electronic circuits.

### Cost and Availability
The 1N5819 is inexpensive, widely available, and commonly used in power protection circuits, making it a practical real-world choice.

## Simulation
LTspice simulation confirms correct operation. The diode allows current flow during correct polarity and blocks current during reverse connection, protecting the load.
