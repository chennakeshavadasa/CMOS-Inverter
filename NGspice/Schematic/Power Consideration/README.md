# Power Calculations
![image](https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/5476131a-fafd-4381-b406-bbb76d836fea)

- To calculate power we need VDD and current drawn from VDD
- Here we donot need DC Analysis, so remove it and run transient analysis and bring back the Wpmos=2u and Wnm=1u
- To calculate the the Intermediate Power we need to calculate, so we Integrate Id from 20n to 40n and multiply with VDD(VDD=1.8) to obtain intermediate power.
- Command
 ```
    plot vout vdd#branch
    meas tran curr_inte integ vdd#branch from=20e-09 to=40e-09
    let power_inter=curr_inte*1.8
    print power_inter
    print power_inter/20e-09
 ```
- I got a power Consumption of 81.4848μW
- Here Layout is also very important to reduce the parascitic capacitance . which also has a big role in Power consumption
- So when i reduce Cload to 0.1pF
- ![image](https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/bd840170-6dbb-40a4-8cfb-e7eb66c499b3)
- We get a Power Consumption of 16.6695μW, which is a huge reduction compared to previous case
