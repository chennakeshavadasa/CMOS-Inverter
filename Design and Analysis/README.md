# Design and Analysis
This is the Analysis of CMOS Inverter

# Circuit
<p align="center">
  <img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/ae2d444a-fbad-47ab-8c0c-07a17661e63e" alt="CMOS Inverter">
</p>

# Basic Operation
- **Case 1: Vin=0 (logic 0)**
  - Here PMOS is ON (Saturation region) and acts as a Current Source.
  - NMOS is OFF (cutoff).
- **Case 2: Vin=VDD (logic 1)**
   - Here NMOS is ON (saturation region).
   - PMOS is OFF (cutoff).
 

# Switch Model

<p align="center">
<img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/b082889c-7a76-430e-9c53-3bf6c6993bd1" >
</p>

- The NMOS acts as a Open Circuit and PMOS acts as a resistor (short circuit for Ideal Case), this enables the Load Capacitor to get Charged with time constant(𝜏=RpCL).
- The PMOS acts as a Open Circuit and NMOS acts as a resistor (short circuit for Ideal Case), this enables the Load Capacitor to get Discharged with time constant(𝜏=RnCL).

# Voltage Transfer Characterisitics

![image](https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/5da41980-b9a1-412e-ae3a-b9e1e1d5d9b1

![image](https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/c222b0ed-ebcd-48e7-ae6b-91abc45dbc01)


<p align="center">
<img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/68744562-90b0-4a91-82fc-610fe2b8e783" >
</p>

# Major Issues 
- Noise Margin
- Inverter Delay
    - Propagation Delay
- How to Improve Design Technique ?
  - Reduce Load Capacitance
  - Increase Transistor sizing
  - Increase VDD (Power Consumption)
     
