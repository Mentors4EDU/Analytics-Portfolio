# Chapter 9
**#2** \
In regards to direct implementation:
1. Reduced instructions
2. Ease of direct hardware control
3. Approximation
4. 3 Different Register Operands
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
Given that you already have 4 filled registers, a single register window would need to be saved for a new procedure. \
**#12** \
The four categories are: SISD (Single Instruction Single Data Stream), SIMD (Single Instruction Multiple Data Steam), MISD (Multiple Instruction Single Data Stream), MIMD (Multiple Instruction Multiple Data Steam). \
SISD: Used for single operations for single data sets and streams (one at a time instructions, generally slow) \
SIMD: Single control unit with mulpile levels for the processor streaming data \
MISD: More of a form of vector processing, that is done through the same data stream flow but a linear processing array \
MIMD: Multiple instructions done through a distributed or sequent array of interconnected processors \
**#16** \
SPMD stands for Single Program/Multiple Data while SIMD is Single Instruction/Multiple Data. SPMD utilizes processing/executing the same operation, and is oriented towards shared/parallel computing over multi-threaded processing for many pieces of data on the same operation i.e (SIMD). \
**#18** \
VLIW architectures focus on parallelism in respect to instruction-levels. So you have the main unit, multiple levels, and data streams, sending data to the direct memory-level access. There is also a model in regards to super-scalar architectures which have multiple procesing units with multiple data streams running various operations through simultaneously ran processes. Other things could include shared and distributed memory, sequent computing, or interconnected networks. There are many variations of real world software defined computing networks that utilize similar architectures, even on large-scale mainframes. \
**#22** \
UMA is Unform Memory Access while NUMA is Non-Uniform Memroy Access. UMA utilizes a shared memory architecture in regards to parallel computing over a shared memory design in regards to multithreaded processing. They also utilize different communication methods, have different access time, and the execution is different. Data is also indexed differently given the architecture and design differences.
