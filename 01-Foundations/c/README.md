# C Programming

Building C fundamentals for malware analysis using
Programming in C by Stephen Kochan as primary text.

## Compiler setup
- Terminal: MSYS2 UCRT64
- Compiler: GCC 15.2.0
- Command: `gcc filename.c -o filename`
- Practice folder: C:\Users\tpard\c_practice

## Goal
Recognize compiled C patterns in disassembly.
Every program written here gets compiled with GCC
in MSYS2 UCRT64 and examined in Ghidra.

## Progress tracker

| Program | Concept | Status | Date |
|---------|---------|--------|------|
| hello.c | Basic output using puts() | Completed | 4 April 2026 |
| program1.c | Basic output using printf() | Completed | 4 April 2026 |
| branch.c | If/else conditional branching | Completed | 4 April 2026 |

## Program index
- [hello.c](./hello.c)
- [program1.c](./program1.c)
- [branch.c](./branch.c)

## Key compiler note
Use MSYS2 UCRT64 terminal for compiling — not MINGW64
or MSYS. GCC is in the PATH by default in UCRT64.
