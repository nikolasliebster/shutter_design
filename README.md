# shutter_design
Fast Shutter Design

This shutter design is a fast, consistent way to physically block laser light. All credit for original design inspiration to https://arxiv.org/pdf/1509.01566.pdf.

A schematic of the circuit (ShutterCircuit.jpeg) is in the repository. An incoming TTL signal is split and inverted once. This signal goes into the inputs of the H-Bridge (SN754410NE). 

The outputs of the H-Bridge go to the shutter motor and a set of capacitors in series with a resistor. The capacitors serve to allow a burst of current when the TTL signal switches, allowing the shutter to quickly close. The resistor allows a steady offset current to flow, which holds the shutter in place after switching. 

Vcc can be adjusted (~10-15V is suggested), but zener diodes should be set such that the zener-voltage matches Vcc.

The parts for the shutter can be 3D printed (STL files are attached). The shaft of the motor must be filed down and inserted into the center of the "bowtie". This is in turn inserted into the larger housing. Two thin, flat strips of rubber should be glued onto the top and bottom stops of the shutter housing, described in more detail in https://arxiv.org/pdf/1509.01566.pdf.

At 10V Vcc, the shutter has a mean delay between TTL signal switching and physically blocking light of 5.02 +/- 0.01 ms.
