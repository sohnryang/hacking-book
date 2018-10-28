# hacking-book
My source repo for the book "Hacking: The Art of Exploitation"

## Patches
Since the second edition of the book was published in 2008, there are many inconsistencies between the book and my computer's Arch Linux.

### Critical
- `char_array2.c`: Changed the size of `str_a` to 20.

### Architecture-Dependent
- `pointer_types5.c`: The type of `hacky_nonpointer` should be `unsigned long long` when compiled to 64-bit binary. The code is patched in `pointer_types5_x64.c`. If it's compiled to 32-bit binary, the original code works fine.
- `scope3.c`: The original code used `0x%08x` in format string to print address of variables, but the code doesn't work properly in x64; I changed it to `%p` to show addresses properly in 64-bit systems.

### Coding Style
1. There are spaces in front and back of operators. (example: `i = 0;` instead of `i=0;`)
2. In for statements, use pre-increment operator rather than post-increment operator.

### Misc
- All code: I modified the book's original code to return 0 if ended successfully.
