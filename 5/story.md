**Fixing the Voys Mortal Combat machine**

It's break time at Voy's headquarters, and besides the usual ping pong activities, there are a number of Voys colleagues who want to play a real classic on the Mortal Combat machine. Panic! The computer won't start up. Urgent help is needed, and you have to solve it. After extensive research, you discover a strange infinite loop in the boot code (puzzle input) of the machine. This should not be a problem, but first, the code must be executed in a safe environment.

The boot code is stored in a text file, and each line contains one instruction. Each instruction consists of an operation (acc, jmp, or nop) and an argument (a signed number, for example: +4 and -20). Acc increases or decreases a global variable, also known as the accumulator, by the value given in the argument. For example, acc +7 will increase the value of the accumulator by 7. The accumulator starts with a value of 0. After an acc instruction, the instruction below it will be executed. Jmp jumps to an instruction relative to its own position. The next instruction to be executed can be found by using the argument of the jmp instruction as an offset. For example; jmp +1 will execute the instruction below the current jmp. Jmp -20 will execute the instruction that is 20 lines above the current instruction. Nop does absolutely nothing and stands for No Operation. The program continues with the instruction below the nop.

An example program:

```
nop +0
acc +1
jmp +4
acc +3
jmp -3
acc -99
acc +1
jmp -4
acc +6
```

The program will be executed in this order:

```
nop +0 | 1
acc +1 | 2, 8(!)
jmp +4 | 3
acc +3 | 6
jmp -3 | 7
acc -99 |
acc +1 | 4
jmp -4 | 5
acc +6 |
```

First, the ` nop +0` does nothing. In the next step, the accumulator is increased from  `0` to `1` (`acc +1`). In the next instruction (`jmp +4`), a jump of `4` steps is made to the instruction `acc +1`. This instruction increases the value of the accumulator from `1` to `2`. Then `jmp -4` is executed and the program jumps to `acc +3`. Here, the accumulator is adjusted from `2` to `5`. The `jmp -3` will bring the program back to `acc +1` from the second line. This line has already been executed.

And here we see the program entered an infinite loop and will never stop. The moment the program wants to execute an instruction for the second time is the moment to stop the program. This instruction should not be executed anymore. At the time of stopping the example, the value of the accumulator is `5`. That is the answer for the example.

Now execute the instructions of the puzzle input.

_**If an instruction is to be executed for the second time (thus creating an infinite loop), what is the value of the accumulator?**_
