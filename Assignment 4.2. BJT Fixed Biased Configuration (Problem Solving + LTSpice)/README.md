# Assignment 4.2 – BJT Fixed Bias Configuration (Problem Solving + LTspice)

## Overview
This assignment analyzes a fixed-bias BJT circuit and verifies results using LTspice.

## Given Data
- VCC = 20V
- RB = 470kΩ
- RC = 910Ω
- β = 135
- VBE ≈ 0.7V

## Objectives
- Calculate IB, IC, IE, VC, VB, VE, VCE
- Determine Q-point
- Verify using LTspice

## Calculations

### Base Current (IB)
IB = (VCC - VBE) / RB  
IB = (20 - 0.7) / 470000  
IB ≈ 41.1 µA  

### Collector Current (IC)
IC = β × IB  
IC = 135 × 41.1µA  
IC ≈ 5.55 mA  

### Emitter Current (IE)
IE = IC + IB ≈ 5.59 mA  

### Collector Voltage (VC)
VC = VCC - (IC × RC)  
VC = 20 - (5.55mA × 910)  
VC ≈ 14.95 V  

### Base Voltage (VB)
VB ≈ 0.7 V  

### Emitter Voltage (VE)
VE = 0 V  

### Collector-Emitter Voltage (VCE)
VCE = VC - VE  
VCE ≈ 14.95 V  

## Final Results
- IB = 41.1 µA  
- IC = 5.55 mA  
- IE = 5.59 mA  
- VC = 14.95 V  
- VB = 0.7 V  
- VE = 0 V  
- VCE = 14.95 V  

## Operating Point
Q-point ≈ (VCE = 14.95V, IC = 5.55mA)

## Load Line
VCC = IC RC + VCE  

Endpoints:
- VCE = 20V, IC = 0  
- VCE = 0, IC = 21.98mA  

## LTspice Netlist
```
* BJT Fixed Bias Circuit
V1 VCC 0 DC 20
RB VCC B 470k
RC VCC C 910
Q1 C B 0 QNPN
.model QNPN NPN(BF=135)
.op
.end
```

## Conclusion
The transistor operates in the active region with Q-point:
Q ≈ (15V, 5.55mA)

Results are verified by LTspice simulation.
