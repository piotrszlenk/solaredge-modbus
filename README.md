# solaredge-modbus

## Intro
This is an example configuration for SolarEdge integration with Home Assistant via modbus TCP. To receive a final value of some registers (i.e. output AC power) they need to be scaled and multiplied by a scale factor which is stored under different register. In order to make sure that the final value is correct both registers must be read during one modbus transaction. Otherwise it may happen that the value of scale factor changes between two transactions, hence giving wrong final value.