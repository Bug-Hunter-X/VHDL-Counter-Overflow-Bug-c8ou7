# VHDL Counter Overflow Bug

This repository demonstrates a common bug in VHDL code: an unhandled overflow condition in a simple counter.  The `bug.vhdl` file contains the erroneous code.  The solution, addressing the overflow, is in `bugSolution.vhdl`.

**Bug Description:**

The counter's `internal_count` signal is incremented until it reaches 15.  However, there's no explicit handling of what occurs when the counter should wrap around from 15 to 0. This can lead to unexpected behavior, simulation errors, or even synthesis issues.

**Solution:**

The improved code in `bugSolution.vhdl` uses a modulo operation to handle the wrap-around correctly, ensuring that the counter behaves as expected.