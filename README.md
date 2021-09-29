# Comparison of Shortest Path Searching Algorithms
## Dijkstra’s Algorithm <br>
This shortest path algorithm is most commonly used for finding the shortest path from a source vertex to all other vertex. It was conceived by computer scientist Edsger W. Dijkstra in 1956 and published three years later. The original dijkstra’s algorithm does not use min priority queue and runs in O(V2) time where V is the number of nodes. The implementation of this algorithm based on min priority queue implemented using Fibonacci heap brings down the running time by O((E+V)log V). This is asymptotically the fastest known single source shortest path algorithm for arbitrary directed graph with unbounded non-negative weights.

<br><b>Applications :</b>
1) Finding shortest route in a road network (Google Maps).
2) Finding shortest path for a packet in an internet (IP routing).
3) Telephone Networks as well as Flow network.

<br><b>Complexity :</b>
1) Binary Heap as priority queue:- O((E+V) log V).
2) Fibonacci heap : - O(E+V log V).

## Floyd Warshall <br>

We initialize the solution matrix same as the input graph matrix as a first step. Then we update the solution matrix by considering all vertices as an intermediate vertex. The idea is to one by one pick all vertices and update all shortest paths which include the picked vertex as an intermediate vertex in the shortest path. When we pick vertex number k as an intermediate vertex, we already have considered vertices {0, 1, 2, .. k-1} as intermediate vertices. For every pair (i, j) of source and destination vertices respectively, there are two possible cases.
1) k is not an intermediate vertex in shortest path from i to j. We keep the value of p[i][j] as it is.
2) k is an intermediate vertex in shortest path from i to j. We update the value of p[i][j] as p[i][k] + p[k][j].

<br><b>Applications :</b>
1. Finding a regular expression denoting the regular language accepted by a finite automaton (Kleene’s algorithm)
2. Inversion of real matrices (Gauss–Jordan algorithm).
3. Optimal routing.
4. Finding a regular expression denoting the regular language accepted by a finite automation.

<br><b>TIME COMPLEXITY- O(n3)</b>

## Performance:

Calculated on a Peer to Peer Network graph having 16 vertices and 58 edges. 

1.	Dijkstra’s Algorithm	:   <b>0.024s</b>
2.	Floyd Warshall      :   	<b>0.026s</b>

 



