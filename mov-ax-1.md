# mov ax, 1

Output:

    66 b8 01 00
    ^^ ^^ ^^^^^
    1  2  3

1. 66 prefix: indicates that instead of 32-bit memory, this instruction uses 16 bit memory.
2. Same as `mov eax, 1`.
3. Same as `mov eax, 1`, but 16 bit only.

Intel manual says: `mov eax, 1`, which is analogous to 
