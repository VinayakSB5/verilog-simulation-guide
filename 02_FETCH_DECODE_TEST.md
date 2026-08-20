# 🔍 Instruction Fetch & Decode Test

### Description
Tests the Program Counter (PC), Instruction Memory sequencing, and Control Unit opcode decoding.

### Files Involved
* pc_unit.v
* instruction_memory.v
* control_unit.v
* tb_top_fetch_decode.v

### Commands
iverilog -o sim_fetch_decode.vvp pc_unit.v instruction_memory.v control_unit.v tb_top_fetch_decode.v
vvp sim_fetch_decode.vvp
gtkwave fetch_sim.vcd

### Signals to Inspect
* clk, reset
* pc[31:0]
* instr[31:0]
* opcode[6:0]
* reg_write, alu_src, mac_en