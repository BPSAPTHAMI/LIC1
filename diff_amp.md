# MOSFET DIFFERENTIAL PAIR AMPLIFIER

### MOSFET Differential Pair Amplifier Circuit:
A MOSFET differential pair amplifier is a fundamental building block in analog circuit design, widely used in operational amplifiers (op-amps), comparators, and other signal-processing circuits. It's used for amplifying the difference between two input signals. The differential amplifier amplifies the voltage difference between two input terminals while rejecting any common-mode signals (signals that are common to both inputs). This makes it ideal for applications where the signal is small and needs to be extracted from noise, which might affect both inputs equally.

### Key Components and Operation:

1. MOSFETs:
   - The differential pair consists of two MOSFETs (Metal-Oxide-Semiconductor Field-Effect Transistors), typically n-channel MOSFETs are used.
   - These two MOSFETs are configured so that the drains are connected to the same load resistor or current source, while the gates are the inputs for the differential signals.

2. Input Differential Signals:
   - The two input signals, Vin1 and Vin2, are fed into the gates of the two MOSFETs.
   - The idea is to amplify the voltage difference between Vin+ and Vin-, while rejecting any signals that are the same for both inputs (the common-mode signal).

3. Current Source or Tail Current:
   - A constant current source is typically placed at the source terminals of the two MOSFETs. This current source sets the tail current, which is shared by both MOSFETs.
   - The current through the differential pair is fixed, and it is split between the two transistors based on the voltage difference at the gates (the input signals).
   - The total current through the pair remains constant, but the individual MOSFETs conduct different amounts of current depending on the differential input signal.

4. Operation of the Differential Pair:
   - When the input voltages are equal (Vin1 = Vin2), both MOSFETs conduct the same amount of current, and no voltage difference appears across the load resistors.
   - When the input voltages are different (Vin1 ≠ Vin2), the MOSFET with the higher input voltage will conduct more current, while the other will conduct less. This current imbalance creates a voltage difference across the load resistors, which is the output of the amplifier.
   - The output voltage is proportional to the difference between the two input voltages, hence the ckt is called as "differential amplifier."

5. Output:
   - The output is typically taken from the drain of one or both of the MOSFETs.
   - The voltage at the drain of the MOSFET that conducts more current will be lower, while the voltage at the drain of the other MOSFET will be higher, assuming the load resistors are in place.
   - The overall output can be given by the equation:
     - Vout= Av*(Vin1-Vin2)
     where Av is the gain of the differential amplifier.

- Common Mode Rejection Ratio (CMRR): 
   - This is the ability of the differential amplifier to reject common-mode signals. Common-mode signals are signals that appear identically on both inputs.
   - The ability of the amplifier to reject these common-mode signals is quantified by the CMRR. A high CMRR indicates that the amplifier is good at rejecting noise and unwanted signals that affect both inputs.

- Differential Gain and Common-Mode Gain:
   - The amplifier's differential gain is the gain for the difference between the two inputs. Ideally, the common-mode gain should be zero, meaning the amplifier only amplifies the difference and rejects common-mode signals.

- Biasing:
   - Proper biasing is crucial for the MOSFET differential pair to operate in the active region. This is typically done by the tail current source or other biasing circuitry.
   - If the biasing is not set correctly, the MOSFETs might not work efficiently, leading to signal distortion or improper operation.


