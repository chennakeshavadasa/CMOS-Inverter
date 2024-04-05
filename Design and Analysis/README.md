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

<p align="center">
  <img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/052cf4eb-2f2d-4577-a5fb-3aba90e9d915" alt="Image 1">
</p>

- Here ID is mirroring around X axis


<p align="center">
  <img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/48467720-c38e-406b-bbae-a554bcea6e32" alt="Image 2">
</p>

- Here ID is horizontally Siftef over VDD

- Governing Equation
  - IDSp = -IDSn
  - VGn = Vin
  - VGSp = Vin - VDD
  - VDSn = Vout
  - VDSp = Vout - VDD

<p align="center">  
<img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/ae06ad2f-b02c-4b87-90cf-5a58bb5e5385" >
</p>
- The points where both NMOS ans PMOS Voltages will be same , the current will also be same in magnitude with relation IDSp = -IDSn

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
     
