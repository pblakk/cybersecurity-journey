# Ghidra Observation 01 — If/Else Branching in Assembly

**Date:** 27 April 2026
**Source file:** branch.c
**Binary analyzed:** branch.exe

## The C code I wrote
```c
int x;
scanf("%d", &x);

if (x == 5) {
    puts("Correct");
} else {
    puts("Wrong");
}
```

## What Ghidra showed in the decompiler
```c
int local_c;
scanf("%d", &local_c);
if (local_c == 5) {
    puts("Correct");
}
else {
    puts("Wrong");
}
```

## What the disassembly showed
```asm
CMP  EAX, 0x5
JNZ  LAB_1400014d8
```

## What I learned
- Variable names do not survive compilation. I named
  my variable x but Ghidra calls it local_c because
  that information is stripped from the binary.
- The compiler turned my if/else into two instructions:
  CMP compares the value to 5, JNZ jumps to the else
  branch if the comparison was not equal.
- JNZ means Jump if Not Zero — it fires when the
  CMP result was not equal. This is the opposite of
  what you might expect reading the source code.
- When the compiler can see that a variable is always
  the same value it removes the branch entirely through
  constant folding. My first branch.c with x hardcoded
  to 5 had no if/else in the compiled output at all.

## Malware analysis relevance
- CMP followed by a conditional jump is one of the
  most common patterns in all compiled C code and
  in malware. Recognizing it instantly is a core
  reverse engineering skill.
- Malware uses conditional jumps to implement license
  checks, anti-debug checks, and environment detection.
  A CMP followed by JNZ that skips past a block of
  code is often exactly what a crackme or malware
  check looks like.
- Constant folding means compiled malware will not
  always look like its source code. Optimizations
  remove dead branches and inline values — analysts
  must reason about what the code does, not just
  what it looks like.
