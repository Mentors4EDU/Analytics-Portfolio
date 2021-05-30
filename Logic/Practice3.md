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
One directly states the instructional address, and one stores it in the memory field instead of directly accessing it. Therefore, direct memory access is faster, but limited in regards to flexibility outside of speed. How one wants to use direct vs indirect memory addressing, and whether they want to address it or load instructions from a pointer, depends on the application and what they are trying to do. In general, my preference have been direct memory addressing.
