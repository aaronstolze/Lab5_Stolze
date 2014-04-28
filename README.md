Lab5_Stolze
===========

Lab 5 

# Part 1

This part of the lab involved understanding the following PRISM code as it would appear as a waveform.

![alt text](https://raw.githubusercontent.com/aaronstolze/Lab5_Stolze/master/PRISMCode.PNG "ALU Waveform")

The code above would load a value of 8 into the accumulator, add 1 to this value, the output the new value to output port 3. It loops back to the addition portion causing an output from 9 to F.  The following waveform demonstrates this code. 

![alt text](https://raw.githubusercontent.com/aaronstolze/Lab5_Stolze/master/AnnotatedWaveform.png "ALU Waveform")

The code was then implemented onto the NEXYS2 board.  As seen in the linked video below, the board counts from 9 to F.
https://www.youtube.com/watch?v=5sR2Jg-be3I 

# Questions

1.	When the controller’s current state is “FETCH,” what is the status of the following control lines:

a.	PCLd - high

b.	IRLd - high 

c.	ACCLd - low

2.	The current state is Decode LoAddr and the IR contains “OUT.”  What are the control signals are asserted, and what will the next state be?

The asserted signals are MARLoLD, PCLd, MEMSel.  The next state is Direct I/O Execute.

3.	What are the three status signals sent from the PRISM datapath to the PRISM controller?

The three status signals are A = 0, A < 0, and the value of IR.

4.	Why is it important that ACCLd signal be active during the execute state for the ADDI instruction?

It is important because the ADDI must load the accumulator with some value which cannot be done without a high ACCLd signal.

5.	What changes are necessary to the PRISM datapath to add another instruction (SUBI, which would subtract an immediate value from the accumulator) to the instruction set?

There would need to be an increase in the size of the multiplexer to allow for the extra instruction.  
