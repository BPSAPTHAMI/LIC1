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

















