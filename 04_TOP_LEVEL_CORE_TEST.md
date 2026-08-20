# 🏛️ Full Top-Level RISC-V Core Integration Test

### Description
Executes full instruction flow from fetch through execution and writeback for both RV32I arithmetic and custom INT8 MAC instructions.

### Files Involved
* alu.v
* control_unit.v
* instruction_memory.v
* pc_unit.v
* register_file.v
* int8_mac.v
* riscv_top.v
* tb_riscv_top.v

### Commands
iverilog -o sim_top.vvp alu.v control_unit.v instruction_memory.v pc_unit.v register_file.v int8_mac.v riscv_top.v tb_riscv_top.v
vvp sim_top.vvp
gtkwave riscv_top_sim.vcd

### Signals to Inspect
* clk, reset
* pc[31:0]
* instr[31:0]
* wr_data[31:0]
* mac_en
* mac_out[31:0]