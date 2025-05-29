## MONOSTABLE MULTIVIBRATOR USING 555 TIMER IC
A multivibrator is an electronic circuit that switches between two states (HIGH and LOW) to create different types of pulses or signals. It uses feedback to keep changing states.

### Pin Configuration
![image](https://github.com/user-attachments/assets/9940bb3d-ff68-48a3-83ec-44fea36ed361)

### Internal circuit diagram of 555 timer IC
![image](https://github.com/user-attachments/assets/796379f8-93c5-432a-8739-2f204a63d23d)

The types of multivibrators are:
1.Astable Multivibrator
Also called free-running because it never stops switching states.
It has no stable state.
Produces continuous pulses at a fixed frequency and duty cycle.
Made with two transistors, two capacitors, and some resistors.
Used in oscillators, clocks, and pulse generators.

2.Monostable Multivibrator
Called one-shot because it produces only one pulse when triggered.
Has one stable state and one temporary (unstable) state.
When triggered, it gives a pulse of fixed length, then returns to stable.
Also uses two transistors, two capacitors, and some resistors.
Used for timers, delays, and pulse width modulation.

3.Bistable Multivibrator
Known as a flip-flop.
Has two stable states and stays in either until triggered to switch.
Made with two transistors, capacitors, and resistors.
Used as memory elements, switches, or latches in digital circuits.


### How the 555 Timer Monostable Multivibrator Works
Initially, the output is low (stable state).
When triggered (input voltage falls below a threshold), output goes high (temporary unstable state).
The internal capacitor starts charging through resistor R, controlling how long output stays high.
Once the capacitor voltage reaches 2/3 of supply voltage, output goes back low (stable state).
Pulse width (duration of the high output) = 1.1 × R × C seconds.


Design Example: Pulse Width 0.5 ms
When you trigger the 555 timer, it creates a 0.5 ms high pulse regardless of trigger length.
It ignores any further triggers during the output pulse.
After the pulse ends, it’s ready for the next trigger.

### SIMULATION RESULTS
INPUT WAVE @ trigger pin
![image](https://github.com/user-attachments/assets/0f5c53a8-920f-4220-81f3-c22bf6b924d1)

output wave @ output pin and @ capcitor pin between threshold and discharge
![image](https://github.com/user-attachments/assets/5cbf074c-7df1-4159-bc6b-0a1f4254c481)

LTspice circuit diagram
![image](https://github.com/user-attachments/assets/423fa657-9279-45dd-8fc0-690fb4b0a6e6)

![image](https://github.com/user-attachments/assets/e8ea12d8-bdf2-4794-9fe7-93d78468a41d)
*V1 is Output of the Astable Multivibrator
*V2 is Capacitor Voltage of Astable Multivibrator
V3 is Output of Differentiator
V4 is Capacitor Voltage of Monostable Multivibrator
Vout is Output of Monostable Multivibrator
pulse width is 0.5ms

### Inference
Changing R and C changes output pulse time.
RC=T
Normal 555 astable circuit can’t always give exact ON/OFF times needed.
Using an inverter (NOT gate) can help flip signals and get desired timing.
Small resistors and capacitors allow short pulses (under 1 ms).
Differentiator circuits help detect exact signal edges for precise triggering.
The monostable 555 setup produces clean pulses independent of trigger length, useful for timing and signal shaping.











