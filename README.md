# CS61CPU

Look ma, I made a CPU! Here's what I did:

partnership: Yongoh Moon, Gyeongmin Lee

Part A:

amount of works: Yongoh Moon: 50% and Gyeongmin Lee: 50%
Gyeongmin: task1, task2
Yongoh Moon: task2, task3
Gyeongmin works alu.circ for task1 and debug regfile.circ for task2
Yongoh Moon works regfile.circ and works cpu.circ for task3.

Tasks 1 and 2 were the basic sections to implement instructions(ALU) and registers for CPU.
ALU stands for arithmetic and logical units. A subsystem or component of the CPU. Its main goal is to handle arithmetic and logical operations. Arithmetic operations include addition, subtraction, division, and multiplication. Logical operations determine whether a statement is true or false.
When we implement these, we cared about following the spec of the tasks and fitting them into the regfile_harness.circ.
For task 3, we only need to make addi instruction works, so we set 1 and 0 at constant for ImmSel, B, rs2, and ALUSel.
For the rest of the design, we carefully read the spec and followed accordingly. Furthermore, the addi Datapath slide in lec18 was helpful to finish task 3.

Part B:

amount of works:
Gyeongmin Lee: imm_gen.circ and prosessor part in CPU.circ
Yongoh Moon: worked on the rest part of the project.

we divide tasks by zoom meeting.
At first, Gyeongmin Lee worked branch comp and custom tests, but those were wrong. Therefore, Yongoh Moon made new branch comparator and all of the custom tests.

We made a Datapath in circs that it contain cpu, imm_gen, control_logic, branch comp, csr.
In the control logic part, there is PCSel, inst, ImmSel, Breq, Brlt, ALUSel, MenRW, WBSel.
Moreover, in the control_logic.circ, Yongoh Moon divided all bits to check what instruction is. and then, Yongoh Moon made circuit for all control data such as Breq, ASel, Bel, and etc in control_logic by instruction name and types.
In lec20 and review session for midterm 1, we learned control logic truth table that we reference that table.
