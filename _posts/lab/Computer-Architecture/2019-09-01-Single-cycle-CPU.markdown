---
index: 1 # labs number
num: 2 # lab number
title: Single-cycle CPU
permalink: /lab/Computer-Architecture/Single-cycle-CPU # link
category: lab # project or lab
---

#### **Overview**

---

Single-cycle CPU Lab is intended to give you hands-on experience in designing the simplest form of a modern microprocessor, whose operations are conducted within a single clock cycle. Based on the concepts and skills you have acquired through ALU Lab and Vending Machine Labs, you are now ready to implement a single-cycle CPU. Through this lab assignment, you will have gain an in-depth understanding on the fundamentals of designing a CPU microarchitecture.

<br>

#### **Task**

---

In Single-cycle CPU Lab, you are required to implement a single-cycle CPU, which is the simplest form of CPU.

Your implementation MUST comply with the following rules:

1. The instruction memory and data memory is physically separated as two independent modules (check the testbench files).

2. The overall memory size is 4KB for instructions and 16KB for data.

3. The memory follows byte addressing, which supports accessing individual bytes of data rather than only larger units called words (for instructions, this is naturally handled whereas for data, this is enabled using the D_MEM_BE port, check the testbench files and the RISCV_TOP.v file).

4. Little-endian

5. The control path and data path should be separated.

6. As we have not covered the concept of “Virtual Memory” in this course just yet, you can assume that the lower N-bits of the instruction and data memory addresses are used as-is to access instruction memory and data memory.

   1. For accessing instructions, use (Effective_Address & 0xFFF) as the translation function
   2. For accessing data, use (Effective_Address & 0x3FFF) as the translation function

7. The initial value of the Program Counter (PC) is 0x000.

8. The initial value of the stack pointer is 0xF00.

9. You need to implement only below instructions

   1. LUI, AUIPC
   2. JAL
   3. JALR
   4. BEQ, BNE, BLT, BGE, BLTU, BGEU
   5. LB, LH, LW, LBU, LHU,
   6. SB, SH, SW
   7. ADDI, SLTI, SLTIU, XORI, ORI, ANDI, SLLI, SRLI, SRAI
   8. ADD, SUB, SLL, SLT, SLTU, XOR, SRL, SRA, OR, AND

The template of memory and register file is already given to you. You are only required to implement the control and data path of the single-cycle CPU. If you implement correctly, you will see a “Success” message in the console log when you run the testbench file, as shown in the figure below. The TAs recommend you to carefully design which modules are needed, how to connect them, and which control signals are necessary to transfer to the data units, before you start to write the code.

![Figure1](/assets/lab/Computer-Architecture/Figure1.PNG)

<br>

#### **Code, Report and Results**

---

[Github](https://github.com/Heejinee3/Computer-Architecture/tree/master/Single-cycle%20CPU)

<br>

#### **Glossary**

---

[Control Path & Data Path](https://velog.io/@chunjakim/Control-Path-Data-Path)

[Single-cycle CPU](https://velog.io/@chunjakim/Single-cycle-CPU)

[ISA](https://velog.io/@chunjakim/ISA-Instruction-Set-Architecture)
