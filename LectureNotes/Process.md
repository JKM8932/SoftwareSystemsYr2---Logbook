*a [[Process]] is a ==program in execution==*
- so "echo" would be a program
	- the ongoing action of doing "echo" would be a process

- like the abstraction of the running program's machine state:
	- has their own **process ID** (pid)
		- program counter
		- stack & frame pointers


# Describing the process' state

*information describing a process' state is kept in the ==process control block (PCB)==*
- a ==🟢process list== (linked list or array) contains pointers to PCB
	- PCB is essentially a C struct object
	- this allows the OS to manage and switch between processes

- during a **context switch**, a process is stopped:
	- execution state (registers, stack, program counter) is saved in its own PCB
		- (recall PCB is like a struct, it will contain all the info)
	- the OS resumes another process by restoring the saved state from their PCB

- ==🔵essentially like, OS will cycle between a "conceptual" linked list of processes, and to start/continue/end/pause any of them, the PCB of the respective process being interacted with is accessed==


*process states are basically just state machines (quite literally in the name too*
- running -> currently executing
- ready -> descheduled, but is able to run when OS schedules it in
- blocked -> OS awaits for external event until putting process into the queue



# Process API

*essential features of a process API that the OS provides* (Assignment 1)
- Create
	- a way to create new processes 

- Destroy
	- methods to forcefully terminate processes

- Wait
	- processes can be paused until another process finishes

- Control
	- suspending, resuming, or modifying process behaviour

- Status
	- interfaces exist to retrieve process details, like runtime and state



# [[Parent & Child Process]]

