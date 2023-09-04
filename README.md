1. Name - Vinod Kumar Puttamadegowda

2. UTA ID - 1002028556

3. Programming Language and Version Used - Python 3.9.13

4. Code Structure - 
    - Follows Functional and Procedural Programming
    - Functions used in the main program:
        - read(file)
            - To read text file and store the data in a 2d numpy array
        - fetch_all_possible_states(node,cost,level,method,pathway,move)
            - To expand a node and generate all possible child nodes
        - action(tile,direction,move)
            - To find and store the action taken to reach a state
        - path(pathway,node)
            - To find and store the path of a state
        - def heuristic_value(node)
            - To find the total manhattan distance of a state
        - addtofringe(state_n,cost_n,level,path_n,action_n):
            - To append node and its details to the fringe
    - Prcoedural Programming for the methods to solve the puzzle:
        - Check for the validilty of start and goal text files and store them in 2 different arrays
        - Intialising the dictionary called fringe with required initial data
        - Stores the data about all the states, their costs, depths, pathways, actions, heuristic values and f(n) values in a dictionary called fringe
        - Conditional statments for the method to be used, if not found default method is A* 

5. Instructions To Run The Code - 
    - command line command format to run the code is :
        python expense_8_puzzle.py <start-file> <goal-file> <method> <dump-flag>
    - Example commands :
        - BFS algorithm :
            python expense_8_puzzle.py start.txt goal.txt bfs
        - UCS algorithm with dumpFlag true :
            python expense_8_puzzle.py start.txt goal.txt ucs true
    - All the methods need to be passed with only small letters(eg: "bfs") 
    - For the method A* the method argument should be "a\*" 
        - OR even no method argument passed will defaultly run with the A* method
    - start and goal file are required arguments
        - start file can be passed with any different tile locations, as long as the file is in the standard format
    - method and dumpFlag are optional arguments
        - default values for method is a* and for dumpFlag is false
    
6. Contents Of The Directory - 
    - The source code - expense_8_puzzle.py
    - The readme file - readme.txt
    - A start file - start.txt
    - The goal file - goal.txt

    - Note :
        If source code run with dumpFlag true, a dump.txt text file will be created in the directory


7. dump.txt
    - Printing each node and its cost,depth,action done to get to the state, its f(n) value(only for a* search), and its parent state