#### 1. Circuit Diagrams:
##### Differential pair amplifier with resistor Rss
![Image](https://github.com/user-attachments/assets/1bc99cbd-3bbf-4b53-ae17-f8eff2eb6f64)
##### Differential pair amplifier with current source Iss
![Image](https://github.com/user-attachments/assets/edee8873-0136-40a9-ae43-f50798b9c9c8)
##### Differential pair amplifier with nMOS
![Image](https://github.com/user-attachments/assets/7628e4b4-c367-473f-891f-bb3fb2566847)

In the above circuits:
- M1and M2 are the two MOSFETs that make up the differential pair.
- Vin1 and Vin2are the two input signals (differential inputs).
- Iss is the tail current source, which sets the total current for both MOSFETs.
- Rd are the load resistors connected at the drains of the MOSFETs.
- The output is typically taken from the drain of either M1 or M2.
- Vdd is the supply voltage.

#### 2. Operation of the Differential Pair:
The differential amplifier amplifies the difference between the two input signals Vg1 and Vg2. The total current flowing through the differential pair is set by the tail current source. 
- If Vg1 = Vg2, the currents in both MOSFETs M1 and M2 will be equal, meaning both MOSFETs conduct half of the total current, and no voltage difference appears at the output.
- If Vg1 ≠ Vg2, the current through one MOSFET will increase, while the current through the other will decrease, creating a voltage difference at the output.

#### 3. Mathematical Analysis:
Assume that both MOSFETs M1 and M2 are identical and operating in the saturation region.
- The drain current for each MOSFET is given by:
  
       Id1=1/2 Kn(Vgs1-Vth)^2
where:
- Kn is transconductance parameter
- Vgs1 is the gate-source voltage of MOSFET M1
- Vth is the threshold voltage

- For M2,
   
        Id2=1/2 Kn(Vgs2-Vth)^2

- Vgs1 = Vg1-Vs1 for MOSFET M1
- Vgs2 = Vg2-Vs2for MOSFET M2
- where Vs is the source voltage

#### 4. Current Division:
The total tail current Iss is split between the two MOSFETs in proportion to the difference in their gate-source voltages. 
- Id1+Id2=Iss
the current through each transistor is controlled by the differential input voltage Vid=Vin1-Vin2

#### 5. Output Voltage:
The output voltage is taken from the drain of M1 or M2. If we consider the drain voltage of M1, the voltage drop across the load resistor Rd is given by:
- Vout = Vdd-Id1*Rd

The output voltage is therefore proportional to the differential input voltage Vid. The voltage gain of the amplifier is given by the derivative of the output voltage with respect to the differential input.
- Av=Vout/Vid

### 6. Common-Mode Rejection Ratio (CMRR):
A key feature of differential amplifiers is their ability to reject common-mode signals. The CMRR measures the ability of the amplifier to reject signals that are common to both inputs (i.e., the same signal appears on both Vgs1 and Vgs2).

The CMRR is defined as:
- CMRR = Differential Gain/Common-Mode Gain

In ideal conditions, the common-mode gain should be zero, meaning the amplifier does not respond to common-mode signals. In practice, the CMRR is finite and depends on the matching of the MOSFETs and the symmetry of the circuit.


### 7. Definitions
- Common-mode input voltage:
  - VinCM=Vin1+Vin2
  
- Gate-source voltage:
  - Vgs=Vg-Vs
  
- Overdrive voltage:
  - Vov = Vgs - Vth  
where:
- Vg is the gate voltage.
- Vs is the source voltage.
- Vth is the MOSFET threshold voltage.

### 8. Relationship Between VinCM,Vgs and Vov
The source voltage Vs is determined by the current source Iss in the tail of the differential pair:
Vs = Vee + VssRs
where Vee is the 
For matched transistors, both MOSFETs have the same Vgs, so we can express it in terms of VinCM:

- Vgs = VinCM - Vs

- Vov = (VinCM-Vs) - Vth

- Vov = (VinCM-(Vee + VssRs)) - Vth
This equation shows how the common-mode input voltage affects the overdrive voltage, which in turn influences transistor operation.

### 9. Common-Mode Input Voltage Range
For proper operation, the MOSFETs must operate in saturation.
- Vds > Vov

The source voltage is:
- Vs = Vee + VssRs

Thus, the upper limit on VinCM occurs when the MOSFET enters the triode region:
- VinCMmax = Vdd - Vov

The lower limit occurs when the source voltage reaches a point where the transistors turn off:
- VinCMmin = Vs + Vth

### 10. Source Voltage and Its Dependence on VinCM:
Since the tail current source Iss is shared between both transistors, the source voltage Vs is influenced by VinCM:
- Vs = Vee+ (Iss/2*Rs)
- Vgs = VinCM - (Vee + (Iss/2*Rs))
- Vov = Vgs-Vth
- Vov = (VinCM - (Vee + (Iss/2*Rs))) -Vth
 This shows that Vov increases with VinCM

### 11. Key Insights
- Higher VinCM increases Vgs, leading to higher Vov.
- if VinCM is too high, transistors leave saturation and enter triode mode.
- if VinCM  is too low, the transistors may turn off.

## Design Question:
Design and analyse the differential amplifier for the following specifications.
Vdd=2.2V, P<=2.2mW, VinCM=1.2 V, VoCM=1.25V, Vp=0.4V
Perform DC analysis,transient analysis, frequency analysis and extract the parameters.
- VinCM = Vp + Vgs1
  - 1.2 = 0.4 + Vgs1
  - Vgs1 = 0.8V

- Assume Vth = 0.36 V
  - Vov = Vgs - Vth
  - Vov = 0.8 - 0.36
  - Vov = 0.44 V
    
- Iss=P/Vdd
  - Iss = 2.2mW/2.2V
  - Iss = 1mA
    
- Id1 = Id2 = Iss/2 = 0.5mA
 
- Rss = Vp/Iss
  - Rss = 0.4V/1mA
  - Rss = 0.4k ohm
 
- Vo1 = Vdd - Id*Rd
  - 1.25V = 2.2 - (0.5m) Rd
  - Rd = 1.9 k ohm

- gm = 2Id/Vov
  - gm = (2*0.5m)/0.44
  - gm = 2.27 mS

- Av = -gm*Rd
  - Av = -(2.27m)(1.9k)
  - Av = -4.31 V/V
    
### Design Considerations:
- Load Resistors: 
   - The choice of load resistors affects the output voltage swing and overall gain. In many designs, active loads are preferred because they provide better gain and allow for higher output impedance.

- Gain Setting:
   - The overall gain of the differential amplifier can be adjusted by the values of the load resistors or by using an additional amplification stage.


## Analysis of differential pair amplifier with resistor Rss as load:
### DC ANALYSIS:
- Connect the components as per the circuit diagram.
- Calculated Rd and Rss values are set to keep the transistors in saturation region.
- Rd=1.9 k ohm,Rss=0.4 k ohm
- To get the required VoCM as 1.25 V,vary the W/L of M1 and M2.
![Image](https://github.com/user-attachments/assets/7b22dcfe-1eae-4461-ab5f-8813790c97d4)
- L = 180 nm, W = 6.4125 um for both transistors M1 and M2.
- Q point (Vds,Id)=(0.85 V,0.5 mA)
- VinCMmin= Vth+Vp= 0.895 V
- VinCMmax= Vdd- (Id*Rd) + Vth= 1.745 V
- VoutCMmin= Vov1 +Vov3=0.705 V
- VoutCMmax= Vdd- (Id*Rd)=1.25 V

- Spice output  log:
- Check all the necessary device parameters and voltage conditions in spice error log.
![Image](https://github.com/user-attachments/assets/dba220c2-e972-4a8b-9def-27d0aba2bdcb)
- Vgs=0.8 V , Vds= 0.85 V , Vth=0.495 V
- Vgs > Vth, Vds > Vov
- Therefore, transistors M1 AND M2 lie in saturation region.

  
### Transient Analysis:
Input and output waveforms of M1:
![Image](https://github.com/user-attachments/assets/ecee44f1-1a85-4d46-9747-2922d181790d)
Input and output waveforms of M2:
![Image](https://github.com/user-attachments/assets/36bd8049-fa85-4208-b0d4-a03b76242e67)
Both:
![Image](https://github.com/user-attachments/assets/e787a9c0-6c71-487e-a9c2-7d6ca4f4e18e)
Transient gain:
![Image](https://github.com/user-attachments/assets/7164147d-327a-41a5-97a8-5d98bdecfc87)
 From simulation, Gain= -4.011 V/V
 Theoretical gain= -4.31 V/V

 
### AC Analysis:
Input and output waveforms of M1:
![Image](https://github.com/user-attachments/assets/1c372a2f-4ecf-4b09-b0e7-c26fffd89937)
Input and output waveforms of M2:
![Image](https://github.com/user-attachments/assets/5a29456e-225d-406d-a1d0-fc0fcb703400)
Both:
![Image](https://github.com/user-attachments/assets/c4d09f12-da60-4066-8c8d-be56b60be21d)
 From simulation, Gain= 12.145 dB
 Theoretical gain= 12.68 dB


## Analysis of differential pair amplifier with current source Iss as load:
### DC Analysis:
- Replace the load resistor Rss by a current source Iss.
- Set the theoretical value of Iss, which is 1 mA.
- Rd=1.9 k ohm
- L = 180 nm, W = 6.4125 um for both transistors M1 and M2.
![Image](https://github.com/user-attachments/assets/a6481fc7-8c0d-4de1-b829-3fc921585bce)
  Spice output log:
![Image](https://github.com/user-attachments/assets/b0552a2b-4d85-482b-8a07-593481e0b258)
- Check all the necessary device parameters and voltage conditions in spice error log.
- Vgs=0.8 V , Vds= 0.85 V , Vth=0.495 V
- Vgs > Vth, Vds > Vov
- Therefore, transistors M1 AND M2 lie in saturation region.

### Transient Analysis:
Input and output waveforms of M1:
![Image](https://github.com/user-attachments/assets/5b13f2ba-5109-4422-a345-74ced121b61e)
Input and output waveforms of M2:
![Image](https://github.com/user-attachments/assets/0a3fd2ab-500a-4341-a816-6a9d22006ea0)
Both:
![Image](https://github.com/user-attachments/assets/6feb22be-bfeb-45c0-bda5-3be4c1f415f7)
Transient gain:
![Image](https://github.com/user-attachments/assets/03f479e0-2c71-41b8-a0e9-82978bf9d5ca)
 From simulation, Gain= -4.011 V/V
 Theoretical gain= -4.31 V/V

### AC Analysis:
Input and output waveforms of M1:
![Image](https://github.com/user-attachments/assets/fd7404cd-fb30-43b9-8a4c-2e2e414de65b)
Input and output waveforms of M2:
![Image](https://github.com/user-attachments/assets/8724a273-4048-4180-98d1-81f300982c0f)
Both:
![Image](https://github.com/user-attachments/assets/d7a85b6e-047f-4b34-b86d-2aa8f8de21f5)
 From simulation, Gain= 12.145 dB
 Theoretical gain= 12.68 dB


## Analysis of differential pair amplifier with nMOSFET as a current source(load) :
### DC Analysis:
- Replace the current source Iss by a nMOS transistor M3.
- Connect a voltage source Vb(biasing voltage) which is 0.76 V, to the gate terminal of M3.
- Vb= Vp + Vth = 0.4 + 0.36 = 0.76 V.
- Rd=1.9 k ohm
- L = 180 nm, W = 6.4125 um for transistors M1,M2 and M3.
![Image](https://github.com/user-attachments/assets/56411f98-e16f-448f-8716-625745a2a0fa)
Spice output  log:
![Image](https://github.com/user-attachments/assets/0780118a-00ce-47a1-8a6b-f7e7cf808a9b)

  - Q point variation can be seen here.
  - To set the Q point , changed the channel width of M3.
  -  L = 180 nm, W = 40.1785 um
![Image](https://github.com/user-attachments/assets/7494297b-fc13-4396-8437-9cf8ed7fd00e)
Spice output log:
![Image](https://github.com/user-attachments/assets/c892ef20-e805-4363-bb67-b1cba15a7ba5)

### Transient Analysis:

Input and output waveforms of M1:
![Image](https://github.com/user-attachments/assets/9a3b8925-d46e-415e-b5b4-36ef291e9b92)
Input and output waveforms of M2:
![Image](https://github.com/user-attachments/assets/bd8683fa-f285-439e-8386-6f1ff90e735b)
Both
![Image](https://github.com/user-attachments/assets/357ad05a-aa8c-4da2-8746-a7764d138441)
Transient gain:
![Image](https://github.com/user-attachments/assets/a07ac687-6d82-440c-87b6-2ff10b5ff748)
From simulation, gain=-8.68 V/V
Therefore, gain is more in this case than the previous cases(-4.31 V/V)

### AC Analysis:
Input and output waveforms of M1:
![m3 ac m1](https://github.com/user-attachments/assets/f2b649d5-0a89-4fa9-b970-c63f0411295a)
Input and output waveforms of M1:
![m3 ac m2](https://github.com/user-attachments/assets/40622e89-ce78-40bf-a4e7-07dc21144e6e)
Both:
![m3 ac gain](https://github.com/user-attachments/assets/62caf00d-b1b7-47ae-ba04-eb49dd8ad2c0)
From simulation, Gain=19.400 dB
Therefore, gain is more in this case than the previous cases(12.68 dB)

### Tabular column:

### Inference:
### Practical Applications:
- Operational Amplifiers (Op-Amps): The MOSFET differential pair is a core component in op-amps, where it forms the basis for differential signal amplification.
- Comparators: In analog-to-digital conversion, a MOSFET differential pair amplifier can be used in the input stage of a comparator to compare two input voltages and provide a digital output.
- Signal Processing: The differential pair is used in circuits that process differential signals, such as in instrumentation amplifiers and high-precision analog systems.


