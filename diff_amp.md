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
     Vout= Av*(Vin1-Vin2)
     where Av is the gain of the differential amplifier.

- Common Mode Rejection Ratio (CMRR): 
   - This is the ability of the differential amplifier to reject common-mode signals. Common-mode signals are signals that appear identically on both inputs.
   - The ability of the amplifier to reject these common-mode signals is quantified by the CMRR. A high CMRR indicates that the amplifier is good at rejecting noise and unwanted signals that affect both inputs.

- Differential Gain and Common-Mode Gain:
   - The amplifier's differential gain is the gain for the difference between the two inputs. Ideally, the common-mode gain should be zero, meaning the amplifier only amplifies the difference and rejects common-mode signals.

- Biasing:
   - Proper biasing is crucial for the MOSFET differential pair to operate in the active region. This is typically done by the tail current source or other biasing circuitry.
   - If the biasing is not set correctly, the MOSFETs might not work efficiently, leading to signal distortion or improper operation.

### Design Considerations:
- Load Resistors: 
   - The choice of load resistors affects the output voltage swing and overall gain. In many designs, active loads are preferred because they provide better gain and allow for higher output impedance.

- Gain Setting:
   - The overall gain of the differential amplifier can be adjusted by the values of the load resistors or by using an additional amplification stage.

### Practical Applications:
- Operational Amplifiers (Op-Amps: The MOSFET differential pair is a core component in op-amps, where it forms the basis for differential signal amplification.
- Comparators: In analog-to-digital conversion, a MOSFET differential pair amplifier can be used in the input stage of a comparator to compare two input voltages and provide a digital output.
- Signal Processing: The differential pair is used in circuits that process differential signals, such as in instrumentation amplifiers and high-precision analog systems.

#### 1. Circuit Diagram:

```plaintext
                Vdd
                 |
                 |
                Rc      Rc
                 |       |
           +-----+-----+-----+
           |                 |
          (M1)               (M2)
           | \                | \
         Vg+  Vg-            Vg+  Vg-
           |                   |
           |                   |
          Rs                  Rs
           |                   |
          GND                 GND
```

In the above circuit:
- M1and M2 are the two MOSFETs that make up the differential pair.
- Vg1 and Vg2are the two input signals (differential inputs).
- Rss is the tail current source, which sets the total current for both MOSFETs.
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
Id1+Id2=Iss


\[
I_{\text{D1}} = \frac{I_{\text{tail}}}{2} \left( 1 + \frac{V_{\text{d}}}{V_{\text{T}}} \right)
\]

\[
I_{\text{D2}} = \frac{I_{\text{tail}}}{2} \left( 1 - \frac{V_{\text{d}}}{V_{\text{T}}} \right)
\]

where:
- **Vd** is the differential input voltage (**Vd = Vg+ - Vg-**),
- **VT** is the thermal voltage, typically around 26 mV at room temperature.

Thus, the current through each transistor is controlled by the differential input voltage.

#### 5. Output Voltage:

The output voltage is taken from the drain of **M1** or **M2**. If we consider the drain voltage of **M1**, the voltage drop across the load resistor **Rc** is:

\[
V_{\text{out1}} = V_{\text{DD}} - I_{\text{D1}} R_{\text{C}}
\]

Substituting for **I_D1**:

\[
V_{\text{out1}} = V_{\text{DD}} - \frac{I_{\text{tail}}}{2} \left( 1 + \frac{V_{\text{d}}}{V_{\text{T}}} \right) R_{\text{C}}
\]

The output voltage is therefore proportional to the differential input voltage **Vd**. The voltage gain of the amplifier is given by the derivative of the output voltage with respect to the differential input:

\[
A_v = \frac{V_{\text{out}}}{V_{\text{d}}}
\]

### 6. Common-Mode Rejection Ratio (CMRR):

A key feature of differential amplifiers is their ability to reject common-mode signals. The **CMRR** measures the ability of the amplifier to reject signals that are common to both inputs (i.e., the same signal appears on both **Vg+** and **Vg-**).

The **CMRR** is defined as:

\[
\text{CMRR} = \frac{\text{Differential Gain}}{\text{Common-Mode Gain}}
\]

In ideal conditions, the **common-mode gain** should be zero, meaning the amplifier does not respond to common-mode signals. In practice, the CMRR is finite and depends on the matching of the MOSFETs and the symmetry of the circuit.

### 7. Summary:

The **MOSFET differential pair amplifier** amplifies the difference between two input signals while rejecting common-mode signals. It works by splitting a tail current between two MOSFETs based on the difference in their gate-source voltages. The output is a voltage that is proportional to the differential input, and the gain of the amplifier depends on the tail current and load resistors. The differential pair is widely used in operational amplifiers and other circuits where precise, noise-immune amplification is needed.


