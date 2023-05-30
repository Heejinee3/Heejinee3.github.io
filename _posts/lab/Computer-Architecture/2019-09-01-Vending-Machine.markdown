---
index: 1 # labs number
num: 1 # lab number
title: Vending Machine
permalink: /lab/Computer-Architecture/Vending-Machine # link
category: lab # project or lab
---

#### **Overview**

---

Vending Machine Lab teaches you more advanced concepts and skills of Verilog language. You have learned the basics of Verilog language in ALU Lab, now it’s time to improve it. In Vending Machine Lab, you are required to implement a vending machine. After
you finish Vending Machine Lab by yourself, you will have a good understanding of register-transfer level, synchronous circuit, and finite state machine which you have learned from the lectures.

<br>

#### **Task**

---

In Vending Machine Lab, you are required to implement a vending machine, which is an example of FSMs. There might be several corner cases while you implement the vending machine, so you have to make sure that your implementation of the vending machine functions properly for all use cases.

You are given a template of a vending machine in vending_machine.v. The template defines the interface of the vending machine, as shown in the table below.

<table>
   <tr>
      <th colspan="3"><strong>Input</strong></th>
   </tr>
   <tr>
      <th><strong>Signal</strong></th>
      <th><strong>Description</strong></th>
      <th><strong># of bits</strong></th>
   </tr>

   <tr>
      <td>i_input_coin</td>
      <td>Insert a coin</td>
      <td>1 for each coin</td>
   </tr>
   <tr>
      <td>i_select_item</td>
      <td>Select an item</td>
      <td>1 for each item<</td>
   </tr>
   <tr>
      <td>i_return_trigger</td>
      <td>Return</td>
      <td>1</td>
   </tr>
   <tr>
      <td>clk</td>
      <td>Clock</td>
      <td>1</td>
   </tr>
   <tr>
      <td>reset_n</td>
      <td>Reset</td>
      <td>1</td>
   </tr>
   <tr>
      <th colspan="3"><strong>Output</strong></th>
   </tr>
   <tr>
      <td>o_output_item</td>
      <td>Get an item</td>
      <td>1 for each item</td>
   </tr>
   <tr>
      <td>o_available_item</td>
      <td>Available items</td>
      <td>1 for each item</td>
   </tr>
   <tr>
      <td>o_return_coin</td>
      <td>Return coins</td>
      <td>1 for each item</td>
   </tr>
</table>

<br>

#### **Code, Report and Results**

---

[Github](https://github.com/Heejinee3/Computer-Architecture/tree/master/Vending-Machine)

<br>

#### **Glossary**

---

[RTL](https://velog.io/@chunjakim/RTL-Register-Transfer-Level)

[FSM](https://velog.io/@chunjakim/FSM-Finite-State-Machine)
