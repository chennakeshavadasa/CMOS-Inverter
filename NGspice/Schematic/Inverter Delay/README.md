![image](https://github.com/chennakeshavadasa/CMOS-Inverter/assets/123294639/f0cabbb6-fb97-4fd2-b6b6-97a2037fb1a0)# Output
- Commands in terminal
# With Input Propagation Delay
` plot Vin Vout
  meas tran vin50 when vout=0.9 RISE=2
  meas tran vout50 when vout=0.9 FALL=2
  let tpHL=vout50-vin50
  print tpHL
