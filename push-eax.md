# push eax

Output:

    50

Which is a single opcode.

The opcode can be further decomposed into the following bits:

    0 1 0 1 0 0 0 0
    ^^^^^^^^^ ^^^^^
    1         2

1. This is a `push` instruction.
2. From where we will push. `000` is `eax`.

This is documented as: opcode == `50+rd` in the Intel manual. The `+rd` part says that the 3 last bits indicate where to push from.
