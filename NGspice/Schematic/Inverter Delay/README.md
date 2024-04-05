# Output
- Commands in terminal
- 
# With Input Propagation Delay

-  Commands to check and obtain time delay of the inverter with input delay
```
  plot Vin Vout
  meas tran vin50 when vout=0.9 RISE=2
  meas tran vout50 when vout=0.9 FALL=2
  let tpHL=vout50-vin50
  print tpHL
```

# Without Input Propagation Delay

- To remove the input Propagation Delay, simply make the vin pulse faster with code for Vin
  
  ```
  name=Vin value="PULSE(0 1.8 0 0.1n 0.1n 3n 6.6n 5)" savecurrent=false
```