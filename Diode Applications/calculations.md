# Calculations — Diode Applications (Week 3–4)

## Assumptions / Models
- Thermal voltage: \(V_T = \frac{kT}{q}\)
- Approximate diode model:
  - Silicon diode (Si) ON: \(V_D \approx 0.7\text{ V}\)
  - Silicon diode OFF: open circuit
  - GaAs diode ON: \(V_D \approx 1.2\text{ V}\) (typical)
- Ideal diode model:
  - ON: \(V_D = 0\text{ V}\)
  - OFF: open circuit

---

## 1(a) Thermal voltage at 25°C

\[
V_T = \frac{kT}{q}
\]

Where:
- \(k = 1.38\times 10^{-23}\ \text{J/K}\)
- \(q = 1.60\times 10^{-19}\ \text{C}\)
- \(T = 25^\circ C = 298\text{ K}\)

\[
V_T = \frac{(1.38\times10^{-23})(298)}{1.60\times10^{-19}}
\approx 0.0257\text{ V}
\]

**Answer:** \(\boxed{V_T \approx 25.7\text{ mV}}\)

---

## 1(b) Diode current using Shockley equation

Given:
- \(I_S = 40\text{ nA} = 40\times10^{-9}\text{ A}\)
- \(n = 2\)
- \(V_D = 0.5\text{ V}\)
- \(V_T = 0.0257\text{ V}\)

\[
I_D = I_S\left(e^{\frac{V_D}{nV_T}} - 1\right)
\]

\[
nV_T = 2(0.0257)=0.0514\text{ V}
\]

\[
\frac{V_D}{nV_T}=\frac{0.5}{0.0514}\approx 9.73
\]

\[
I_D \approx 40\times10^{-9}(e^{9.73}-1)
\approx 40\times10^{-9}(16800)
\approx 6.73\times10^{-4}\text{ A}
\]

**Answer:** \(\boxed{I_D \approx 0.673\text{ mA}}\)

---

## 2) Chapter 2, Problem 4 (Boylestad)

Circuit: \(E=30\text{ V}\), Si diode in series with \(R=1.5\text{ k}\Omega\)

### (a) Approximate model (Si diode)

Diode is forward-biased → ON, so \(V_D \approx 0.7\text{ V}\)

\[
V_R = E - V_D = 30 - 0.7 = 29.3\text{ V}
\]

\[
I_D = \frac{V_R}{R}=\frac{29.3}{1500}=0.01953\text{ A}\approx 19.5\text{ mA}
\]

**Answers:**
- \(\boxed{V_D \approx 0.7\text{ V}}\)
- \(\boxed{V_R \approx 29.3\text{ V}}\)
- \(\boxed{I_D \approx 19.5\text{ mA}}\)

### (b) Ideal model

Ideal ON diode: \(V_D = 0\)

\[
V_R = 30\text{ V}
\qquad
I_D = \frac{30}{1500}=0.02\text{ A}=20\text{ mA}
\]

**Answers:**
- \(\boxed{V_D = 0\text{ V}}\)
- \(\boxed{V_R = 30\text{ V}}\)
- \(\boxed{I_D = 20\text{ mA}}\)

### (c) Comment (comparison)

Ideal and approximate are close because \(30\text{ V} \gg 0.7\text{ V}\).  
So the ideal model can be a good approximation when the supply voltage is much larger than the diode drop.

---

## 3) Chapter 2, Problem 5 (Boylestad) — Approximate model

### (a)
The diode is reverse-biased (no conduction).

\[
\boxed{I = 0\text{ A}}
\]

### (b)
Right side is connected to ground. The 20 V source makes the left node \(-20\text{ V}\).
With diode ON, node before resistor is:

\[
V \approx -20 + 0.7 = -19.3\text{ V}
\]

Current through 10 Ω branch:

\[
I_{10}=\frac{0-(-19.3)}{10}=1.93\text{ A}
\]

Current through 20 Ω branch:

\[
I_{20}=\frac{0-(-19.3)}{20}=0.965\text{ A}
\]

Total current:

\[
I = I_{10}+I_{20}=1.93+0.965=2.895\text{ A}
\]

\[
\boxed{I \approx 2.90\text{ A}}
\]

### (c)
Two series diodes in opposite directions block current in the middle branch, so only the 10 Ω resistor sets current:

\[
I=\frac{10}{10}=1\text{ A}
\]

\[
\boxed{I = 1.0\text{ A}}
\]

---

## 4) Chapter 2, Problem 11 (Boylestad)

### (a)
Top node = 1 V. Two parallel diodes: Si (0.7 V) and GaAs (1.2 V).
Si conducts first because it needs smaller forward voltage.

\[
V_o = 1 - 0.7 = 0.3\text{ V}
\]

\[
I=\frac{V_o}{1\,\text{k}\Omega}=\frac{0.3}{1000}=0.0003\text{ A}=0.3\text{ mA}
\]

**Answers:**
- \(\boxed{V_o \approx 0.30\text{ V}}\)
- \(\boxed{I \approx 0.30\text{ mA}}\)

### (b)
From +16 V down to \(V_o\), there are two forward Si drops:
- top Si: 0.7 V
- one of the parallel Si diodes: 0.7 V

\[
V_o = 16 - (0.7+0.7)=16-1.4=14.6\text{ V}
\]

Resistor is between \(V_o\) and \(-4\text{ V}\):

\[
I=\frac{V_o-(-4)}{4.7\,\text{k}\Omega}
=\frac{14.6+4}{4700}
=\frac{18.6}{4700}
=0.00396\text{ A}\approx 3.96\text{ mA}
\]

**Answers:**
- \(\boxed{V_o \approx 14.6\text{ V}}\)
- \(\boxed{I \approx 3.96\text{ mA}}\)
