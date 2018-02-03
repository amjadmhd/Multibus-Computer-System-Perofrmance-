# Multibus-Computer-System-Perofrmance
An example of using SHARPE to evaluate computer system perofrmance.

Based on the model provided in: Marsan, M. A., & Gerla, M. (1982). Markov models for multiple bus multiprocessor systems. IEEE Transactions on Computers, (3), 239-248.

In this example we consider a system with 4 processors, 4 common memories and 2 buses with the following considerations:
* Processors execute on there own private cache and then perform some operations on a common memory.
* The rate of requesting common memories is exponentially distrbuted and defined as Lambda.
* The processor selects a common memory randomly with equal probaility 1/4.
* The rate of releasing the common memory by a processor is exponentially distrbuted and defined as Mu.
* When a memory or bus is not free, the processor will wait.
* The system performance is evaluated as the count of processors executing or accessing the common memory.

The system is modeled as a markov chain, the system is in a state "A-B-C" where:
+ A: The count of processors accessing common memory.
+ B: The count of processors waiting for memories.
+ C: The count of processors waiting for a free bus.

![alt text](Multibus-Computer-System-Perofrmance-/img/MarkovChain442.PNG)


