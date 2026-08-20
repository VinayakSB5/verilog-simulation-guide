# 🚀 Verilog Simulation Commands

### 1. Single Module Test (e.g., INT8 MAC)
```powershell
# Step 1: Compile module + testbench
iverilog -o sim_mac.vvp int8_mac.v tb_int8_mac.v

# Step 2: Run simulation
vvp sim_mac.vvp

# Step 3: Open waveform
gtkwave mac_waveform.vcd