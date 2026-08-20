# ⚙️ Arithmetic Logic Unit (ALU) & Datapath Test

### Description
Verifies 32-bit arithmetic (ADD, SUB), bitwise logical operations (AND, OR, XOR, shifts), signed comparisons, and Zero flag assertion for branching.

### Files Involved
* `alu.v`
* `register_file.v`
* `test.v` (or `tb_alu.v`)

### Run Command
```powershell
# Compile design and testbench
iverilog -o sim_alu.vvp alu.v register_file.v test.v

# Run simulation
vvp sim_alu.vvp

# Open waveform viewer
gtkwave wave.vcd