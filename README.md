# END 497 Line Balancing with Heuristic Algorithm

Problem Definition: In a electronic card producer company, there are lots of defective product and low production line efficiency. Because, there are no order assignment to lines, no operator assginment to produce the cards with a rational method. 


Solution Method: In order the decrease the number of defective unit of product and increase the line efficiency, we developed mathematical models to assign orders to the lines with optimal solution. However, firms orders data is to large to find optimal solution with CPLEX IBM.
Because of that, we developed a heuristic algorithm to assign orders to lines and assign operator to lines for producing electronic cards.

Conclusion: After we develop and run the heuristic algorithm in python, company can complete the monthly orders in 11 days. In addition to that, company has 36 operator for production lines. However, heuristic algorithm need 30 operator with the given order data and bottleneck of the production lines are decreased with optimal number of operators.


If we explain the algorithm in a basic way: 
1) First our data is group by their card types in order to reduce the possible setup times. After that data is sorted by latest start time.
2) We know that which card type will be produce in which type of lines. With the given info, we divide the data in to two sub data by pallets and non_pallets.
3) In the factory there are 9 lines and 3 of them are pallet lines, other 6 of them are non_pallet lines. In order to minimize the cycle time, we divide the orders as much as we can. If we have a pallet order we divide the order 3 equal piece, if we have a non_pallet order we divide the order 6 equal piece.
4) We repeat the step 3 to finish all the orders and then we create a matrix for completion time with cumulative increase. Also, we create 2 more matrix to see sequence of the orders and assign the operators to the line.
5) Lastly, we developed another mathematical model to find have many operator should we have to prevent the bottleneck situation. With that, we match the num of operators with each order.


A heuristic algorithm applied to reduce cycle time and operator assignment to the lines. 

Solutions:


Completion Times (in days):

![completion_time](https://user-images.githubusercontent.com/94453796/165308504-04f89b50-43a8-4d65-a3aa-87a040cb221f.PNG)

Operator Assignments:

![Operator_assignment](https://user-images.githubusercontent.com/94453796/165308672-12db36b8-180c-4e4e-b1e9-4037759d1951.PNG)

Order No:

![Order_no](https://user-images.githubusercontent.com/94453796/165308712-a0d492db-7fb9-4ed6-89e7-f236f80263fc.PNG)


