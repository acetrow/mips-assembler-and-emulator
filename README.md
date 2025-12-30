# MIPS Assembler and Emulator

A C-based MIPS assembler and emulator that parses MIPS assembly code, converts it into bytecode, and executes it in a simulated environment. The project supports a subset of MIPS instructions, label resolution, memory access, branching, and register-level execution.

This project demonstrates low-level systems programming concepts such as instruction encoding, CPU execution flow, memory mapping, and endianness handling.

---

## Features

- Parses MIPS assembly source files (.asm)
- Supports `.data` and `.text` sections
- Assembles instructions into 32-bit MIPS bytecode
- Executes instructions in a simulated MIPS environment
- Implements register file, program counter, and memory
- Supports label resolution for branch instructions
- Handles big-endian memory representation using `htonl` / `ntohl`

---

## Supported Instructions

### R-type
- `add`
- `sll`
- `srl`
- `nop`

### I-type
- `addi`
- `andi`
- `bne`
- `lui`
- `lw`
- `sw`
- `lhu`
- `sh`

---

## Project Structure

- `emulator.c` — Core assembler and emulator logic
- `emulator.h` — Shared definitions, constants, and data structures
- `main.c` — Program entry point and CLI handling
- `Makefile` — Build instructions
- `*.asm` — Example MIPS assembly programs

---

## Build Instructions

Requires:
- GCC
- Linux / Unix-based system

To build the emulator:
make


This produces the executable:
./emulator

---

## Usage

Run the emulator with an assembly file:

./emulator -i program.asm

Example:

./emulator -i simple_add.asm


The emulator will:
1. Load the program
2. Assemble instructions into bytecode
3. Execute the program
4. Print register states and memory output

---

## Example Programs

Included example assembly programs demonstrate:
- Arithmetic operations
- Loops and branching
- Bitwise operations
- Memory load/store
- Checksum-style calculations

---

## Technical Highlights

- Instruction decoding using bit masking and shifting
- Register file implemented as a fixed-size array
- Program counter managed using MIPS memory layout conventions
- Branch offsets calculated relative to instruction position
- Endianness handled explicitly for correct memory behavior

---

## Why This Project Matters

This project demonstrates:
- Understanding of CPU architecture and instruction sets
- Low-level C programming skills
- Assembly language parsing and execution
- Systems-level thinking beyond application development

It is intended as a personal learning and portfolio project.

---

## License

MIT License