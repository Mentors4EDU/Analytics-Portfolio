# Chapter 9
**#2** \
In regards to direct implementation:
1. Reduced instructions
2. Ease of direct hardware control
3. Approximation
4. 3 Different Register Operancds
5. Few Addressing modes
6. Uniform pipeling time
7. Fixed-length/short direct instructions

In regards to what couldn't be implemented:
1. Difficult to implement multiple registers
2. Limitations on pipeline structuring and parameter passing
3. Access over load instructions for access memory
4. Micro-programmed controlled implmentations
5. Requires harded compiling in regards to implementation

**#10** \
**a)** \
Since a single set of registers are implemented be each procedure execution, then it can only save N-1 procedures for the current active execution. 4 Procedure calls are allowed for the RISC w/ 5 registers. \
**b)** \
A minimum of 2 registers need to be directly saved and stored as the procedure calls. \
**c)** \
Since the recently saved pointer is mantained, when the most recent procedure returns a process, then the register window is restored back for usage. \
**d)** \ 
Given that you already have 4 filled registers, a single register window would need to be saved for a new procedure.
