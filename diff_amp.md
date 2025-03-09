# MOSFET DIFFERENTIAL PAIR AMPLIFIER
### A "MOSFET Differential Pair Amplifier" is a core element of many analog circuits, particularly in the design of operational amplifiers (op-amps) and other analog signal processing systems. The differential pair is designed to amplify the difference between two input signals while rejecting any common-mode signals (those that appear identically at both inputs). This makes it an essential building block for high-performance analog circuits where precision and noise rejection should take place.

## Basic Structure of a MOSFET Differential Pair**

A MOSFET differential pair typically consists of two **MOSFETs (Metal-Oxide-Semiconductor Field-Effect Transistors)** with their gates connected to two input signals. The source terminals of the two MOSFETs are usually connected to a common current source or current mirror. The drains of the MOSFETs are connected to a load resistor or active load, and the output is taken from the drain of one or both of the MOSFETs. The configuration looks like this:

```
       Vdd
         |
         |
       [R_D]
         |
         |---- Vout (1)
         |
    Drain |----|---- Vout (2)
           M1   M2
           |    |
   Vin1----|    |---- Vin2
           |    |
          [I]  [I]
           |    |
          Vss  Vss
```

- **M1 and M2**: These are the two MOSFETs in the differential pair.
- **R_D**: The load resistor connected to the drain of the MOSFETs.
- **Vout(1)** and **Vout(2)**: Output voltages taken from the drains of M1 and M2.
- **I**: The current source or current mirror that provides a constant current to the differential pair.

### 2. **How a MOSFET Differential Pair Works**

The operation of a MOSFET differential pair can be understood in terms of how the currents through the MOSFETs respond to the input signals and the overall current that is shared between the two transistors.

#### a) **Input Signals**:

The input signals \( V_{in1} \) and \( V_{in2} \) are applied to the gates of MOSFETs M1 and M2, respectively. These are the differential input signals, and the circuit amplifies the difference between them. The source terminals of both MOSFETs are connected to a common current source or current mirror that provides a constant current, denoted \( I_{bias} \).

#### b) **Differential Operation**:

The basic idea is that the current \( I_{bias} \) is shared between the two MOSFETs. When the input voltages change, the MOSFETs adjust the current flowing through them, thus amplifying the difference between the two input signals.

- When \( V_{in1} \) increases, it causes M1 to conduct more current, and M2 to conduct less.
- When \( V_{in2} \) increases, the reverse happens: M2 conducts more, and M1 conducts less.

This results in a varying current through each MOSFET that is dependent on the difference between the two input voltages, \( V_{in1} - V_{in2} \). In an ideal differential pair, the current split is perfectly balanced, and only the difference in input voltages causes a current imbalance.

#### c) **Output**:

The output voltage of the differential pair can be taken from the drains of the MOSFETs. The output voltage is related to the current flowing through each MOSFET and the load resistor \( R_D \).

- For example, the output voltage at the drain of M1 can be expressed as:
  
  \[
  V_{out1} = V_{DD} - I_{D1} R_D
  \]
  
  where \( I_{D1} \) is the drain current of M1, and \( R_D \) is the load resistor.

- Similarly, the output at the drain of M2 can be written as:
  
  \[
  V_{out2} = V_{DD} - I_{D2} R_D
  \]
  
  where \( I_{D2} \) is the drain current of M2.

The difference in the drain currents \( I_{D1} - I_{D2} \) corresponds to the difference in input voltages \( V_{in1} - V_{in2} \). This output can then be used in further stages of an amplifier or processing circuit.

### 3. **Common-Mode Rejection (CMR)**

One of the key advantages of a differential pair amplifier is its ability to reject common-mode signals—those that are the same at both input terminals. Common-mode rejection is critical in many applications, especially where noise and interference are prevalent (such as in audio, communication, or sensor interfaces).

The differential pair works because any common-mode signal (e.g., noise or a voltage spike affecting both inputs equally) will affect both MOSFETs in the same way. Since the circuit is designed to amplify the difference between the input signals, any identical voltage present on both \( V_{in1} \) and \( V_{in2} \) will not contribute to the output voltage.

The **Common-Mode Rejection Ratio (CMRR)** is a measure of how effectively the differential pair rejects common-mode signals. A high CMRR is desirable because it means the circuit can effectively reject noise while amplifying the desired differential signal.

### 4. **Biasing and Operating Regions**

To ensure proper operation of the MOSFET differential pair, it is important to bias the MOSFETs correctly so that they operate in the **saturation region** (also known as the **active region**) of their characteristic curves. This ensures that the MOSFETs behave as controlled current sources, which is essential for the differential pair to function as an amplifier.

- **Bias Current**: The current source or current mirror must supply a constant current to the differential pair. This is typically set based on the desired operating point of
