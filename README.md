# LIC EXPERIMENT 1
## DC, Transient and AC analysis of Common Source Amplifier Using LTspice
### Components :
#### n-mosfet(180nm technology node), Resistor-1k,Voltage source(1.8V, 0.9 V),AC ground,wires

### Circuit diagram 1:
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
  ![Image](https://github.com/user-attachments/assets/5c05fc11-f7d5-4155-a6c6-9ef7cabe6c2d) 
Here, keep sinusoidal signal dc offset as 0.8 V ,amplitude as 50 mV, frequency as 1kHz, AC amplitude as 1 V. In configure analysis, set stop time as 3m seconds.
3. AC ANALYSIS:

![acnew](https://github.com/user-attachments/assets/587a8ce2-4ef2-49b6-a335-d9527282b792)
Gain =2 dB
Set type of sweep as decade,number of points per decade as 20,start and stop frequency as 0.1 Hz and 1T Hz to get expected response.
### Inference :
1. To get the desired drain current,we changed the channel width which is directly proportional to drain current.
2. DC analysis gives the dc operating point and checks whether the mosfet is in saturation region or not.
3. For time varying AC signal,transient analysis shows the characteristics of the mosfet.
4. Gaain and frequency is found by AC analysis.


### Circuit diagram 2:
![sim0](https://github.com/user-attachments/assets/a09f8fcb-68e4-48f5-87ee-3f7c23cc5f99)

### Components:
NMOSFET,PMOSFET,Voltage supply,AC ground,wires.

### Theory:
A CS amplifier with NMOS and PMOS works like a CMOS inverter. NMOS pulls output low, PMOS pulls output high giving high gain. Both the mosfets conduct to amplify signals.A NMOS amplifier's gain is improved by PMOS load.This circuit design gives high gain and better efficiency.
DC ANALYSIS:
In DC analysis of a CS amplifier, we find the Q point. The gate voltage Vg controls the transistor's mode. DC biasing network sets Vgs for proper operation.The drain current is determined by Vgs and other device parameters.
TRANSIENT ANALYSIS:
In transient analysis, a changing input modulates Vgs, altering Id.This creates an inverted and amplified output.
AC ANALYSIS:
In AC analysis, small signal input causes Vgs variations,changing Id.This creates an inverted and amplified output at the drain. Gain depends on the transconductance Gm and load resistance.

### Procedure :
1. Create a Folder
Make a new folder and save the given library file (tsmc018 (1).txt) and your LTspice file in it.
2. Import the Library File
Open LTspice and use the .include SPICE directive to import the library file.
3. Set Up the Transistors
Use CMOSP for the PMOSFET and CMOSN for the NMOSFET, as per the library file.
Set L = 180nm and W = 1µm for both transistors.
4. Diode-Connect the PMOSFET
Connect the PMOSFET in a diode configuration (Gate tied to Drain) to ensure it stays in saturation.
5. Apply Circuit Voltages
Set VDD = 1.8V and VGS(NMOS) = 0.7V.
6. Calculate Drain Current
Find the expected drain current for the given power rating and adjust the transistor width to match this value.
7. DC Analysis
Perform a DC sweep to get a list of values for different circuit conditions and verify the drain current
8. Transient Analysis
Set DC offset = 0.9V, Amplitude = 50mV, Frequency = 1kHz, and Stop time = 3ms to observe the transient response.
9. AC Analysis
Perform an AC sweep (Decade type, 20 points per decade, frequency range 0.1Hz to 1THz) to obtain the AC response.
10. Run and Analyze Results
Execute all simulations and verify that the results match expected values, adjusting transistor width if needed.

### Calculation :
Take power as 100 uW 
P=VI,where V= 1.8 V 
Id will be 55.5 uA
From KVL, VDD = IdRd + Vout
Rd = 1 k ohm
therefore Vout = 1.745 V
Q point will be (Vds,Id)=(1.745 V, 55.5 uA)

### Simulation results:
1. DC ANALYSIS:
   ![sim1](https://github.com/user-attachments/assets/c2aab848-4340-4c9c-85be-84e64c99d34e)
M1 Width = 300nm
M2 Width= 590nm
Length of M1 and M2 is 180nm
3. TRANSIENT ANALYSIS:

![SAP](https://github.com/user-attachments/assets/348ef544-c748-4691-ae13-5c3cabad397b)
Amplitude of Output peak voltage =92.8 mV
Amplitude of input peak voltage = 50mV
Gain=1.84 
Here, keep sinusoidal signal dc offset as 0.8 V ,amplitude as 50 mV, frequency as 1kHz, AC amplitude as 1 V. In configure analysis, set stop time as 3m seconds.
3. AC ANALYSIS:
![sim3](https://github.com/user-attachments/assets/e8a98f08-5f6f-4f51-8226-0a733f72f45a)
Gain=6.4 dB
Set type of sweep as decade,number of points per decade as 20,start and stop frequency as 0.1 Hz and 1T Hz to get expected response.
### Inference:
1. A diode connected mosfet operates in saturation region typically.
2. The drain current depends on the mosfet's width, other parameters kept constant.
3. DC analysis determines op pnt and confirms saturation mode.
4. Transient analysis shows the response of the mosfet to time varying signals.
5. AC analysis gives information about gain and frequency.

   ### Conclusion:
   Larger Output Swing: Allows better utilization of the supply voltage, enabling a wider output range.

Using a PMOS active load provides self-biasing, making the circuit more stable compared to using a resistor.

Lower Power Consumption: Reduces power dissipation compared to using a resistor.

Replacing a resistor with a PMOS active load significantly improves gain, power efficiency, and frequency response, making it the preferred choice in integrated circuit (IC) amplifiers.

   
