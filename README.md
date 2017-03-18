# sensortag.powerDevPack

Devboard for adding lipo battery. It features battery charger through micro USB, high efficiency DCDC regulator and UART to USB converter through a FTDI chip. 

It has been designed for cc2650 sensorTag, but it should work also with the other versions till the so called "SKIN" connector keeps the same pinout settings.
The output voltage is fixed by the DCDC to 3.75 volt, it can be reduced acting on the values of RTPS1, RTPS2 and RTPS3. See TPS62737 datasheet for details.
Note that the AON battery monitor won't work because of the DCDC. The battery voltage can be measured usign the appropriate circuit on the powerDevBoard. To activate it set DP2 pin to 'HIGH', then read analog voltage at DP3 pin. The actual battery voltage is twice the voltage measured at DP3. The battery measurement circuit absorbs about 10uA from the battery, when not used set DP2 to "LOW".
