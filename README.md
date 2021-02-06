# Bomb
The raw project is in the main branch and contains executable `bomb`, C script `bomb.c` and a readme file. Files in the `testing` branch are created during debugging. My solution is in `solutions.txt`
* Bomb is a script written by the evil developer.
* There are six phases to the bomb each of which need to be defused by passing a string, otherwise the bomb explodes.

## Skills Tested
* Assembly(x86-64) language comprehension

## Working environment 
Ubuntu 64-bit 20.04
VMware Workstation 15 player

## File description
* `bomb` - The executable that need to be defused by passing strings
* `bomb.c` - Starter code.
* `README` - **Please read this.** This contains some useful information about bomb.c and bomb executable. Possibly some hints too!
* `disassembly.txt` - Assembly code created by my machine for bomb executable. 
	* Use command `objdump -d > disassembly.txt` to generate this file. 
	The hole solution lies in understanding *some important* functions in this assembly.
* `phase2_disassembly.txt` - The disassembly for phase_2 function. 
	* Can generate this either by copying from `disassembly.txt` or by using `disas` command in *gdb* after using a breakpoint at phase_2 
* `symbolTable.txt` - This file lists all the functions and variables in the bomb executable. 
	* Use command `objdump -t > symbolTable.txt` to generate this file
* `solution.txt` - My solution strings

## Strategies
###  * Phase 1
	This phase was quite easy. The only catch is to understand that the argument passed to the `strings_not_equal` function is the starting address of string to be passed. Rest is retrieving the individual characters of the string.
### * Phase 2
	Here the strategy was to understand what the assembly was doing. Annotating each line of the machine code helps.
	
### * Phase 3
  The only thing to focus on is to how to get through the eax comparison at line 6 in disassembly. Have to check scanf as it changes the return register rax. Rest is simple assembly comprehension.

### * Phase 4
  The only knack is to understand a little big chunk of assembly code. Only comprehension for assembly is required.

### * Phase 5
  Its easy. Just need assembly comprehension skills and knowledge of which registers stores input arguments and how.

### * Phase 6
  A little complex as have to understand a lot of assembly. Key is to understand the functionaly of some chunks and move past by getting an abstract idea. Knoledge of structs and linked lists is required for the last chunk of assembly. 

## Skills Acquired
* (x86-64)Assembly comprehension
* Extracting abstractions from machine code

