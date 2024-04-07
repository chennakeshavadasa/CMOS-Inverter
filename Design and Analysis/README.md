# Design and Analysis
This is the Analysis of CMOS Inverter

## Circuit
<p align="center">
  <img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/ae2d444a-fbad-47ab-8c0c-07a17661e63e" alt="CMOS Inverter">
</p>

## Basic Operation
- **Case 1: Vin=0 (logic 0)**
  - Here PMOS is ON (Saturation region) and acts as a Current Source.
  - NMOS is OFF (cutoff).
- **Case 2: Vin=VDD (logic 1)**
   - Here NMOS is ON (saturation region).
   - PMOS is OFF (cutoff).
 

## Switch Model

<p align="center">
<img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/b082889c-7a76-430e-9c53-3bf6c6993bd1" >
</p>

- The NMOS acts as a Open Circuit and PMOS acts as a resistor (short circuit for Ideal Case), this enables the Load Capacitor to get Charged with time constant(𝜏=RpCL).
- The PMOS acts as a Open Circuit and NMOS acts as a resistor (short circuit for Ideal Case), this enables the Load Capacitor to get Discharged with time constant(𝜏=RnCL).

## Voltage Transfer Characterisitics

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
- We only have those Voltages that are either low or either very high.

<p align="center">
<img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/68744562-90b0-4a91-82fc-610fe2b8e783" >
</p>

## Major Issues 
- Noise Margin.
- Inverter Delay.
    - Propagation Delay.
- How to Improve Design Technique ?
  - Reduce Load Capacitance.
  - Increase Transistor sizing.
  - Increase VDD (Power Consumption).

## Noise Margin 
<p align="center"> <img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/108fba64-167d-470e-b175-205537b823ca" > </p>

- We expect switching to happen somewhere near VDD/2, So Switching thereshold = VDD/2.
- NMH=Voh-Vil, For Ideal Case NMH=NML= VDD/2.
- We lower VDD, Noise margin will also be lower, so its property to reject noise will be compromised.

## Propagation delay

- We get tPHL= 0.69ReqnCL and tPLH= 0.69ReqpCL.
- Overall propagation delay = 0.69CL(Reqn+Reqp)/2.
- For tPHL=tPLH then Reqp=Reqn, but Reqp>Reqn. For tPHL=tPLH, we need to make width=3W, so Resistance reduces to Reqp so that Reqp=Reqn.
- For skewed transistor (tPHL=tPLH).
- Non skewed transistor (tPHL<tPLH).

## Capacitance that affect the design

- Gate drain Capacitance(Cgd12).
- Diffusion Capacitance(Cdb1,2).
- Wiring Capacitance(Cw).
- Gate Capacitance of fanout(Cg3,4).

## How to improve design 

- Reduce CL.
- Increase transistor sizing.
- Increase VDD.

## Optimal value of NMOS to PMOS Ratio

- While improving the PMOS width improves tPLH of the inverter by increasing the charging current, it also degrades the charging current. It degrades the tPHL by causing a large parascitic Capacitance.
- β=Wp/Wn.
- We get βopt=sqrt(r(1+ Cw/(Cdn1+Cdn2))), where r=Reqp/Reqn.

## Sizing of Inverter Chain

- <p align="center"> <img src="https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/73541ee4-93ed-40fd-97ee-ae7167a64777" > </p>
- For an Inverter CL= Cint+Cext.
- tp=tp0(1+Cext/Cint), where tp0=0.69ReqCint.
- We have tp=tp0(1+f/γ), where γ= proportional constant and f=Cext/Cint.
- the delay of the inverter is a function of the ratio between external load capacitor and its intrinsic capacitance.
- Cg,i=sqrt(Cg,j+1 * Cg,j-1)
- The optimum size of each inverter is the geometric mean of its neighbour.
- tp=Ntp0(1+(f/γ)^1/n)
