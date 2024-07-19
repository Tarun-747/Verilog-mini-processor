# Mini Processor Design and Implementation in Verilog

## Overview

This project involves the design and implementation of a mini processor using Verilog. The processor is capable of executing a predefined set of instructions, including arithmetic, logical, and control operations. The final design is synthesized and implemented on an FPGA.

## Table of Contents

1. [Project Description](#project-description)
2. [Features](#features)
3. [Directory Structure](#directory-structure)
4. [Instructions](#instructions)

## Project Description

The mini processor has a register file consisting of 16 registers, each of 8 bits. The processor can execute various instructions, including addition, subtraction, multiplication, division, and logical operations. It also supports branching and data movement instructions. The design includes modular components such as the ALU, register file, and control unit, ensuring a clear and testable structure.

## Features

- **16 8-bit Registers**: Supports a wide range of operations with 16 general-purpose registers.
- **Instruction Set**: Implements a variety of instructions including arithmetic, logical, and control operations.
- **FPGA Implementation**: Synthesized and tested on an FPGA for real-world validation.
- **Detailed Testbenches**: Comprehensive testing for each module and the overall processor.

## Directory Structure

## Instructions

1. **Verilog Simulation and Synthesis**:
    - Use your preferred Verilog simulation tool (e.g., ModelSim, Xilinx Vivado) to simulate the Verilog files.
    - Ensure all testbenches pass the simulations.

2. **FPGA Implementation**:
    - Synthesize the design using an FPGA tool like Xilinx Vivado.
    - Program the FPGA with the generated bitstream file.


