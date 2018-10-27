# hacking-book
My source repo for the book "Hacking: The Art of Exploitation"

## Patches
Since the second edition of the book was published in 2008, there are many inconsistencies between the book and my computer's Arch Linux.

### Critical
- `char_array2.c`: Changed the size of `str_a` to 20.

### Architecture-Dependent
- `pointer_types5.c`: The type of `hacky_nonpointer` should be `unsigned long long` when compiled to 64-bit binary. The code is patched in `pointer_types5_x64.c`. If it's compiled to 32-bit binary, the original code works fine.
