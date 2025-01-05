# VHDL Counter Reset Bug

This repository demonstrates a subtle bug in a simple VHDL counter. The counter is designed to count from 0 to 15 and reset to 0 when it reaches 15. However, under specific clock and reset conditions, the counter might not reset correctly.  The bug is related to how the reset signal interacts with the rising edge of the clock.

## Bug Description
The `buggy_counter.vhd` file contains the buggy code.  The counter's reset behavior is not always reliable due to a potential race condition or unexpected sensitivity to the reset signal timing relative to the clock.  The exact conditions for the bug to appear might be simulation-dependent. 

## Bug Solution
The `fixed_counter.vhd` file presents a corrected implementation that addresses the reset issue by carefully handling the reset condition. The solution ensures that the counter reliably resets to 0 whenever the reset signal is asserted, regardless of the clock's state. This example emphasizes proper handling of asynchronous resets in VHDL.