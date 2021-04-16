# RV32I-Logisim
# RISCV-single-cycle-core-Logisim
RV32I single core processor 
## Description
This repository contains RISC-V Single Cycle 32 Bit Processor simulation on Logic Simulator called Logisim. This circuit contains 32 bit ALU, 32 bit Data Bus, 16KB ROM/RAM, 12 Bit Address Bus for both RAM MAR(memory address register). Register File contains 32 Registers with data width of 32 bits. Troubleshooting codes used to verify all the circuit components.
## Under The Guidance Of
Zeeshan Rafique
## Pre-Req Tools
Logisim Software
Venus online simulator
Github 
Git
## Designing Procedure
At first learn the basic instructions of the RV32I Instruction Set Architecture and learn their functionality. To learn the backend working use Venus Online RV32I Simulator. This Simulator helps grasp the working behind the instruction much faster. On the Logic Simulator software first start with the program counter and memory address register. Then develop the circuit for the immediate generation which uses full instruction and PC to generate respective immediate. after that create register file with 32 registers each 32-bit data width. This register file takes 5-bit address to select one of the 32 registers and write data to it using register enable wire. two 5-bit address RS1 and RS2 are to read one of the 32 registers simultaneously. Now make 32 Bit ALU with 4-bit ALU operation Select which selects which operation to perform according to the instruction. After completing create type decoder which uses 7-bit opcode to decode the type of the instruction. Then in control Decoder depending upon the type of instruction, function3 and function7 different components are controlled. Integrate type decode and control decode, and this will become your control unit. Add RAM and configure its data bits to 32bit and address width to 12 bits. To handle branch instruction Branch circuit is now having to be created using the simple comparators and depending upon the RS1 and RS2 conditional jump is done if branch is true. In the end Add a 32-bit adder for jalr as this instruction requires two additions. One ALU cannot perform 2 operation on a single cycle. Connect the wiring using the splitters, multiplexers, constants, tunnels, and clocks. To troubleshoot the circuit, start with the simpler instructions e.g.; add, addi and watch the circuit behavior using temporary register outputs. To load the machine code on the Instruction Register, simulate the code on Venus then using dump feature copy the machine code and create .mem extension file on notepad.
## Circuit screenshot
![image](https://user-images.githubusercontent.com/80220683/113491595-78369300-94eb-11eb-93ac-f8d275778f61.png)
