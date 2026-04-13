# Circuit Challenges Assignment

## Student Information

Name: MD PARVEZ ALAM
Course: Analog Electronics one 

---

## Overview

This assignment demonstrates the construction and testing of basic electronic circuits using components such as resistors, LEDs, transistors, and LDR sensors.

All circuits were built on a breadboard using components from the provided parts list, including:

* Breadboard
* Jumper wires
* 9V power supply
* Resistors
* LEDs
* PN2222 transistor
* LDR (Light Dependent Resistor)
* Multimeter

---

# Challenge 1: Bright Bright Lights

## Objective

To build a circuit with 4 LEDs that are bright, safe, and independent.

## Circuit Description

Each LED was connected in parallel with its own resistor:

Vcc → 200Ω resistor → LED → Ground

## Result

All LEDs glowed brightly. Removing one LED did not affect the others, confirming correct parallel configuration.

## Image

---

# Challenge 2: Meter Mystery

## Objective

To produce approximately 9 mA current using resistors.

## Calculation

Total resistance = 5 × 200Ω = 1000Ω

Using Ohm’s Law:
I = V / R
I = 9 / 1000 = 0.009 A = 9 mA

## Circuit Description

Five 200Ω resistors were connected in series and measured using a multimeter.

## Result

The measured current was approximately 9 mA.

## Images

(Add circuit image here)
(Add multimeter reading image here)

---

# Challenge 3: Night Light Company

## Objective

To create a light that turns ON in darkness and OFF in bright light.

## Circuit Description

A voltage divider was created using a 100K resistor and an LDR.
The output was connected to the base of a PN2222 transistor.

When:

* Light → LDR resistance low → transistor OFF → LED OFF
* Dark → LDR resistance high → transistor ON → LED ON

## Result

The LED turned ON in darkness and OFF in light.

## Images

(Add light condition image here)
(Add dark condition image here)

---

# Proof of Work

A photo with my name written on paper is included to verify that I built the circuits myself.

(Add proof image here)

---

# Conclusion

This assignment helped me understand:

* Series vs parallel circuits
* Ohm’s Law application
* Safe LED operation
* Voltage dividers
* Transistor switching
* Sensor-based automation using LDR
