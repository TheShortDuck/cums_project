# cums_project
Project in unified method and stack cache

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

