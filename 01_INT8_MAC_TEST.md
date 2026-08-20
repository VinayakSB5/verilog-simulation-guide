# ⚡ INT8 MAC Hardware Accelerator Test

### Description
Verifies 8-bit signed multiplication and 32-bit accumulation for neural network matrix multiplications.

### Files Involved
* int8_mac.v
* tb_int8_mac.v

### Commands
iverilog -o sim_mac.vvp int8_mac.v tb_int8_mac.v
vvp sim_mac.vvp
gtkwave mac_waveform.vcd

### Signals to Inspect
* clk, reset
* in_a[7:0] (Signed activation input)
* in_b[7:0] (Signed weight input)
* out_acc[31:0] (Accumulated 32-bit result)