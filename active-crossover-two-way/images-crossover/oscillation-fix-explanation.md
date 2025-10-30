# High-frequency oscillation fix on U5A (NE5532)

An oscillation around 3 MHz was observed when resistor R31 (7k87) was connected 
between the non-inverting input and ground. This resistor, together with the input 
capacitance of the op-amp, introduced a high-frequency pole that reduced phase margin. See the picture below:

![High-frequency oscillation](oscilation-with-R31.png)

By grounding the non-inverting input directly (removing R31), the phase margin improved 
and the oscillation was completely eliminated. See the picture below:

![High-frequency oscillation eliminated](oscilation-eliminated-R31-grounded.png)

