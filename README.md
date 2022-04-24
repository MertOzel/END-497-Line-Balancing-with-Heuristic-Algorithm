# END-497-Line-Balancing-with-Heuristic-Algorithm
Before we start to heuristic algorithm, a mathematical model developed and run with CPLEX IBM. However, our database is too big for solve in CPLEX.


Because of that, we have start to thing a heuristic algorithm to find a feasible solution in the given line balancing problem.




If we explain the algorithm in a basic way: 
1) First our data is group by their card types in order to reduce the possible setup times. After that data is sorted by latest start time.
2) Second, we know that which card type will be produce in which type of lines. With the given info, we divide the data in to two sub data by pallets and non_pallets.
3) Third, in the factory there are 9 lines and 3 of them are pallet lines, other 6 of them are non_pallet lines. In order to minimize the cycle time, we divide the orders as much as we can. If we have a pallet order we divide the order 3 equal piece, if we have a non_pallet order we divide the order 6 equal piece.
4) Fourth, we repeat the step 3 to finish all the orders and then we create a matrix for completion time with cumulative increase. Also, we create 2 more matrix to see sequence of the orders and assign the operators to the line.
5) Fifth, we developed another mathematical model to find have many operator should we have to prevent the bottleneck situation. With that, we match the num of operators with each order.






A heuristic algorithm applied to reduce cycle time and operator assignment to the lines. 
