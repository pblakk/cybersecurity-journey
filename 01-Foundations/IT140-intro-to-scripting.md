# IT 140 — Introduction to Scripting (Python)

Completed: March 2026

## Topics covered
- Data types and variables — integers, strings, floats,
  booleans and how Python handles each
- Decision statements — if/elif/else logic for
  controlling program flow based on conditions
- Loops — for and while loops for iteration and
  repetition, including loop control with break
  and continue
- Functions — defining reusable code blocks, parameters,
  return values, and scope
- File handling — reading from and writing to files,
  managing file input and output in scripts
- Lists and data structures — creating and manipulating
  ordered collections of data
- Regular expressions — pattern matching for searching
  and extracting text from strings
- Debugging — identifying and fixing errors in Python
  code using PyCharm IDE
- Practical scripting — building simple, useful
  applications from fundamental programming constructs

## Tools used
- **PyCharm** — primary IDE for writing, executing,
  and debugging Python scripts
- **zyBooks** — interactive platform for hands-on
  learning and weekly lab exercises

## Projects completed

### Text-based game
Developed an interactive text-based application
demonstrating decision logic, loops, functions, and
user input handling. Required integrating multiple
Python concepts into a working, structured program.

### Weekly scripting labs
Completed hands-on labs covering each major concept —
data types, conditionals, loops, functions, file I/O,
and regular expressions — building practical scripting
fluency through repeated application.

## What I understand now that I didn't before
- Programming is structured thinking made executable.
  The logic of if/else decisions and loops is the same
  logic used in every automated process — including
  malware. Understanding how to build that logic means
  understanding how to read it when you encounter it
  in disassembly.
- Regular expressions are a powerful pattern matching
  tool. The ability to search for patterns in strings
  is directly applicable to extracting indicators of
  compromise from malware output, log files, and
  memory dumps.
- File handling is where programs interact with the
  system. Reading and writing files in Python is the
  same conceptual operation malware performs when it
  drops payloads, reads configuration files, or
  exfiltrates data — understanding it from a
  programming perspective makes it recognizable
  from an analysis perspective.
- Debugging is a transferable methodology. Tracing
  why a script behaves unexpectedly by stepping
  through logic and checking variable states is
  the same approach used in dynamic malware analysis
  with a debugger like x64dbg.
- Functions make code reusable and readable. Most
  malware is organized into functional components —
  a function for network communication, a function
  for encryption, a function for persistence. Learning
  to think in functions makes recognizing those
  components in disassembly more natural.

## Connection to malware analysis
- **Python is the primary scripting language for
  malware analysis tooling.** Volatility, pefile,
  YARA Python bindings, and Ghidra scripting all
  use Python. IT 140 built the foundation that
  every analysis tool in the roadmap depends on.
- **Regular expressions connect directly to IOC
  extraction.** Analysts use regex constantly —
  extracting IP addresses, URLs, file paths, and
  registry keys from malware output, memory dumps,
  and log files. IT 140 introduced the skill that
  Phase 2 tooling work will develop further.
- **File I/O connects to binary file analysis.**
  Reading files in Python — especially in binary
  mode — is how analysis tools examine malware
  samples. The pefile library, hex viewers, and
  string extractors all build on basic file handling.
- **Debugging methodology connects to dynamic
  analysis.** Stepping through code to understand
  behavior is identical whether you are debugging
  a Python script in PyCharm or stepping through
  malware instructions in x64dbg. IT 140 built
  the mental model.
- **Functions connect to reverse engineering.**
  Malware analysts spend significant time identifying
  and naming functions in disassembly. Understanding
  how functions are structured in source code makes
  recognizing them in compiled code significantly
  faster.

## Current status
Python knowledge from this course needs reactivation
after a gap of approximately one month. A targeted
three-session reactivation plan is underway focused
on file I/O, binary data handling, and the pefile
library — the specific Python skills needed for
Phase 2 malware analysis tooling.

## What I want to go deeper on
- Binary file handling in Python — reading executables
  as raw bytes, working with hex values, and parsing
  structured binary formats like PE files
- The pefile library — parsing PE file headers, import
  tables, and section data programmatically
- Regular expressions for IOC extraction — building
  patterns that reliably extract IP addresses, URLs,
  file hashes, and registry paths from unstructured
  text and memory dumps
- Automating malware analysis tasks — writing Python
  scripts that perform static analysis steps
  automatically rather than manually, building toward
  the tools in 04-Projects and 08-Scripts-Tools
- Ghidra Python scripting — using Python to automate
  repetitive reverse engineering tasks inside Ghidra,
  covered in Phase 2 and beyond
