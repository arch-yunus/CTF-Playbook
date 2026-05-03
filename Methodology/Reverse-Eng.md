# Reverse Engineering Methodology

Techniques for analyzing and deconstructing binaries.

## 1. Static Analysis
- **File Identification**: `file ./binary`.
- **Code Decompilation**: Use **Ghidra**, **Cutter**, or **IDA Pro**.
- **Control Flow Graph**: Visualize the logic flow.

## 2. Dynamic Analysis
- **Debugging**: Step through code using **GDB** or **x64dbg**.
- **Tracing**: Use `ltrace` (library calls) and `strace` (system calls).
- **Patching**: Modify the binary to bypass checks (e.g., changing a `JZ` to `JNZ`).

## 3. Specialized Techniques
- **Unpacking**: Identify and unpack packed binaries (UPX, etc.).
- **Deobfuscation**: Simplify complex, obfuscated logic.
- **Symbolic Execution**: Use **Angr** to find paths to specific code locations.
