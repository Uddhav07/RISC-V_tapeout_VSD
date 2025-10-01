## Introduction

System On Chip (SOC):
all in a single chip including:
1. CPU
2. Memory
3. I/O ports
4. GPU
5. DSP
6. Power management unit, and other special features dependent preiferrals.


amazing since they take less space and are more energy efficient.   
Apple in its macbook uses soc which enables faster access, it is more close to being an soc so its more efficient than its competitors.


## Types of SOC

1. Microcontroller based SOC: for low compute, embedded tech. simple control tasks.
2. MicroProcessor based SOC: more compute, calculations, running OS.
3. Application based SOC: 


## VSDBabySoC 

VSDBabySoC integrates 3 ip cores for them to work together.

1. RVMYTH Processor Core: digital processing brain, cycling data through its r17 register for continuous data stream generation.
2. PLL: Generates stable, synchronized clock signals.
3. DAC: 10 bit digital to analog converter for conversion of digital signals from RVMYTH into analog signals.

this allows control and data sharing with analog devices 

data is sent from r17 pin of RVMYTH processor.

uses sky130 pdk.




off chip clocks are not used since they are unreliable.

there are 2 types of DAC:

1. weighted resister DAC:

![381912254-344e4ffd-7509-41e7-ac42-21a553b3db11](https://github.com/user-attachments/assets/c21a2891-f26e-40b4-8955-1bff03defdf0)

3. R-2R Ladder DAC:
<img width="484" height="197" alt="381912104-5c15f424-1a94-4424-b019-a76c0ca0db43" src="https://github.com/user-attachments/assets/271afb51-58ec-4e87-b09d-457e58fe4ad1" />




