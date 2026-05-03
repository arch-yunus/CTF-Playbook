# Binary Exploitation (Pwn) Methodology

Systematic approach to memory corruption challenges.

## 1. Initial Analysis
- **Check Security Mitigations**:
  ```bash
  checksec --file ./binary
  ```
- **Static Analysis**:
  - `strings ./binary`
  - Use **Ghidra** or **IDA Pro** to understand logic.
- **Dynamic Analysis**:
  - Use **GDB** with **GEF** or **pwndbg**.

## 2. Vulnerability Identification
- **Buffer Overflow**: Look for `gets()`, `scanf()`, `strcpy()`.
- **Format String**: Look for `printf(user_input)` without format specifiers.
- **Integer Overflow**: Check arithmetic operations on user-controlled integers.

## 3. Exploit Development
- **Find Offset**:
  ```python
  from pwn import *
  pattern = cyclic(100)
  ```
- **Control Instruction Pointer (EIP/RIP)**.
- **Bypass Protections**:
  - **NX**: Use ROP (Return Oriented Programming).
  - **ASLR**: Leak addresses to calculate base.
  - **Canary**: Leak or brute-force the canary value.

## 4. Execution
- Use `pwntools` to automate the exploit script.
