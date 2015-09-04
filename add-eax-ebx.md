# add eax, ebx

Output:

    01 d8
    ^^ ^^

1. Opcode
1. ModR/M

Opcode bits:

    0 0 0 0 0 0 0 1
    ^^^^^^^^^^^ ^ ^
    1           2 3

1. This is an add.
2. Add REG to R/M as represented on the ModR/M byte. Otherwise, other way around.
3. 32-bit operands. Otherwise, 8-bit.

ModR/M bits:

    1 1 0 1 1 0 0 0
    ^^^ ^^^^^ ^^^^^
    1   2     3

1. MOD = 3: REG and R/M are registers.
2. REG = 3: EBX
3. REG = 0: EAX

So from the opcode, we move REG (EBX) into R/M (EAX).

Note that two encodings are possible on reg / reg operations: we could swap the before last bit to 1 and both registers.

Both possible encodings are documented on the instruction table:

    01 /r    ADD r/m32, r32
    03 /r    ADD r32, r/m32

`/r` says that a MOdR/M follows the opcode, and that the 2 last bits describe it.
