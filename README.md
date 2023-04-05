# Undirected-Graph-is-Bipartite-using-BFS

Problem Description
The program creates a graph object and allows the user to determine whether the graph is bipartite.

Problem Solution
1. Create classes for Graph, Vertex and Queue.
2. Create a function is_bipartite that takes a Vertex object v and a set visited as arguments.
3. The function works by painting each vertex a colour opposite to the colour of its neighbours. If it is found not possible to do so, the graph is not bipartite.
4. The function begins by creating an empty set called visited and a Queue object, q.
5. It also creates a dictionary colour which maps each vertex to either 1 or 0 which represent two different colours. The Vertex object passed is mapped to 0.
6. It enqueues the passed Vertex object and also adds it to the set visited.
7. A while loop is created which runs as long as the queue is not empty.
8. In each iteration of the loop, the queue is dequeued and all of its neighbours are enqueued which have not already been visited.
9. In addition to enqueuing, they are also added to the set visited and the colour of each neighbour is set to the colour opposite to the colour of the dequeued element.
10. If a neighbour is found to be already visited and its colour is the same as that of the dequeued element, the graph is not bipartite and False is returned.
11. After the loop is finished, True is returned to indicate that the graph is bipartite.
12. Thus, the function returns True if the connected component containing v is bipartite. It also puts all nodes reachable from the source vertex in the set visited.

Program Explanation
1. An instance of Graph is created.
2. A menu is presented to the user to perform various operations on the graph.
3. To determine whether the graph is bipartite, is_bipartite is called with a vertex from the graph and an empty set visited.
4. If is_bipartite returns True, the graph is not bipartite. Otherwise, if not all vertices were visited, is_bipartite is called again with an unvisited source vertex.
5. This continues until all vertices have been visited or is_bipartite returns False.
6. If all vertices have been visited, the graph is bipartite.

