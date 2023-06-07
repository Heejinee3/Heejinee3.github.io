---
index: 1 # labs number
num: 3 # lab number
title: Multi-cycle CPU
permalink: /lab/Computer-Architecture/Multi-cycle-CPU # link
category: lab # project or lab
---

#### **Overview**

---

Multi-cycle CPU Lab is intended to give you hands-on experience in designing a modern microprocessor, whose operations are conducted within multiple clock cycles. Based on the concepts and skills you have acquired through previous labs, you are now ready to implement a multi-cycle CPU (Fig. 1). Through this lab assignment, you will have gained an in-depth understanding on the fundamentals of designing a CPU microarchitecture.

<br>

#### **Task**

---

In Multi-cycle CPU Lab, you are required to implement a multi-cycle CPU.

The template assumes the system with following rules:

1. The instruction memory and data memory are physically separated as two independent modules (check the testbench files).

2. The overall memory size is 4KB for instructions and 16KB for data.

3. The memory follows byte addressing, which supports accessing individual bytes of data rather than only larger units called words (for instructions, this is naturally handled whereas for data, this is enabled using the D_MEM_BE port, check the testbench files and the RISCV_TOP.v file).

4. Little-endian

5. The control path and data path should be separated.

6. Since we have not covered the concept of “Virtual Memory” in this course yet, you can assume that the lower N-bits of the instruction and data memory addresses are used as-is to access instruction memory and data memory.

   1. For accessing instructions, use (Effective_Address & 0xFFF) as the translation function
   2. For accessing data, use (Effective_Address & 0x3FFF) as the translation function

7. The initial value of the Program Counter (PC) is 0x000.

8. The initial value of the stack pointer is 0xF00.

Your implementation MUST comply with the following rules:

1. RISC-V ISA (RV32I)

2. Each stage takes one clock cycle.

   1. e.g.) jump instruction takes one cycle.

3. You only need to implement the below instructions (some instructions are removed):

   1. JAL
   2. JALR
   3. BEQ, BNE, BLT, BGE, BLTU, BGEU
   4. LW
   5. SW
   6. ADDI, SLTI, SLTIU, XORI, ORI, ANDI, SLLI, SRLI, SRAI
   7. ADD, SUB, SLL, SLT, SLTU, XOR, SRL, SRA, OR, AND

The template of memory and register file is already given to you. You are only required to implement the control and data path of the multi-cycle CPU. If you implement correctly, you will see a “Success” message in the console log when you run the testbench file. The TAs recommend you to carefully design which modules are needed, how to connect them, and which control signals are necessary to transfer to the data units, before you start to write the code.

<br>

#### **Code, Report and Results**

---

[Github](https://github.com/Heejinee3/Computer-Architecture/tree/master/Multi-cycle%20CPU){:target="\_blank"}

<br>

#### **Glossary**

---

[Multi-cycle CPU](https://velog.io/@chunjakim/Multi-cycle-CPU){:target="\_blank"}
