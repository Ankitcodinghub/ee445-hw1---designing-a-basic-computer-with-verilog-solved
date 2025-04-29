# ee445-hw1---designing-a-basic-computer-with-verilog-solved
**TO GET THIS SOLUTION VISIT:** [EE445 HW1 – Designing a Basic Computer with Verilog Solved](https://www.ankitcodinghub.com/product/ee445-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;112885&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EE445 HW1 – Designing a Basic Computer with Verilog Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
&nbsp;

You are going to submit your homework via ODTUCLASS as a .zip file containing the relevant source files and your PDF report. Name your file as “HW1 studentid.zip”.

Using code directly taken from any kind of resource, except those provided in

In this homework, you will design Basic Computer I (as described in lecture notes) using Verilog. Then use cocotb to simulate your designs. Finally, you will write a very short report detailing your simulation and results and you can also briefly discuss the keypoints of your design. The report should not contain any code.

1 Operations to Be Implemented

Operations to be implemented are shown in Figure 1. That is all the data-processing and memory operations with indirect/direct interrupts. No input/output operations are required to be implemented. The details about these instructions are given in the basic computer lecture notes. You should use the machine code translations used in the lecture notes which are shown in the figure below. That is 0XXX for AND, 7400 for CLE, etc. Do not design your own.

Figure 1: List of Operations to Be Implemented

Implementations of INP, OUT, SKI, SKO operations are not required.

2 Module Design with Verilog HDL (20% Credits)

To construct the datapath, several modules are needed. In this section, each of them will be described.

2.1 Multiplexer

Implement a W-bit 8 to 1 multiplexer to be used as a bus in your datapath, where W is a parameter specifying the data width of the input.

2.2 Arithmetic Logic Unit (ALU)

Implement a W-bit ALU, where W is a parameter specifying the data width of its inputs. The ALU will have 2 W-bit data inputs named AC and DR, a 1-bit input named E, a 3-bit operation select input and a W-bit result output. The ALU should also have 4 other status output bits: Carry-out (CO), overflow (OVF), negative (N), and zero (Z). E input will be connected to a register that stores the CO. Negative and zero bits are affected by all the ALU operations; whereas, carry-out and overflow can only be affected by arithmetic operations. The ALU operations to be implemented are given in Table 1 and the status descriptions are given in Table 2.

Table 1: ALU Operation Control

ALU Operation Output

Table 2: ALU Status Descriptions

Status Description

CO 1 if there is a Carry-out from add or subtract operations; 0 for logic operations

OVF 1 if the add or subtract operation results in overflow; 0 for logic operations

Z 1 if the result is zero

N 1 if the result is negative

2.3 Register with Load, Reset and Increment

Implement a positive edge triggered register with parallel load, write enable, synchronous reset and increment. The specifications of the register are provided in Table 3. All the operations should take place in the positive clock edge and DATA is always the parallel load input.

Table 3: Register with Synchronous Reset, Write Enable and Increment

Reset Write Enable Increment Operation

0 0 0 A ← A (Retain)

0 0 1 A ← A + 1

0 1 X A ← DATA

1 X X A ← 0

2.4 Memory Unit

For this step, you will implement a word-addressable memory. The module has the inputs of clock, write enable, 16-bit write data, 12-bit input address, and the 16-bit output of read data. Memory should be 4096×16.

Memory addressing should be combinational, read data output should change the moment input address changes.

3 Datapath Design (10% Credit)

Datapath should be the same as the one shown in Figure 2 with addition of the IEN register for the interrupt enable/disable functionality.

Figure 2: Datapath Illustration

4 Controller Design (40 % Credit)

For the interrupts you can assume FGI input of the Basic Computer is asserted correctly, you do not need to store it as I/O is not implemented.

5 Putting The Computer Together

The computer is put together by connecting the datapath with the controller. This will be done in another .v file by instantiating the datapath and the controller and then connecting them with wire variables. This file should be your top level design file.

Your computer should have PC, AR, IR, AC, DR registers as its outputs and clk, FGI as its input. A Verilog file (BC I.v) is given with the homework, you should use that file. This is important as your design will be put through a test-bench as part of the grading.

6 Simulation (30% Credit)

Write a sample test program in assembly language and translate it into machine code. Use at least 10 different instructions.

Prepare a testbench using cocotb to check for the correct operation of your implementation, using the fully connected computer. Load your sample test code to the memory of the basic computer you have implemented and by the help of your testbench, compare register/memory contents with expected results.

One thing to note here is that the test-bench should be fully automated, that is just printing the results and checking them with hand is not expected. You can use prints for your debug purposes but the final test-bench should tell if there is a error in the design or not, and if there is a error where it has happened.

7 Deliverables

You can basically submit your project folder as long as it contains the below elements.

1. All the Verilog codes necessary (reg, mem, mux, ALU, datapath, controller, BC I.v,…).

2. cocotb test bench (.py file, makefile).

3. A short report in PDF format with the assembly program you used for the simulation and the simulation results. You can also briefly discuss the keypoints of your design.
