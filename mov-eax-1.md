# mov eax, 1

Basic mov immediate instruction.

Output:

    b8 01 00 00 00
    ^^ ^^^^^^^^^^^
    1  2

1.  Opcode
2.  Immediate value: `1` in little endian

Opcode bits:

    1 0 1 1 1 0 0 0
    ^^^^^^^^^ ^^^^^
    1         2

1. What to do.
2. Where to move to. `000` is `eax`.

Intel documentation says:

-   Opcode: `B8 + rd id`.

    `+rd` says that the 3 bits at the end are the destination register.

    `id` says that a double word immediate follows.

-   Op/En: `OI`.

    The "Instruction Operand Encoding" table for `mov` and `OI` says:

    Operand 1: `opcode + rd (w)`
    Operand 2: `imm8/16/32/64`
