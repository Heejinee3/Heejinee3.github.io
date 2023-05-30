---
index: 1 # labs number
num: 4 # lab number
title: Pipeline CPU
permalink: /lab/Computer-Architecture/Pipeline-CPU # link
category: lab # project or lab
---

#### **Overview**

---

Pipeline CPU Lab is intended to give you hands-on experience in designing a modern microprocessor, whose operations are conducted in pipelined fashion. Based on the concepts and skills you have acquired through the lab assignments, you are now ready to implement a pipeline CPU. Through this lab assignment, you will be gaining an in-depth understanding on the fundamentals of designing a CPU microarchitecture.

<br>

#### **Task**

---

In Pipeline CPU Lab, you are required to implement a pipeline CPU.

The template assumes the system with following rules:

1. The instruction memory and data memory is physically separated as two independent modules (check the testbench files).

2. The overall memory size is 4KB for instructions and 16KB for data.

3. The memory follows byte addressing, which supports accessing individual bytes of data rather than only larger units called words (for instructions, this is naturally handled whereas for data, this is enabled using the D_MEM_BE port, check the testbench files and the RISCV_TOP.v file).

4. Little-endian

5. The control path and data path should be separated.

6. As we have not covered the concept of “Virtual Memory” in this course just yet, you can assume that the lower N-bits of the instruction and data memory addresses are used as-is to access instruction memory and data memory.

   1. For accessing instructions, use (Effective_Address & 0xFFF) as the translation
      function
   2. For accessing data, use (Effective_Address & 0x3FFF) as the translation function

7. The initial value of the Program Counter (PC) is 0x000.

8. The initial value of the stack pointer is 0xF00.

Your implementation MUST comply with the following rules:

1. RISC-V ISA (RV 32I)

2. You’re required to implement 5 stage pipeline

3. You need to resolve data hazards and control hazards.
   Refer the grading policy

4. You need to implement only below instructions
   1. JAL
   2. JALR
   3. BEQ, BNE, BLT, BGE, BLTU, BGEU
   4. LW
   5. SW
   6. ADDI, SLTI, SLTIU, XORI, ORI, ANDI, SLLI, SRLI, SRAI
   7. ADD, SUB, SLL, SLT, SLTU, XOR, SRL, SRA, OR, AND

The template of memory and register file is already given to you. You are only required to implement the control and data path of the pipeline. If you implement correctly, you will see a “Success” message in the console log when you run the testbench file. The TAs recommend you to carefully design which modules are needed, how to connect them, and which control signals are necessary to transfer to the data units, before you start to write the code.

<br>

#### **Code and Report**

---

[Github](https://github.com/Heejinee3/Computer-Architecture/tree/master/Pipeline%20CPU)

<br>

#### **Glossary**

---

[Pipeline CPU](https://velog.io/@chunjakim/Pipeline-CPU)

[Hazard](https://velog.io/@chunjakim/Hazard)
