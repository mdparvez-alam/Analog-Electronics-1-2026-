# Assignment 2.5 – Temperature Effects on Diode Behavior (1N4148)

## What I simulated
I used the same diode circuit (V1 → 1 kΩ → diode to ground) and ran a DC sweep from -2 V to +2 V.
I repeated the same sweep at two temperatures:
- 25°C
- 75°C

## What changed (observations)

### 1 Forward voltage (Vf)
At 75°C the diode conducts at a lower forward voltage than at 25°C.
This happens because increasing temperature increases the diode’s saturation current and carrier activity, so the diode needs less voltage to reach the same current.
As a result, the “turn-on” region shifts left (lower Vf) at higher temperature.

### 2 Reverse current (leakage)
At 75°C the reverse leakage current is noticeably higher than at 25°C.
This is because higher temperature generates more minority carriers in the junction, which increases leakage in reverse bias.

## Why this matters in real systems
Temperature changes can affect rectifiers, clamps, and protection diodes:
- Lower Vf at high temperature changes output voltage levels (e.g., rectifier DC output drops/rises slightly).
- Higher leakage at high temperature can cause unwanted standby current, measurement errors, or bias shifts in sensitive circuits.

