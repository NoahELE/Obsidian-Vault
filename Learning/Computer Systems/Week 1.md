---
date created: Thursday, March 2nd 2023, 2:31:40 pm
date modified: Thursday, March 2nd 2023, 2:36:23 pm
---

# Week 1

## Introduction to Computer Systems

Key Functionalities:

- hardware abstraction 
- resource management 

## CPU

CPU cycle: fetch - decode - execute 

Registers:

- General registers: hold variables and temporary results
- Specific registers:
    - Program counter
    - Stack pointer
    - PSW (Program Status Word)

## User Vs. Kernel Mode

- Mode bit in PSW gives the current mode
- Code running in user mode:
    - Code running in user mode
    - Can access only the parts of memory allowed by kernel mode code
- Code running in kernel mode:
    - Can issue all instructions
    - Can access all memory 
- Instructions and memory locations whose use could interfere with other processes (e.g., by accessing I/O devices) are privileged

## Memory

Access time: registers < cache < main memory < magnetic disk 

## IO Devices

- device - controller - driver
- accessed via system calls
- can be done using 
  - busy waiting
  - interrupts
  - DMA

## System Calls

Interface between user programs and the operating system

## Process

- running program
- encapsulate all the resource/information needed to run a program

## Address Space (of a process)

- stack
- heap
- data
- text