# Power Calculations
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
- here Layout is also very important to reduce the parascitic capacitance . which also has a big role in Power consumption
