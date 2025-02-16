# LIC EXPERIMENT 1
## DC, Transient and AC analysis of Common Source Amplifier Using LTspice
### Components :
#### n-mosfet(180nm technology node), Resistor-1k,Voltage source(1.8V, 0.9 V),AC ground,wires

### Circuit diagram :
![Image](https://github.com/user-attachments/assets/19efe59d-ee91-4130-871f-cfc8a93bc041)

### Theory :
Common source amplifier is a basic transistor amplifier circuit. It provides hoigh voltage gain with 180 phase shift. The input is at the gate or base, the output is from the drain or collector.It has high input impedance and moderate output impedance. It is used in audio, RF,and signal processing applications.
DC ANALYSIS:
DC analysis of a CS amplifier determines the operating point by analysing the network. It involves solving for Vgs, Id,Vds, using kirchhoff's voltage law to ensure that the mosfet operates in saturation region for amplification.
TRANSIENT ANALYSIS :
Transient analysis of a CS amplifier is nothing but knowing its response to time varying signals. It checks how capacitors, resistors, and transistors affect signal propagation, rise time, settling behavior. This analysis helps to determine the bandwidth, stability, and distortion.
AC ANALYSIS :
AC analysis of a CS amplifier determines gain, bandwidth, impedance using small signal models considering Gm, Rds for frequency response.

### Procedure :
1. Build the common source amplifier circuit as the circuit diagram using LTspice.
2. Set the Resistor value as 1K, DC voltage as 1.8V, Gate voltage as 0.9V.
3. Download the library file tsmc018 (1).txt
4. Create a folder. Save the library file and LTspice file to the folder.
5. Import the library file to LTspice using spice directive(.op).
6. Set the mosfet model name CMOSN as given in the library file, length as 180nm, width as 1uF.
7. Find the current value for the given power rating.
8. DC analysis: In edit simulation option, change to dc offset to get list of values obtained from the circuit. We should get the calculated current value in the simulation result.So that we need vary the value of width since width is directly proportional to Drain current(Id) keeping other parameters constant.
9. Transient analysis: In edit simulation option, change from dc offset to transient. Set the dc offset as 0.9V, Amplitude 50mV, frequency 1KHz. Keep stop time for 3ms and run to get the expected waveform.
10. AC analysis : In edit simulation option, change from transient to ac analysis. Set type of sweep as decade, number of points per decade as 20, start and stop frequency as 0.1Hz and 1THz to get the expected ac waveform.

### Calculation :
Take power as 100 uW 
P=VI,where V= 1.8 V 
Id will be 55.5 uA
From KVL, VDD = IdRd + Vout
Rd = 1 k ohm
therefore Vout = 1.745 V
Q point will be (Vds,Id)=(1.745 V, 55.5 uA)

### Simulation results :
1. DC ANALYSIS :
![Image](https://github.com/user-attachments/assets/8d00be35-329d-438d-976e-ef18719ff9ff)
 Id = 55.5 uA
 Width = 0.203 um
 Vout = 1.745 V
 DC op pnt is (1.745 V, 55.5 uA)
   
2. TRANSIENT ANALYSIS:
   

