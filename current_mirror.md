# Current mirrors

A current mirror as an active load refers to a circuit configuration where a current mirror replaces a passive resistor or other conventional load to improve gain and performance in amplifier circuits. It provides a high output resistance, ensuring better current sourcing and sinking with minimal voltage dependency.

## Working Principle
A current mirror consists of two or more transistors configured to copy a reference current to another branch with high accuracy. When used as an active load in amplifier circuits (e.g., differential amplifiers or common-emitter amplifiers), it replaces the traditional resistive load, providing:

High output impedance → Enhances gain.
Improved linearity → Better performance in small-signal amplification.
Better current matching → Less dependence on variations in supply voltage.

## Design question

 ![image](https://github.com/user-attachments/assets/e2d73e61-9f25-4349-953c-d155459e57b7)
- Design and analyse current mirror circuit as active load in amplifier circuit. 

A)
 i) Design for Av<=-10V/V
- Vdd=1.8V
- p<=1mW
- Design for current mirror ratio 1:1 , 1:2.

- ii) Analysis the current mirror circuit(DC analysis)
- iii)- case 1) L=180n (W/L)=x
  - case 2) L=500n (W/L)= x
  - case 3) L=1u (W/L)=x
- iv) Transient and AC analysis: Max output swing and bandwidth.
- Vary the current mirror ratio and analyse the current mirroring.

B)
- Design the differential amplifer using the same design specification as experiment 3.
- Perform DC analysis, Transient and AC analysis.


Given: 𝑃total<1𝑚𝑊,  𝑉𝐷𝐷=1.8𝑉

Itotal = P/ VDD =1mW/1.8v= 0.56mA

Itotal= 𝐼ref+𝐼x

Iref =Ix = Itotal/2 = 0.28mA 

