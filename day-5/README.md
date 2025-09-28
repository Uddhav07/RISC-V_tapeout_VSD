# Day 5

## 1. if vs case statements  

case statements can cause latches even w/ default.

suppose:
```verilog
case (sel)
00: x=a, y=b
01: begin x=c  // y is not assigned here!
default: x=d, y=b
endcase
```
when sel=01, it doesn't know what y should be so it takes latched value. even w/ default statement.
need to assign all o/p signals to avoid latches.

### if vs case behavior:

#### if-else:
- executes first to last 
- if condition 1 true → terminates, doesn't check others

#### case:
- sequential reading even if one condition matches
```verilog  
case(sel)
00: // condition 1  
10: // condition 2
11: // condition 3
0?: // overlaps w/ 00!
```
if sel=00, it matches first condition AND 0? condition. causes problem.
don't use overlapping cases.

## 2. Theory 

if statements → priority logic  
case statements → parallel execution

if-else creates mux chain:
```verilog
if (condition1) output = c1;
else if (condition2) output = c2; 
// and so on
```
works like cascaded mux. condition1 has priority.

### latch problems:

incomplete if creates inferred latch - not synthesizable in combinational:
```verilog
always @(posedge clk)
if (res) 
    count = 3'b000;
else if (en)
    count <= count + 1; // use non-blocking
```
this works fine becuase when en=0 we want to hold count value. latch is expected here.

but in combinational circuit huge problem - latch not desired.

### case statement latches:

incomplete case also causes latches if no default.
use default statement to avoid latches.

## 3. Looping constructs

2 types:
- for loop → inside always statement  
- generate for loop → outside always

for loop = evaluating expressions, not generating hardware  
generate for = instantiating hardware

### for loop example:

2:1 mux easy to write:
```verilog
always @(*)
case (sel)
0: y = i0;
1: y = i1;
```

but 32:1 or 64:1 mux takes huge space. use for loop:
```verilog
always @(*)
for (i=0; i<32; i=i+1)
    if (i==sel)
        y = inp[i];
```
much easier.

same for demux:
```verilog
always @(*)
opbus[7:0] = 0;
for (i=0; i<8; i=i+1)
    if (i==sel)
        opbus[i] = input;
```

### generate for:

creates instances of gates, replicates hardware.  
used outside always block.
```verilog
generate 
for(i=0; i<8; i++)
    and uand (.a(a[i]), .b(b[i]), .y(y[i]));
endgenerate
```

example: ripple carry adder  
- 8 bit addition needs 8 full adders
- 16 bit needs 16 full adders  
single hardware instantiated multiple times using generate for.

for loop → evaluation  
generate for → hardware replication
