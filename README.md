# hacking-book
My source repo for the book "Hacking: The Art of Exploitation"

## Patches
Since the second edition of the book was published in 2008, there are many inconsistencies between the book and my computer's Arch Linux.

### Critical
- `char_array2.c`: changed the size of `str_a` to 20.

### Architecture-Dependent
- `pointer_types5.c`: the type of `hacky_nonpointer` should be 64-bit unsigned integer (`int64_t`) when compiled to 64-bit binary. If it's compiled to 32-bit binary, the original code works fine.
