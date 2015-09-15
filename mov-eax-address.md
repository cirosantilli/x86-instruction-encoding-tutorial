# mov eax, address

Output:

    b8 05 00 00 00 ff
    ^^^^^^^^^^^^^^ ^^

1. Moving an immediate of value 5 to `eax`
2. The hardcoded `ff` byte we point to.

If we do `objdump -Sr` on the object file, we see:


    00000000 <address-0x5>:
       0:   b8 05 00 00 00          mov    $0x5,%eax
                1: R_386_32 .text

The rellocation applied is `R_386_32`.
