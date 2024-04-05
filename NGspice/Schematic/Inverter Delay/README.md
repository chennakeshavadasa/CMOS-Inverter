# Output
- Commands in terminal
# With Input Propagation Delay

-  Commands to check and obtain time delay of the inverter with input delay
```
  plot Vin Vout
  meas tran vin50 when vout=0.9 RISE=2
  meas tran vout50 when vout=0.9 FALL=2
  let tpHL=vout50-vin50
  print tpHL
