# Chapter 4
**#5** \
**a)** 4M x 16 = 2^2(4) x 2^20(1m) x 2^1 = 2^23 = 23 bits \
**b)** 4M x 16 = 2^2(4) x 2^20(1m) x 2^0 = 2^22 = 22 bits \
**#19** \
The various stages are fetch, decode, execute, memory and write back. \
Also, you have *IR* which is the Instruction Register, \
*MAR* which is the *Memory Address Register* and \
*MBR* which is the *Memory Buffer Register*. \
First you store the instructions to be fetched, which is the buffering. \
You decode and execute the instructions, store the results, \
and write back the memory. \
**#32**
```ASSEMBLY
ORG 100
Load  A
Store X      / Store A
Load  B
Store Y      / Store B
JnS    Mul   / Multiplication
Load  Sum          / Load result
Store E      / E:= A x B
Load  C
Store X      / Repeat with C and D
Load  D
Store Y      
JnS   Mul   
Load  Sum       
Store F      / F := C x D
Load  E 
Add   F     / Load problem
Halt           / Terminate program
A,      Dec ?        / Decrements
B,      Dec ?         / (give valyes
C,      Dec ?       
D,     Dec ? /
X,      Dec 0         
Y,      Dec 0      
Ctr,   Dec 0         / Count
One, Dec 1       
E,      Dec 0         / Buffer
F,      Dec 0        
Sum, Dec 0
Mul,   Hex 0         / Store
Load Y               
Store Ctr            / Store counter
Clear                           /Clear
Store Sum          / Store Sum
Loop, Load Sum /Load Sum
Add   X               / Add variable
Store Sum          / Store Sum Result

           Load  Ctr
           Subt  One          / Decrement counter
           Store Ctr            / Store counter
           Skip  Cond 400   / Conditional Loop
           Jump Loop          / Continue
           JumpI Mul           / Return
           END
```           
**#33**
```ASSEMBLY
Loop
           Load X / Load X
           Subt Diff / Check difference
           Skipcond 400 / Condition
           Jump End / End
           Load X / Reload
           Add One
           Store X / X + 1
           Jump Loop / Return
End Halt / (end while)
One HEX 0001
Diff HEX 000A
X HEX 0001
```
**#38** \
**#60** \
**T or F**
