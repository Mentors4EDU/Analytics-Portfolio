# Chapter 5
**#2** \
**a)**
| Address | 10_16 | 11_16 | 12_16 | 13_16 |
|---------|-------|-------|-------|-------|
| Little  | A1    | 89    | 67    | 49    |
| Big     | 49    | 67    | 89    | A1    |

Little goes to least significant byte while big goes to biggest. \
Byte order is 0x100...103 \
**b)** \
Little: 8A | 05 | 00 | 00 \
Big: 00 | 00 | 05 | 8A
Byte order is 0x104...107 \
**c)** \
Little: 88 | 88 | 14 | 14 \
Big: 14 | 14 | 88 | 88 \
Byte order is 0x108...10B \
**#7** \
The data is not read correctly, because the byte orders are read and stored differently. For example, you can store in both decimal format or hexi or in binary to hexi versus binary to decimal. Since you have different byte orders and byte order capacities, the data has a higher chance of being formatted wrongly, being corrupted, or being needed to be converted to the right format. This can still be manageable and work out if done correctly from a software standpoint, but integrating conversion methods or formats, especially into firmware, is a pain, and not generally worth the extra hassle. \
**#9** \
Stack-based architecture in general has many different lengths regarding different instructions, especially regarding actual logic-based communication and storing. Therefore, for things such as push that require some sort of address field along w/ the generic instruction types, fixed-instructional lengths are generally not preferred. \
**#12** \
**a)** \
X x Y + W x Z + V x U \
XY x + WZ x + VU x \
XY x + WZ x + + VU x \
XY x WZ x VU x + + \
Multiplication first, then addition, by high predecence or importance operation \
**b)** \
W x X + W (U x V + Z) \
W x X + W x UV x + Z \
W x X + W x UV x Z + \
WX x + WUV x Z + x \
WX x WUV x Z + x + \
**c)** \
(W x (X + Y x (U x V)))/(U x (X + Y)) \
(W x (X + Y x UV x))/(U x XY +) \
(W x (X + YUV x x))/(UXY + x) \
(W x (XYUV x x +))/(UXY + x) \
(WXYUV x x + x)/(UXY + x) \
WXYUV x x + x UXY + x / \
**#14** \
**a)** \
W X Y Z - + x \
W X (Y - Z) + x \
W(X + (Y - Z)) x \
W x (X + (Y - Z)) \
**b)** \
U V W X Y Z + x + x + \
U V W X (Y + Z) x + x + \
U V W (X x (Y + Z)) + x + \
U V (W + (X x (Y + Z))) x + \
(U + (V x (W + (X x (Y + Z))))) \
**c)** \
X Y Z + V W - x Z + + \
X (Y + Z) (V - W) x Z + + \
X ((Y + Z) x (V - W)) Z + + \
X + (((Y + Z) x (V - W)) + Z) \
**#20** \
In regards to direct vs indirect memory addressing: \
One directly states the instructional address, and one stores it in the memory field instead of directly accessing it. Therefore, direct memory access is faster, but limited in regards to flexibility outside of speed. How one wants to use direct vs indirect memory addressing, and whether they want to address it or load instructions from a pointer, depends on the application and what they are trying to do. In general, my preference has been direct memory addressing. \
**#23** \
You are talking about a non-pipelined system and a 5 stage pipeline system. You already have 200ns and 40ns, plus the number of segments is already 5. The ratio and theoretical speedup potential (rounding and slight inaccuracies aside), should be around 5 as well. You can input the k-stage equation for execution times regarding uneven pipelines (see [here](https://cs.stackexchange.com/questions/21924/execution-time-of-an-uneven-pipeline)). However, I think this is unnessary given the inputs I already been given. More than likely it will also be around 5 in regards to clock cycles because that is the same ratio in regards to the number of stages, and that should be the maximum speedup nonetheless. \
**#28** \
**a)** \
Ceil(log_2(7)) = 3 bits \
**b)** \
Ceil(log_2(60)) = 6 bits \
**c)** \
Ciel(log_2(256 x 2^10)) = 18 bits \
**d)** \
Adding them together makes 27 bits, and since the instructions are 32 bits, 32-27 = 5 bits left
# Chapter 6
**#2** \
**a)** \
So the main memory is 2^32 bytes \
The cache size is 1024 blocks \
The cache block size is 32 bytes \
2^32/2^5=2^27=128M = 134217728 blocks \
**b)** \
So the total address is 32 bits. \
Since you have 1024 blocks, you have bits of 10 for identification \
5 bits are used for the offset field \
The remain bits are for the tag \
So Tag 17 bits | Block 10 bits | Offset 5 bits \
**c)** \
Using a variation of modular arithmetic, you can convert to binary, then get the cache, and then get the block index. The resulting conversion method should be a block index for a cache that is 799_10. \
**#5** \
**a)** \
So the main memory size is 2^24 bytes or 16M x 8 \
The cache size will be 127 x 64 x 8 \
The block size is the 64 x 8 \
2^24/2^6=2^18=256K which is 262144 blocks \
**b)** \
You have the tag at 18 bits, offset at 6 bits, which equal 24 bits \
There are 16M bits in the main memory address \
This is fully associative, so 2(24) + 16 = 64 \
**c)**  \
Since it is fully associative, the main memory address 1D872_16 can be mapped to any cache block. \
**#9** \
**a)** \
So for a 2 way set, given that 32 blocks are batched into 2, you have 4 bits so, \
2^4, 4 is the set. \
Each block has 8 bytes so 2^3= 8 \
3 is the offset \
And then 16-(4+3)=9 9 is the tag \
so Tag 9 bits | Set 4 bits | Offset 3 bits \
**b)** \
So you have 32 blocks into 4 sets, so 32/4=8 8= 2^ 3 \
The number of sets and offset is 3 \
Since you have 2^16 bytes in main memory, 16-(3+3)=10 \
So, Tag is 10, Set is 3 and Offset is 3 bits.