## Current mirror -  ratio 1:1 
### DC ANALYSIS:
![aa11](https://github.com/user-attachments/assets/7c034319-a0e6-4f41-9da4-b1dc6ba17c8e)
Itotal=Iref+Ix

For 1:1 ratio Iref=Ix

Itotal = Iref + Iref

Iref=Itotal/2

Itotal=P/Vdd

Itotal=1mW/1.8V

Itotal=0.555mA.

Therefore,Iref=0.277mA.

The aspect ratio of MOSFET M2 is same as that of M3

hence,
- W/L for M1 is 101.5um/180nm 
- W/L for M2 is 101.5um/180nm
- W/L for M3 is 101.5um/180nm
  
### TRANSIENT ANALYSIS:
![aa11t](https://github.com/user-attachments/assets/0aa87496-1c6a-422a-bc25-5b5f6feb679c)
### AC ANALYSIS:
![aa11ac](https://github.com/user-attachments/assets/47bcea71-6256-4e6f-b0e9-815801001c2d)
Gain= 29.03 dB

## Current mirror - ratio 1:2 
### DC ANALYSIS:
![Screenshot 2025-03-24 182725](https://github.com/user-attachments/assets/7969c055-7295-4f94-b7b8-05aa36243f18)
Itotal=Iref+Ix

For 1:2 ratio 2*Iref=Ix

Itotal = Iref + 2*Iref

Iref=Itotal/3

Itotal=P/Vdd

Itotal=1mW/1.8V

Itotal=0.555mA.

Therefore,Iref=0.185mA.

The aspect ratio of MOSFET M2 is twice of M3

hence,
- W/L for M1 is 133um/180nm 
- W/L for M2 is 203um/180nm
- W/L for M3 is 101.5um/180nm
- 
### TRANSIENT ANALYSIS:
![aa12t](https://github.com/user-attachments/assets/c790a035-60b9-44ae-8345-f44a1474363f)
### AC ANALYSIS:
![aa11ac](https://github.com/user-attachments/assets/a0a01439-67e5-4d9e-91d7-cd402f895f72)
Gain=29.048 dB


## Current mirror - ratio 1:3
### DC ANALYSIS:
![aa13dc](https://github.com/user-attachments/assets/54000202-b7f0-4caa-8d2a-7a13ae541d88)
Itotal=Iref+Ix

For 1:3 ratio 3*Iref=Ix

Itotal = Iref + 3*Iref

Iref=Itotal/4

Itotal=P/Vdd

Itotal=1mW/1.8V

Itotal=0.555mA.

Therefore,Iref=0.1388mA.

The aspect ratio of MOSFET M2 is thrice of M3

hence,
- W/L for M1 is 150um/180nm 
- W/L for M2 is 304.5um/180nm
- W/L for M3 is 101.5um/180nm

### TRANSIENT ANALYSIS:
![aa13t](https://github.com/user-attachments/assets/13a3be28-e5ff-4ba6-8006-ea52ba3f945c)

### AC ANALYSIS:
![aa13ac](https://github.com/user-attachments/assets/52a9c7c5-c573-408c-8a15-fdcaa0f2ff0f)
Gain= 29.045 dB


## Current mirror - ratio 1:4
### DC ANALYSIS:
![aa14dc](https://github.com/user-attachments/assets/7165123e-bfe7-40a5-aa79-5320ade591e9)
Itotal=Iref+Ix

For 1:4 ratio 4*Iref=Ix

Itotal = Iref + 4*Iref

Iref=Itotal/5

Itotal=P/Vdd

Itotal=1mW/1.8V

Itotal=0.555mA.

Therefore,Iref=0.111mA.

The aspect ratio of MOSFET M2 is four times of M3

hence,
- W/L for M1 is 158.4um/180nm 
- W/L for M2 is 406um/180nm
- W/L for M3 is 101.5um/180nm

### TRANSIENT ANALYSIS:
![aa14t](https://github.com/user-attachments/assets/be1217b3-1f58-4b04-a09a-da07b32199df)

### AC ANALYSIS:
![aa14ac](https://github.com/user-attachments/assets/03c357ad-217f-493c-bea3-624470a9eac4)
Gain= 29.01 dB



## Current mirror - ratio 2:1
### DC ANALYSIS:
![aa21dc](https://github.com/user-attachments/assets/6e885d95-3ef9-4b14-9049-b4bb10e616c8)
Itotal=Iref+Ix

For 2:1 ratio 0.5*Iref=Ix

Itotal = Iref + 0.5*Iref

Iref=Itotal/1.5

Itotal=P/Vdd

Itotal=1mW/1.8V

Itotal=0.555mA.

Therefore,Iref=0.0.37mA.

The aspect ratio of MOSFET M2 is half of M3

hence,
- W/L for M1 is 66.8um/180nm 
- W/L for M2 is 101.5um/180nm
- W/L for M3 is 203um/180nm


### TRANSIENT ANALYSIS:
![aa21t](https://github.com/user-attachments/assets/8d5b6629-e118-4efb-b73b-9dff48b81745)

### AC ANALYSIS:
![aa14ac](https://github.com/user-attachments/assets/ec30c9e8-ef95-4737-ba7d-15b7b23c3821)
Gain= 29.045 dB


## comparison table:

| Ratio | Iref | Vx | Vout |
|------|----|----|------|
|  1:1 | 0.277mA | 1.20712 V | 1.2084 V  |
|  1:2 | 0.185mA | 1.23094 V | 1.23876 V  |
|  1:3  | 0.1388 mA | 1.24655 V | 1.24099 V |
|  1:4  |0.111mA | 1.25816 V | 1.25824 V  |
|  2:1  | 0.37 mA | 1.23085 V | 1.23166 V  |

| Ratio | M1(W) | M2(W) | M3(W) | 
|------|----|----|------|
| 1:1   | 101.5um | 101.5um | 101.5um  |
| 1:2   | 133um | 203um | 101.5um  |
| 1:3   | 150um | 304.5um | 101.5um  |
| 1:4   | 158.4um | 406um| 101.5um  |
| 2:1   | 66.8 um | 101.5um | 203um  |
- length= 180 nM

 ## 1:1 ratio for length 500nm:
 ### DC ANALYSIS:
![50011](https://github.com/user-attachments/assets/0e78c719-17e5-4077-b5ee-7e00a1072ab5)
- Width of M3,M2 is 101.5 um.
- Width of M1 is 193 um.

  ### AC ANALYSIS:
  ![image](https://github.com/user-attachments/assets/6d36ce2c-fc4a-4d49-87e7-98db310323da)
  - Gain=37.754 dB


## 1:1 ratio for length 1um:
 ### DC ANALYSIS:
![image](https://github.com/user-attachments/assets/1b13736f-040f-4771-a5c9-b139feb1c952)
- Width of M3,M2 is 101.5 um.
- Width of M1 is 230 um.

  ### AC ANALYSIS:
![image](https://github.com/user-attachments/assets/b9573f25-dd23-4963-90b0-588b47845dbe)
 - Gain= 40.28 dB

 - 
## Inference:

- The reference current (Iref) changes based on the aspect ratio.

As the ratio increases (1:1 → 1:4), Iref decreases, meaning less current flows.

In the 2:1 case, Iref is the highest, showing that more current is being mirrored.


- The output voltage (Vout) stays almost the same for all ratios.


- The transistors (M1, M2, M3) are sized differently to match the aspect ratio and control current flow.

M2, which copies the current, gets bigger as the ratio increases.

M3 stays the same in most cases, except for the 2:1 ratio, where it is larger, allowing it to handle more current.


- The minor difference between Vx and Vout across ratios suggests voltage drops due to drain-source resistance or mobility variations.

The deviation in 1:3 (Vx = 1.24655V, Vout = 1.24099V) indicates a small mismatch possibly due to process variations or short-channel effects.



- The 2:1 ratio gives the highest current (0.37mA) because the transistors are sized to allow more current flow.

This setup is useful when the circuit needs to drive more current.





## PART B

### DC ANALYSIS:
![aachi11](https://github.com/user-attachments/assets/f42db0ca-9fbc-4209-8a18-9241a03a7366)

### TRANSIENT ANALYSIS:
![aachi22](https://github.com/user-attachments/assets/f01ea5a9-d537-4160-befd-aa7b5063b690)

### AC ANALYSIS:
![aachi33](https://github.com/user-attachments/assets/b3d6cc4a-8612-4ff5-9591-8c74b4208729)
Gain=33.31 dB

## Inference: 
- current mirroring is not perfect because of channel length effects.  
- The gain increases as the current mirror ratio increases.
- The gain reaches a maximum value of 33.31 dB during AC analysis.








