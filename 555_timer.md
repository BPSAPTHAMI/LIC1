

A multivibrator is an electronic circuit that switches between two states (HIGH and LOW) to create different types of pulses or signals. It uses feedback to keep changing states.

The three types are:

1. Astable Multivibrator

No stable state — it continuously switches between HIGH and LOW, producing a continuous square wave.

It works like an oscillator generating clock pulses.



2. Monostable Multivibrator

One stable state and one temporary state.

When triggered, it switches to the temporary state for a fixed time, then returns to the stable state.

Used to create a single pulse of a specific duration.



3. Bistable Multivibrator

Two stable states.

It stays in one state until an external trigger switches it to the other state.

Acts like a flip-flop, used for storing binary data.

Sure! Here’s a simplified summary of what you shared, put in easier words:


---

Types of Multivibrators

Astable Multivibrator

Also called free-running because it never stops switching states.

It has no stable state.

Produces continuous pulses at a fixed frequency and duty cycle.

Made with two transistors, two capacitors, and some resistors.

Used in oscillators, clocks, and pulse generators.


Monostable Multivibrator

Called one-shot because it produces only one pulse when triggered.

Has one stable state and one temporary (unstable) state.

When triggered, it gives a pulse of fixed length, then returns to stable.

Also uses two transistors, two capacitors, and some resistors.

Used for timers, delays, and pulse width modulation.


Bistable Multivibrator

Known as a flip-flop.

Has two stable states and stays in either until triggered to switch.

Made with two transistors, capacitors, and resistors.

Used as memory elements, switches, or latches in digital circuits.



---

How the 555 Timer Monostable Multivibrator Works

Initially, the output is low (stable state).

When triggered (input voltage falls below a threshold), output goes high (temporary unstable state).

The internal capacitor starts charging through resistor R, controlling how long output stays high.

Once the capacitor voltage reaches 2/3 of supply voltage, output goes back low (stable state).

Pulse width (duration of the high output) = 1.1 × R × C seconds.



---

Design Example: Pulse Width 0.5 ms

When you trigger the 555 timer, it creates a 0.5 ms high pulse regardless of trigger length.

It ignores any further triggers during the output pulse.

After the pulse ends, it’s ready for the next trigger.



---

Practical Cases

1. Case 1: Trigger starts output pulse, duration depends on R and C only, not trigger length.


2. Case 2: During output pulse, any new triggers are ignored until pulse ends.


3. Case 3: Trigger shorter than output pulse still causes full pulse output.





Key Points and Improvements

Changing R and C changes output pulse time.

Normal 555 astable circuit can’t always give exact ON/OFF times needed.

Using an inverter (NOT gate) can help flip signals and get desired timing.

Small resistors and capacitors allow short pulses (under 1 ms).

Differentiator circuits help detect exact signal edges for precise triggering.

The monostable 555 setup produces clean pulses independent of trigger length, useful for timing and signal shaping.











