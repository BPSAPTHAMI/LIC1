# Current mirrors

A current mirror as an active load refers to a circuit configuration where a current mirror replaces a passive resistor or other conventional load to improve gain and performance in amplifier circuits. It provides a high output resistance, ensuring better current sourcing and sinking with minimal voltage dependency.

## Working Principle
A current mirror consists of two or more transistors configured to copy a reference current to another branch with high accuracy. When used as an active load in amplifier circuits (e.g., differential amplifiers or common-emitter amplifiers), it replaces the traditional resistive load, providing:

High output impedance → Enhances gain.
Improved linearity → Better performance in small-signal amplification.
Better current matching → Less dependence on variations in supply voltage.

## Design question

 ![image](https://github.com/user-attachments/assets/e2d73e61-9f25-4349-953c-d155459e57b7)

Gain: 𝐴𝑣>-10𝑉/𝑉 or >=20dB
​𝑉dd=1.8𝑉
Power 𝑃<1𝑚𝑊
Current Mirror Ratio: 1:1 , 1:2 ,1:3,1:4,2:1


Given: 𝑃total<1𝑚𝑊,  𝑉𝐷𝐷=1.8𝑉

Itotal = P/ VDD =1mW/1.8v= 0.56mA

Itotal= 𝐼ref+𝐼x

Iref =Ix = Itotal/2 = 0.28mA 

















