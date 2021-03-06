#OMSCS 7641 - Machine Learning Assignment 4

This assignment was completed using the generously made boilerplate source code from @juanjose49 at https://github.com/juanjose49/omscs-cs7641-machine-learning-assignment-4

The existing boilerplate included code to run the GridWorld problem. In this assignment I duplicated and modified some of the analysis launchers and runners to the BlockDude program. Execution for both problems are the same. See below for instructions on how to run GridWorld. For BlockDude, execute BlockDudeLauncher. 

##Running the Grid World: Low Difficulty Analysis:

1. While inside the directory structure burlap-assignment-4/src/burlap/assignment4/gridworld/ right-click on the EasyGridWorldLauncher.
2. Go to the “Run As…” section and select “Java Application.
3. All three algorithms will run and the aggregate analysis and optimal policies will be printed to the console.

##Running the Grid World: High Difficulty Analysis:

1. While inside the directory structure burlap-assignment-4/src/burlap/assignment4/gridworld/ right-click on the HardGridWorldLauncher.
2. Go to the “Run As…” section and select “Java Application.
3. All three algorithms will run and the aggregate analysis and optimal policies will be printed to the console.
 
##Running the BlockDude: Level 1 (Low Difficulty) Analysis:

1. While inside the directory structure burlap-assignment-4/src/burlap/assignment4/blockdude/ right-click on the EasyBlockDudeLauncher.
2. Go to the “Run As…” section and select “Java Application.
3. All three algorithms will run and the aggregate analysis and optimal policies will be printed to the console.

##Running the BlockDude: Level 3 (High Difficulty) Analysis:

1. While inside the directory structure burlap-assignment-4/src/burlap/assignment4/blockdude/ right-click on the HardBlockDudeLauncher.
2. Go to the “Run As…” section and select “Java Application.
3. All three algorithms will run and the aggregate analysis and optimal policies will be printed to the console.

##Sample Output
This is the sort of output you get out of the box by running the HardGridWorldLauncher as a Java Application:

```
/////Hard Grid World Analysis/////

This is your grid world:
[0,0,0,0,0,0,0,0,0,0,0]
[0,0,0,0,0,0,0,0,0,0,0]
[0,0,0,0,0,0,0,0,0,0,0]
[0,0,0,1,1,1,1,1,0,0,0]
[0,0,0,1,0,0,0,1,0,0,0]
[0,0,0,1,0,0,0,1,0,0,0]
[0,0,0,1,0,0,0,1,0,0,0]
[0,0,0,1,1,1,1,1,0,0,0]
[0,0,0,0,0,0,0,0,0,0,0]
[0,0,0,0,0,0,0,0,0,0,0]
[0,0,0,0,0,0,0,0,0,0,1]



//Value Iteration Analysis//
Passes: 1
...
Passes: 20
Value Iteration,3752,2228,1150,49,33,31,29,36,31,28,39,29,25,30,28,26,23,23,44,31

This is your optimal policy:
num of rows in policy is 11
[>,>,>,>,>,>,>,>,>,>,>]
[>,>,>,>,>,>,>,>,>,>,^]
[>,>,>,>,>,>,>,>,^,^,^]
[^,^,^,*,*,*,*,*,^,^,^]
[^,^,^,*,*,*,*,*,^,^,^]
[^,^,^,*,*,*,*,*,^,^,^]
[^,^,^,*,*,*,*,*,^,^,^]
[^,^,^,*,*,*,*,*,^,^,^]
[^,^,^,>,>,>,>,>,^,^,^]
[^,^,>,>,>,>,>,>,^,^,^]
[^,>,>,>,>,>,>,>,^,^,*]



Num generated: 1500; num unique: 95
//Policy Iteration Analysis//
Total policy iterations: 1
...
Total policy iterations: 20
Policy Iteration,11375,8124,1514,626,2549,528,214,46,23,25,30,25,21,28,25,23,26,25,25,24
Passes: 19

This is your optimal policy:
num of rows in policy is 11
[>,>,>,>,>,>,>,>,>,>,v]
[>,>,>,>,>,>,>,>,>,^,^]
[>,>,>,>,>,>,>,>,^,^,^]
[^,^,^,*,*,*,*,*,^,^,^]
[^,^,^,*,*,*,*,*,^,^,^]
[^,^,^,*,*,*,*,*,^,^,^]
[^,^,^,*,*,*,*,*,^,^,^]
[^,^,^,*,*,*,*,*,^,^,^]
[^,^,^,>,>,>,>,>,^,^,^]
[^,^,>,>,>,>,>,>,^,^,^]
[^,^,>,>,>,>,>,>,^,^,*]



//Q Learning Analysis//
Q Learning,301,571,191,194,150,302,129,64,137,364,113,114,69,141,155,58,108,89,71,78
Passes: 19

This is your optimal policy:
num of rows in policy is 11
[>,>,^,>,>,>,v,>,^,>,>]
[^,^,>,>,v,>,>,^,>,^,^]
[>,<,>,>,>,^,>,>,>,^,v]
[^,^,^,*,*,*,*,*,^,v,^]
[<,^,<,*,*,*,*,*,v,^,v]
[^,>,<,*,*,*,*,*,>,^,^]
[<,v,^,*,*,*,*,*,^,<,^]
[<,>,<,*,*,*,*,*,>,v,^]
[^,>,>,>,<,>,>,>,^,>,>]
[>,>,^,^,>,v,^,^,>,^,^]
[^,^,v,v,>,>,<,v,<,v,*]



//Aggregate Analysis//

The data below shows the number of steps/actions the agent required to reach 
the terminal state given the number of iterations the algorithm was run.
Iterations,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20
Value Iteration,3752,2228,1150,49,33,31,29,36,31,28,39,29,25,30,28,26,23,23,44,31
Policy Iteration,11375,8124,1514,626,2549,528,214,46,23,25,30,25,21,28,25,23,26,25,25,24
Q Learning,301,571,191,194,150,302,129,64,137,364,113,114,69,141,155,58,108,89,71,78

The data below shows the number of milliseconds the algorithm required to generate 
the optimal policy given the number of iterations the algorithm was run.
Iterations,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20
Value Iteration,224,36,39,44,32,53,67,104,81,86,88,135,121,208,149,100,86,115,102,106
Policy Iteration,18,32,20,51,26,32,39,50,65,51,97,107,111,90,64,80,71,82,162,164
Q Learning,37,50,34,76,29,73,52,44,65,60,28,45,32,23,53,36,34,29,40,40

The data below shows the total reward gained for 
the optimal policy given the number of iterations the algorithm was run.
Iterations,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20
Value Iteration Rewards,-3650.0,-2126.0,-1048.0,53.0,69.0,71.0,73.0,66.0,71.0,74.0,63.0,73.0,77.0,72.0,74.0,76.0,79.0,79.0,58.0,71.0
Policy Iteration Rewards,-11273.0,-8022.0,-1412.0,-524.0,-2447.0,-426.0,-112.0,56.0,79.0,77.0,72.0,77.0,81.0,74.0,77.0,79.0,76.0,77.0,77.0,78.0
Q Learning Rewards,-199.0,-469.0,-89.0,-92.0,-48.0,-200.0,-27.0,38.0,-35.0,-262.0,-11.0,-12.0,33.0,-39.0,-53.0,44.0,-6.0,13.0,31.0,24.0

```
