
*a [[Process]] is a ==program in execution==*
- so "echo" would be a program
	- the ongoing action of doing "echo" would be a process
- each process has its own:
	- ==🔴virtual address space==
	- register values
	- information related to **scheduling and synchronisation**
	- etc...

*because each process has a "virtual space", the physical memory each process gets does not reflect the orderly nature of the "virtual space" set by the OS*
- ==the OS organises virtual memory in an organised manner so that users can allocate memory safely in an optimised way==
	- it's the equivalent of the OS giving us a framework for us to work with 
- ==🔴in reality, the OS then allocates physical memory when available, NOT IN THE SAME ORDERLY FASHION==
	- it does the allocation in its own optimised way (after we have put it in an optimised behaviour)





### Note about (Virtual) Memory - Stack and Heap 

- Stack and heap are usually organised on opposite ends of an entire memory stoage
	- stack usually sits at the top, and grows downward
		- so from xFFFF downward, the more down it goes the more memory in stack
	- heap sits on the opposite end at the bottom, and grows upward
		- so from x0000 upward
- they are organised this way as stack and heap are one of the main memory components at major risk of memory influx
	- stack -> takes local variables and all, tasks, etc.
	- heap -> dynamic memory allocation
- with how they are both the most susceptible suspects, it makes sense to put them on either ends
	- this allows for a much greater headroom in memory overflow in either stack or heap until a system crashes

