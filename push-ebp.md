# push ebp

Output:

    55

Which is a single opcode.

The opcode can be further decomposed into the following bits:

    0 1 0 1 0 1 0 1
    ^^^^^^^^^ ^^^^^
    1         2

1.  It is a push `push`.
2.  From where we will push. `101` is ebp.

This is documented as: opcode == `50+rd` in the Intel manual. The `+rd` part says that the 3 last bits indicate where to push from.
