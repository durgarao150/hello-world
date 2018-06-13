# Problem Statement

Given n number of soldiers with hierarchy. A soldier reports to any other soldier in the group. The highest ranking soldier reports to none (0). The protocol is to salute all the soldiers whom one is directly or indirectly reporting to, and handshake with the rest. Find the number of salutes and handshakes in this group.

### Prerequisites

JDK 7/8 need to be installed to run the program

## Instructions to run the program
```
javac handshake.java
java handshake
```

### Input

Number of soldiers in the group
Array of integers containing the soldiers number the ith soldier reports to

```
5
0 1 1 2 3
```

### Output

Output will give number of salutes and handshakes

```
number of handshakes = 4
number of salutes = 6
```


## Solution

Each soldier will salute his immediate or indirect superior. If a graph is built with the soldiers who reports to none then and connecting all the soldiers reporting to him and so on. For each soldiers the height of the graph will be the number of salutes for the soldier.This can be found using bfs.
Total number of interactions will be nC2
Hence number of handshakes will nC2-number of salutes.
