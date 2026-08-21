#  Verilog & Git Survival Guide

Notes and lessons learned from building and simulating a RISC-V INT8 AI Accelerator on Windows using Icarus Verilog and GTKWave.

---

##  1. How to Run Verilog Simulations

### Step A: Single Module / Submodule Test
When testing just one block (like the INT8 MAC unit or Datapath):
```powershell
# 1. Compile design + testbench into a simulation file
iverilog -o sim_mac.vvp int8_mac.v tb_int8_mac.v

# 2. Run simulation (this creates the .vcd waveform file)
vvp sim_mac.vvp

# 3. Open GTKWave
gtkwave mac_waveform.vcd