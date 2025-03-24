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

## Current mirror - Aspect ratio 1:1 
### DC ANALYSIS:
![aa11](https://github.com/user-attachments/assets/7c034319-a0e6-4f41-9da4-b1dc6ba17c8e)
### TRANSIENT ANALYSIS:
![aa11t](https://github.com/user-attachments/assets/0aa87496-1c6a-422a-bc25-5b5f6feb679c)
### AC ANALYSIS:
![aa11ac](https://github.com/user-attachments/assets/47bcea71-6256-4e6f-b0e9-815801001c2d)


## Current mirror - Aspect ratio 1:2 
### DC ANALYSIS:
![Screenshot 2025-03-24 182725](https://github.com/user-attachments/assets/7969c055-7295-4f94-b7b8-05aa36243f18)
### TRANSIENT ANALYSIS:
![aa12t](https://github.com/user-attachments/assets/c790a035-60b9-44ae-8345-f44a1474363f)
### AC ANALYSIS:
![aa11ac](https://github.com/user-attachments/assets/a0a01439-67e5-4d9e-91d7-cd402f895f72)



## Current mirror - Aspect ratio 1:3
### DC ANALYSIS:
![aa13dc](https://github.com/user-attachments/assets/54000202-b7f0-4caa-8d2a-7a13ae541d88)

### TRANSIENT ANALYSIS:
![aa13t](https://github.com/user-attachments/assets/13a3be28-e5ff-4ba6-8006-ea52ba3f945c)

### AC ANALYSIS:
![aa13ac](https://github.com/user-attachments/assets/52a9c7c5-c573-408c-8a15-fdcaa0f2ff0f)



## Current mirror - Aspect ratio 1:4
### DC ANALYSIS:
![aa14dc](https://github.com/user-attachments/assets/7165123e-bfe7-40a5-aa79-5320ade591e9)

### TRANSIENT ANALYSIS:
![aa14t](https://github.com/user-attachments/assets/be1217b3-1f58-4b04-a09a-da07b32199df)

### AC ANALYSIS:
![aa14ac](https://github.com/user-attachments/assets/03c357ad-217f-493c-bea3-624470a9eac4)




## Current mirror - Aspect ratio 2:1
### DC ANALYSIS:
![aa21dc](https://github.com/user-attachments/assets/6e885d95-3ef9-4b14-9049-b4bb10e616c8)

### TRANSIENT ANALYSIS:
![aa21t](https://github.com/user-attachments/assets/8d5b6629-e118-4efb-b73b-9dff48b81745)

### AC ANALYSIS:
![aa14ac](https://github.com/user-attachments/assets/ec30c9e8-ef95-4737-ba7d-15b7b23c3821)















