# A-Algorithm
A-Star Algorithm for shortest path detection

A* Search Algorithm

  
 Explanation
•	Let's say that you have to get through an enormous maze. This maze is so big that it would take hours to find the goal manually. Additionally, once you finish the maze "by foot", you're supposed to finish another one.
•	To make things significantly easier and less time consuming, we'll boil the maze down to a search problem, and come up with a solution that can be applied to any additional maze that we may encounter - as long as it follows the same rules/structure.
	Any time we want to convert any kind of problem into a search problem, we have to define six things:
1.	A set of all states we might end up in
2.	The start and finish state
3.	A finish check (a way to check if we're at the finished state)
4.	A set of possible actions (in this case, different directions of movement)
5.	A traversal function (a function that will tell us where we'll end up if we go a certain direction)
6.	A set of movement costs from state-to-state (which correspond to edges in the graph)
	In simple cases (like this one), where the generated graph consists of a small number of nodes and edges, BFS, DFS and Dijkstra would suffice.
	However, in a real-life scenario, because we are dealing with problems of enormous combinatorial complexity, we know we will have to deal with an enormous amount of nodes and edges. Therefore, we have to use an algorithm that is, in a sense, guided. That is where an informed search algorithm arises, A*.

Informed search problem algorithm would be finding a path from home to work with the aid of your sight (seeing what path brings you closer to your destination) or a map (knowing exactly how far away every single point is from your destination).
•	A* is based on using heuristic methods to achieve optimality and completeness, and is a variant of the best-first algorithm.
1)	When a search algorithm has the property of optimality, it means it is guaranteed to find the best possible solution, in our case the shortest path to the finish state.
2)	When a search algorithm has the property of completeness, it means that if a solution to a given problem exists, the algorithm is guaranteed to find it.

	Each time A* enters a state, it calculates the cost, f(n) (n being the neighboring node), to travel to all of the neighboring nodes, and then enters the node with the lowest value of f(n).
	These values are calculated with the following formula:
f(n)=g(n)+h(n)f(n)=g(n)+h(n)
	g(n) being the value of the shortest path from the start node to node n, and h(n) being a heuristic approximation of the node's value.

•	g (n): The actual cost path from the start node to the current node. 
•	h(n): The actual cost path from the current node to goal node.
•	f (n): The actual cost path from the start node to the goal node.

 For the implementation of A* algorithm we have to use two arrays namely OPEN and CLOSE.
OPEN: An array that contains the nodes that have been generated but have not been yet examined till yet.
CLOSE: An array which contains the nodes which are examined.

1: Start
2: Place the starting node into OPEN and find its f (n) value.
3: Then remove the node from OPEN, having the smallest f (n) value. If it is a goal node, then stop and return to success.
4: Else remove the node from OPEN, and find all its successors.
5: Find the f (n) value of all the successors, place them into OPEN, and place the removed node into CLOSE.
6: Go to Step-2.
7: Exit.
