*(relative to OS system responsibilities) an OS needs to create multiple logical instances of a single physical resource*
- it creates an "illusion" to each software process, that they all have their own independent copies of hardware/software resources
	- (e.g.) each process may write/read from a memory address named "x000F"
		- although multiple processes have the same x000F named, each one has a =="unique virtual address space"== that is named x000F relative to them
			- this means that processes that write to "x000F" might write to different physical memory locations that are just named x000F relative to them
# Important ideas

- Illusions -> always about creating illusions
	- (e.g.) illusion that the system has a large number of CPUs
		- turns a single CPU (or small set of them) into seemingly infinite number of CPUs
		- (it is what helps the ==illusion that many programs run at once==)

	- (e.g.) illusion that each process refer a particular physical memory
		- (in reality, it's a specific virtual memory relative to the process on a random physical memory)

	- (e.g.) illusion that many programs run at once
		- OS switches between multiple programs
		- has a policy to decide which one gets to run next
			- NOT specific (unless specified), just random -> as determined by scheduler
		- "illusion of true parallelism" through pseudo-parallelism



# [[Virtualisation - Illusion Considerations]]

