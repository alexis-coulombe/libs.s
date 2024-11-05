# LibS: Useful I/O Functions and System Call Wrappers

LibS is a library written in RISC-V assembly that provides useful input/output (I/O) functions and system call wrappers for basic operations like reading integers, characters, and strings, as well as printing them.

## Features

The library includes the following functions:

- **readInt**: Reads an integer from standard input.
- **printInt**: Prints an integer to standard output.
- **readChar**: Reads a single character from standard input.
- **printChar**: Prints a single character to standard output.
- **readString**: Reads a string from standard input until a newline or EOF is encountered.
- **printString**: Prints a null-terminated string to standard output.
- **strlen**: Computes the length of a null-terminated string.
- **printf**: A formatted print function that handles `%d` (integer) and `%s` (string) format specifiers.

## System Calls

The library uses the following Linux system calls:

- **Read** (syscall number 63): For reading from standard input.
- **Write** (syscall number 64): For writing to standard output.
- **Exit** (syscall number 93): For terminating the program.

## Installation

To compile this library, you will need a RISC-V assembler and linker, such as the ones provided in the RISC-V GNU Toolchain. Use the following command to compile:

```bash
riscv64-unknown-elf-gcc -o libS.o -c libS.s
