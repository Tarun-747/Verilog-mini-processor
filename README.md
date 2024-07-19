# Mini Processor Design and Implementation in Verilog

## Overview

This project involves the design and implementation of a mini processor using Verilog. The processor is capable of executing a predefined set of instructions, including arithmetic, logical, and control operations. The final design is synthesized and implemented on an FPGA.

## Table of Contents

1. [Project Description](#project-description)
2. [Features](#features)
3. [Instructions](#instructions)

## Project Description

The mini processor has a register file consisting of 16 registers, each of 8 bits. The processor can execute various instructions, including addition, subtraction, multiplication, division, and logical operations. It also supports branching and data movement instructions. The design includes modular components such as the ALU, register file, and control unit, ensuring a clear and testable structure.

## Features

- **16 8-bit Registers**: Supports a wide range of operations with 16 general-purpose registers.
- **Instruction Set**: Implements a variety of instructions including arithmetic, logical, and control operations.
- **FPGA Implementation**: Synthesized and tested on an FPGA for real-world validation.
- **Detailed Testbenches**: Comprehensive testing for each module and the overall processor.

## Instructions

1. **Verilog Simulation and Synthesis**:
    - Use your preferred Verilog simulation tool (e.g., ModelSim, Xilinx Vivado) to simulate the Verilog files.
    - Ensure all testbenches pass the simulations.

2. **FPGA Implementation**:
    - Synthesize the design using an FPGA tool like Xilinx Vivado.
    - Program the FPGA with the generated bitstream file.

## Instruction Set

| Instruction | Opcode  | Operation                          |
|-------------|---------|-------------------------------------|
| NOP         | 0000 0000 | No operation                      |
| ADD Ri      | 0001 xxxx | Add ACC with Register contents and store the result in ACC. Updates C/B |
| SUB Ri      | 0010 xxxx | Subtract ACC with Register contents and store the result in ACC. Updates C/B |
| MUL Ri      | 0011 xxxx | Multiply ACC with Register contents and store the result in ACC. Updates EXT |
| DIV Ri      | 0100 xxxx | Divides ACC with Register contents and store the Quotient in ACC. Updates EXT with remainder |
| LSL ACC     | 0000 0001 | Left shift left logical the contents of ACC. Does not update C/B |
| LSR ACC     | 0000 0010 | Left shift right logical the contents of ACC. Does not update C/B |
| CIR ACC     | 0000 0011 | Circuit right shift ACC contents. Does not update C/B |
| CIL ACC     | 0000 0100 | Circuit left shift ACC contents. Does not update C/B |
| ASR ACC     | 0000 0101 | Arithmetic Shift Right ACC contents |
| AND Ri      | 0101 xxxx | AND ACC with Register contents (bitwise) and store the result in ACC. C/B is not updated |
| XRA Ri      | 0110 xxxx | XRA ACC with Register contents (bitwise) and store the result in ACC. C/B is not updated |
| CMP Ri      | 0111 xxxx | CMP ACC with Register contents (ACC-Reg) and update C/B. If ACC>=Reg, C/B=0, else C/B=1 |
| INC ACC     | 0000 0110 | Increments ACC, updates C/B when overflows |
| DEC ACC     | 0000 0111 | Decrements ACC, updates C/B when underflows |
| Br <4-bit address> | 1000 xxxx | PC is updated and the program Branches to 4-bit address if C/B=1 |
| MOV ACC, Ri | 1001 xxxx | Moves the contents of Ri to ACC |
| MOV Ri, ACC | 1010 xxxx | Moves the contents of ACC to Ri |
| Ret <4-bit address> | 1011 xxxx | PC is updated, and the program returns to the called program |
| HLT         | 1111 1111 | Stop the program (last instruction) |


