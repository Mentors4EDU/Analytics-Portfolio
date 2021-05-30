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
Byte order is 0x108...10B

**#7** \
The data is not read correctly, because the byte orders are read and stored differently. For example, you can store in both decimal format or hexi or in binary to hexi versus binary to decimal. Since you have different byte orders and byte order capacities, the data has a higher chance of being formatted wrongly, being corrupted, or being needed to be converted to the right format. This can still be manageable and work out if done correctly from a software standpoint, but integrating conversion methods or formats, especially into firmware, is a pain, and not generally worth the extra hassle.
