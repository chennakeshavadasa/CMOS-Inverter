# Output
- Commands in terminal
  
# With Input Propagation Delay

-  Commands to check and obtain time delay of the inverter with input delay
   ```
   plot Vin Vout
   meas tran vin50 when vin=0.9 RISE=2
   meas tran vout50 when vout=0.9 FALL=2
   let tpHL=vout50-vin50
   print tpHL
# Without Input Propagation Delay

![image](https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/065b0d5c-0373-4b6f-a143-a2135c3fc579)


- To remove the input Propagation Delay, simply make the vin pulse faster with code for Vin
  
   ```
    name=Vin value="PULSE(0 1.8 0 0.1n 0.1n 3n 6.6n 5)" savecurrent=false
-  Commands to check and obtain time delay of the inverter without input delay
     ```
       meas tran vin50 when vin=0.9 RISE=2
       meas tran vout50 when vout=0.9 FALL=2
       let tpHL=vout50-vin50
       print tpHL
- The Output I got
  ```
    ngspice 3 -> meas tran vin50 when vin=0.9 RISE=2
    vin50               =  6.650000e-09
    ngspice 4 -> meas tran vout50 when vout=0.9 FALL=2
    vout50              =  6.668350e-09
    ngspice 5 -> let tpHL=vout50-vin50
    ngspice 6 -> print tpHL
    tphl = 1.835000e-11
- Calculate Rise Time
  ```
      let vout10=1.8
      let vout90=1.6
      meas tran t10 when vout=.18 RISE=1
      meas tran t90 when vout=1.6 RISE=1
      let tr=t90-t10
      print tr    
- I got rise time(tr) = 3.477600e-11
 
- Calculate fall Time
  ```
      meas tran t10 when vout=.18 FALL=1
      meas tran t90 when vout=1.6 FALL=1
      let tf=t10-t90
      print tf
- I got fall time(tf) = 3.05029e-11
- Now to improve the design let us decrease the power consumption .
  - put VDD=1 and simulate the test bench
- Calculate rise time(tr)
   ```
      meas tran t10 when vout=.1 RISE=1
      meas tran t90 when vout=.9 RISE=1
      let tr=t90-t10
      print tr
 - We get rise time(tr)=6.006500e-11
- Now lets put VDD=1.8 again but increase W of PMOS and NMOS and increase the Power Consumption
  - put Wpmos=4u and Wnmos=2u
 - Calculate rise time(tr)
   ```
      meas tran t10 when vout=.18 RISE=1
      meas tran t90 when vout=1.6 RISE=1
      let tr=t90-t10
      print tr
  - We get rise time(tr)=3.460800e-11 which is close to 3.477600e-11, so there is not much difference because this unloaded device so we are gettiing same tr
# Loaded CMOS Inverter
 ![image](https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/c156fb0b-7c88-4b9e-86bb-99d5e44353dd)

 - Here we put Load Capacitance = 1pF and simulate it. But this results in output not settling so lets increase clock frequency at Vin
    ```
       name=Vin value="PULSE(0 1.8 0 0.1n 0.1n 10n 20n 10)" savecurrent=false
- Change code_show.sym transient analysis to
   ```
   .tran .02n 40n
- We get an Output some thing like this
  ![image](https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/96c46995-f369-448d-a502-6d45957a4607)

- For the same rise time commands ,We get rise time(tr) = 2.559230e-09
- Now do the same for a capacitance of 0.5pF
![image](https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/a623f563-9976-4636-bfc4-f84459db0c41)
- We get rise time(tr)=1.284700e-09
- Now lets increase the sie of NMOS and PMOS . Put Wpmos=8u and Wnmos=4u
 ![image](https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/02f126b3-fe33-49b5-a6f1-7fe312940b46)
- We get rise time(tr)=6.332000e-10

  
     


