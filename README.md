# Operating Systems Process Management Project 2
This is the second Process Management Project from my Operating Systems class where we add memory management. This includes changes to the PCB and ProcessMgmt classes as well as the additions of the OpenMem and MemoryManager classes. The PCB class contains two new variables, memBase and memLimit, and two new constructors whose parameters are for those variables. The OpenMem class currently just exists to hold the findOpenMem() method which returns T/F depending on whether it finds open memory. It also keeps track of open memory using one PCB's memLimit value(this PCB's ID is 0) and adds the passed PCB to the QMemUsed list if its base memory does not surpass the memory limit. The MemoryManager class simulates adding running processes until memory fills up. Once all processes stop adding, it then simulates memory freeing up by randomly moving them to the QMemOpen list. Once all processes are open, it then sorts the list. The ProcessMgmt class now utilizes a QMemOpen and QMemUsed list to keep track of how much of the available memory each process is using and even returns used to memory to open memory after a process completes.

Since there are two classes with output, I have included two sample output text files named MemMngrSampleOutput.txt and PrcMgmtSampleOutput.txt. The Java files are located under Project2/src/project2 folder.

I completed this assignment using Eclipse and have exported the project as an Eclipse archive zip file. To run the project yourself, simply import the archive named Project2.zip into your workspace using Eclipse.