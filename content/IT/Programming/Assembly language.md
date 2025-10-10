---
tags:
  - "#it/ProgrammingLanguages"
---
![[CompilationStage.png]]



![[MemoryStructure_Assembly.png]]



| Segment | Description                                                                                                                                                                                      |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Stack   | Has a Last-in First-out (LIFO) design and is fixed in size. Data in it can only be accessed in a specific order by push-ing and pop-ing data.                                                    |
| Heap    | Has a hierarchical design and is therefore much larger and more versatile in storing data, as data can be stored and retrieved in any order. However, this makes the heap slower than the Stack. |
| Data    | Has two parts: Data, which is used to hold variables, and .bss, which is used to hold unassigned variables (i.e., buffer memory for later allocation).                                           |
| Text    | Main assembly instructions are loaded into this segment to be fetched and executed by the CPU.                                                                                                   |

## IO/Storage Speed

| Component | Speed                             | Size                |
| --------- | --------------------------------- | ------------------- |
| Registers | Fastest                           | Bytes               |
| L1 Cache  | Fastest, other than Registers     | Kilobytes           |
| L2 Cache  | Very fast                         | Megabytes           |
| L3 Cache  | Fast, but slower than the above   | Megabytes           |
| RAM       | Much slower than all of the above | Gigabytes-Terabytes |
| Storage   | Slowest                           | Terabytes and more  |


## Clock Speed & Clock Cycle

![[Clock_Speed_Clock_Cycle.png]]



## Instruction Cycle

![[single_machine_instruction.png]]



| **Instruction** | **Description**                                                                                                                           |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `1. Fetch`      | Takes the next instruction's address from the `Instruction Address Register` (IAR), which tells it where the next instruction is located. |
| `2. Decode`     | Takes the instruction from the IAR, and decodes it from binary to see what is required to be executed.                                    |
| `3. Execute`    | Fetch instruction operands from register/memory, and process the instruction in the `ALU` or `CU`.                                        |
| `4. Store`      | Store the new value in the destination operand.                                                                                           |



![[fetch_decode_execute_cycles.png]]

![[fetch_decode_execute_cycles2.png]]

| Component          | Description                                                                                                                | Example                                  |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| `Instructions`     | The instruction to be processed in the `opcode operand_list` format. There are usually 1,2, or 3 comma-separated operands. | `add rax, 1`, `mov rsp, rax`, `push rax` |
| `Registers`        | Used to store operands, addresses, or instructions temporarily.                                                            | `rax`, `rsp`, `rip`                      |
| `Memory Addresses` | The address in which data or instructions are stored. May point to memory or registers.                                    | `0xffffffffaa8a25ff`, `0x44d0`, `$rax`   |
| `Data Types`       | The type of stored data.                                                                                                   | `byte`, `word`, `double word`            |
https://academy.hackthebox.com/module/85/section/857