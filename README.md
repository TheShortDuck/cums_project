# cums_project
Project in unified method and stack cache

# Dictionary
stack cache seem to be reffered to as Data cache many places.
Method cache likewise often reffered to as instruction cache.

# Links to articles
- Caching in a Mixed-Criticality 5G Radio Base Station (Emads mail)

## Reference on Patmos (and caches in patmos)

- Patmos: a time-predictable microprocessor https://backend.orbit.dtu.dk/ws/portalfiles/portal/145805464/patmos.pdf
- A Time-predictable Stack Cache https://backend.orbit.dtu.dk/ws/portalfiles/portal/120690215/patstack.pdf
- A Method Cache for Patmos https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6899137
- Stack Caching Using Split Data Caches https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7160125

- The Platin Multi-Target Worst-Case Analysis Tool https://drops.dagstuhl.de/storage/01oasics/oasics-vol121-wcet2024/OASIcs.WCET.2024.2/OASIcs.WCET.2024.2.pdf 
- Static Analysis of Worst-Case Stack Cache Behavior https://dl.acm.org/doi/pdf/10.1145/2516821.2516828

## Related work
- A Survey of Techniques for Reducing Interference in Real-Time Applications on Multicore Platforms https://scispace.com/pdf/a-survey-of-techniques-for-reducing-interference-in-real-e9msev69.pdf
- Data Caches in Multitasking Hard Real-Time Systems https://cgi.cse.unsw.edu.au/~jingling/papers/rtss03.pdf
- A Survey of Techniques for Cache Partitioning in Multicore Processors https://dl.acm.org/doi/10.1145/3062394
- A Survey on Cache Management Mechanisms for Real-Time Embedded Systems https://dspacemainprd01.lib.uwaterloo.ca/server/api/core/bitstreams/5d0a6d3e-90ef-45fc-a4ab-a725d4e91ce9/content
- Making Shared Caches More Predictable on Multicore Platforms https://www.cs.unc.edu/~cjk/papers/ecrts13.pdf

# Initial timeplan
### w7
Research

### w8
Architecture

### w9
Simulation and selection 

###  w10
Implementation in HW

### w11
Implementation in HW 

### w12
Report writing

### w13
Buffer & presentaion

## Initial architecture
Memory space where each of the cahces can grow up to 70% (first come first served)

One will start at max addr and grow down, one from 0 and grow up

Each cache will wrap and eat their own oldest data when 70% is reached (or they meet each other simewhere inbetween 30-70%)

We have to have consideration to when the other cache is allowed to enter the other caches data (cannot be to recent if it has just wrapped itself (has to write some amount of its own old data))

