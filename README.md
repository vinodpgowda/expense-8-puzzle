# Expense 8 puzzle problem
 
Building an agent to solve a modifed version of the 8 puzzle problem (called the Expense 8 puzzle problem). The task is still to take a 3X3 grid on which 8 tiles have been placed, where you can only move one tile at a time to an adjacent location (as long as it is blank) and figure out the order in which to move the tiles to get it to a desired configuration. However now the number on the tile now also represents the cost of moving that tile (moving the tile marked 6 costs 6).

## Programming Language and Version Used - Python 3.9.13

## Code Structure 

### Follows Functional and Procedural Programming

### Functions used in the main program:

1. read(file)  
    To read text file and store the data in a 2d numpy array

2. fetch_all_possible_states(node,cost,level,method,pathway,move)  
    To expand a node and generate all possible child nodes

3. action(tile,direction,move)  
    To find and store the action taken to reach a state

4. path(pathway,node)  
    To find and store the path of a state

5. def heuristic_value(node)  
    To find the total manhattan distance of a state

6. addtofringe(state_n,cost_n,level,path_n,action_n)  
    To append node and its details to the fringe

### Prcoedural Programming for the methods to solve the puzzle:

1. Check for the validilty of start and goal text files and store them in 2 different arrays  
2. Intialising the dictionary called fringe with required initial data  
3. Stores the data about all the states, their costs, depths, pathways, actions, heuristic values and f(n) values in a dictionary called fringe  
4. Conditional statments for the method to be used, if not found default method is A*  

## Instructions To Run The Code

### command line command format to run the code is :

*python expense_8_puzzle.py <start-file> <goal-file> <method> <dump-flag>*

### Example commands:

- BFS algorithm:  
*python expense_8_puzzle.py start.txt goal.txt bfs*

- UCS algorithm with dumpFlag true:  
*python expense_8_puzzle.py start.txt goal.txt ucs true*

- All the methods need to be passed with only small letters(eg: "bfs")   
    For the method A* the method argument should be "a\*"   
    OR even no method argument passed will defaultly run with the A* method

- start and goal file are required arguments  
    start file can be passed with any different tile locations, as long as the file is in the standard format

- method and dumpFlag are optional arguments  
    default values for method is a* and for dumpFlag is false
    
## Contents Of The Directory

- The source code - expense_8_puzzle.py
- The readme file - readme.txt
- A start file - start.txt
- The goal file - goal.txt

### Note
If source code run with dumpFlag true, a dump.txt text file will be created in the directory


## dump.txt
Printing each node and its cost,depth,action done to get to the state, its f(n) value(only for a* search), and its parent state