## 1. introductions to timings .lib
gvim sky130_fd_sc_hd__tt_025C_1v80.lib  
sp <file>  // parallel tab in gvim  
vsp <file path> //vertical tab in gvim  
wider cells consume more power but delay will be less  


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/af494d6f-a1c5-4e43-9098-e618a6a8f027" />

## 2. hierarchical vs Flat Synthesis
YOSYS
```
1. read_lib
2. read verilog
3. synth -top
4. abc -liberty
5. show
6. write_verilog -noattr
7. flatten //hierarchies are flattened out
```
-> stack of nmos gates is better than pmos stack  
-> therefore, nand , not is preffered over or

// only synthesis a module of the whole verilog file
```
synth -top sub_module1 
```
1. preffered when multiple instances of same module exist
2. divide and conquer, convert massive netlist to smaller and 

