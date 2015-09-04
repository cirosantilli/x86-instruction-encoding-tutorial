# mov ebx, 1

Compare with [mov eax, 1](mov-eax-1.md) to see how `ebx` is encoded.

Output:

    bb 01 00 00 00

Bits of opcode:

    1 0 1 1 1 0 1 1
    ^^^^^^^^^ ^^^^^
    1         2

Field 2 contains `3` which corresponds to `ebx` as expected.
