# BMSIMDShutdownCircuit

Gautham Sathyanarayanan

This concept was a project designed for Rutgers Formula SAE.

The Shutdown circuit of a car is a series of switches that
must all be closed for the car to be on at any time. Therefore,
if one of the switches is not closed, no current will be allwoed to
flow to the car functions. 

Two components, the Battery Managment System(BMS), and Insulation 
Monitoring Device(IMD) are two monitors that make sure that the
accumulator( main high voltage battery pack) is separate from 
the chassis ground and low voltage systems. The BMS monitors
the voltage, current, and temperature of each battery in the accumulator 
and actively balances the cells when charging whilst also monitoring its own status.

When either fail or detect a fault signal, the shutdown circuit must 
be opened, and an LED blinker must show that the car is not 
ready to drive. Additionally, the fault must be shown to the 
driver. When the car is in a latched state of failure, someone
external to the car must be able to reset the failure state. 
Consequently, if the systems are all good, a green light should be illuminated.

The circuit to implement this process was not permitted 
to use programmable chips and was done in all analog components
and ICs.

The LEDs were all attached to the respective fault signals as 
shown in the schematic. When a fault signal was received,
the signal was latched with an or gate that caused a 
n-channel MOSFET to connect the shutdown circuit to ground, 
thereby opening the circuit. A 555 timer was used for 
the red blinker.
