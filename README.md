Shift Register using Verilog

Description

A shift register is a sequential digital circuit used to store and shift binary data from one flip-flop to another. In this project, a 4-bit right shift register is designed using Verilog HDL.

Data is shifted by one position on every positive edge of the clock.

Features

- 4-bit shift register
- Right-shift operation
- Synchronous operation with clock
- Reset input
- Designed using Verilog HDL
- Includes testbench and simulation

Inputs and Outputs

Signal| Direction| Description
"clk"| Input| Clock signal
"reset"| Input| Reset signal
"serial_in"| Input| Serial data input
"q"| Output| 4-bit register output

Working

When "reset" is active, the register is cleared to "0000".

On every positive edge of the clock:

q[3] <= q[2]
q[2] <= q[1]
q[1] <= q[0]
q[0] <= serial_in

For example, if serial data "1011" is given one bit at a time, the data shifts through the register with each clock pulse.

🛠️ Tools Used

- Verilog HDL
- Icarus Verilog
- GTKWave
- GitHub

📊 Expected Result

The output "q" shifts by one bit on every positive clock edge. When reset is applied, the output becomes "0000".

Files

- "shift_register.v" – Design code
- "shift_register_tb.v" – Testbench
- "simulation_output.txt" – Expected simulation output
- "README.md" – Project documentation
