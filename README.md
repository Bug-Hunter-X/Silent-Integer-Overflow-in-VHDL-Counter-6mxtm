# Silent Integer Overflow in VHDL Counter

This repository demonstrates a subtle bug in VHDL involving silent integer overflow in a counter. The `buggy_counter.vhdl` file contains a counter that increments until it reaches its upper limit (15), at which point it silently wraps around to 0. This behavior is unexpected and can lead to difficult-to-debug issues in larger designs.

The `fixed_counter.vhdl` file shows a corrected version that handles the overflow situation more robustly, utilizing a more appropriate data type or explicitly checking for overflow conditions.

**How to reproduce:** Simulate `buggy_counter.vhdl` and observe the counter behavior when it reaches 15.  Note the lack of any error or warning indication.  This is the unexpected behavior.

**Key takeaway:**  Be mindful of potential integer overflows in your VHDL code, and consider using appropriate data types or explicit checks to mitigate the risk of silent errors.