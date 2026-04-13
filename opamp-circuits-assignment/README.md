# OPAMP Circuits Assignment

## Student Information
Name: YOUR NAME  
Course: 4_EFA8100-3004  
Lab: LAB 0 - OpAmp Applications  

## Submission Contents
This repository contains:
- LTspice-ready circuit files for:
  - Task 1: Open-Loop Op-Amp (Comparator)
  - Task 2: Non-Inverting Amplifier
  - Task 3: Inverting Amplifier
- A short explanation of expected behavior
- Placeholder image locations for waveform screenshots

## Tool
LTspice and Lab

## Submission Note
Your instructor asked for:
- One LTspice schematic file (.asc)
- Screenshots of waveforms
- GitHub submission only

Because screenshots must match your own LTspice run, open each circuit in LTspice, run the simulation, and capture the waveform windows.

---

# Task 1 - Open-Loop Op-Amp (Comparator)

## Build
- Op-amp supply: +5 V and -5 V
- Vin -> non-inverting input (+)
- Inverting input (-) -> GND
- No feedback
- Vin = SINE(0 10m 1k)

## Expected Result
- The output saturates near the supply rails
- The op-amp behaves like a comparator
- Since the input is a sine wave around 0 V, the output becomes a square-like waveform

## Screenshot to Add
Save a screenshot showing:
- Vin
- Vout

---

# Task 2 - Non-Inverting Amplifier

## Build
- Vin -> non-inverting input (+)
- Rg = 10k from inverting input (-) to GND
- Rf = 90k from Vout to inverting input (-)
- Supply rails: +5 V and -5 V
- Vin = SINE(0 10m 1k)

## Gain
Av = 1 + Rf/Rg  
Av = 1 + 90k/10k = 10

## Expected Result
- Output amplitude is about 10 times input amplitude
- No phase inversion
- Vin = 10 mV peak should give about 100 mV peak at output

## Screenshot to Add
Save a screenshot showing:
- Vin
- Vout

---

# Task 3 - Inverting Amplifier

## Build
- Non-inverting input (+) -> GND
- Rin = 10k from Vin to inverting input (-)
- Rf = 90k from Vout to inverting input (-)
- Supply rails: +5 V and -5 V
- Vin = SINE(0 10m 1k)

## Gain
Av = -Rf/Rin  
Av = -90k/10k = -9

## Expected Result
- Output amplitude is about 9 times input amplitude
- 180 degree phase inversion
- Vin = 10 mV peak should give about 90 mV peak at output

## Screenshot to Add
Save a screenshot showing:
- Vin
- Vout

---

# GitHub Folder Suggestion

```text
opamp-circuits-assignment/
├── README.md
├── task1_comparator.cir
├── task2_non_inverting.cir
├── task3_inverting.cir
└── screenshots/
    ├── task1_waveform.png
    ├── task2_waveform.png
    └── task3_waveform.png
```

---

# How to Run in LTspice
1. Open LTspice
2. Create a new schematic, or convert these netlists into schematics
3. Place the op-amp symbol and components
4. Use the same values listed in each task
5. Add the transient command:
   .tran 10ms
6. Run the simulation
7. Plot Vin and Vout
8. Save screenshots and upload to GitHub

---

# Short Conclusion
This assignment demonstrates three important op-amp behaviors:
- Open-loop operation as a comparator
- Non-inverting amplification with positive gain
- Inverting amplification with phase reversal

