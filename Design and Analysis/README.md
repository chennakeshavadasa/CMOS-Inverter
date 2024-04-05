# Design and Analysis
This is the Analysis of CMOS Inverter

# Circuit
<p align="center">
  <img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/ae2d444a-fbad-47ab-8c0c-07a17661e63e" alt="CMOS Inverter">
</p>

# Basic Operation
- **Case 1: Vin=0**
  - Here PMOS is ON (Saturation region) and acts as a Current Source.
  - NMOS is OFF (cutoff).
  - The NMOS acts as a Open Circuit and PMOS acts as a resistor (short circuit for Ideal Case), this enables the Load Capacitor to get Charged with time constant(𝜏=RpCL).
- **Case 2: Vin=VDD**
   - Here NMOS is ON (saturation region).
   - PMOS is OFF (cutoff).
  - The PMOS acts as a Open Circuit and NMOS acts as a resistor (short circuit for Ideal Case), this enables the Load Capacitor to get Discharged with time constant(𝜏=RnCL).
     
