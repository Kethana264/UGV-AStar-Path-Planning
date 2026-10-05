# UGV-AStar-Path-Planning
UGV shortest path planning using A* search with randomly generated obstacles.
# UGV Path Planning Using A* Search

## Objective

This project aims to design an algorithm for an Unmanned Ground Vehicle (UGV) that will navigate a 70 x 70 km grid and avoid randomly generated known obstacles while reaching its goal in the shortest possible path.

Three different obstacle densities are considered to study the performance of the path-planning algorithm.

## Problem Setup

- Grid size: 70 × 70 km
- Start position: (0, 0)
- Goal position: (69, 69)
- Obstacles: Randomly generated
- Obstacle densities:
  - Low: 10%
  - Medium: 20%
  - High: 30%

The UGV is capable of horizontal, vertical and diagonal movement.

## Algorithm Used

### A* (A-Star) Search

A* search is a technique for solving the shortest path problem in the presence of obstacles from the initial node to the goal node.

The heuristic function used by A* is:

f(n) = g(n) + h(n)

where:

- g(n) is the actual cost from the start node to the node n.
- h(n) is the estimated cost from a node to the goal.
- f(n) is the cumulative total cost estimated.

Euclidean distance is used as the heuristic function.

## Obstacle Generation

The obstacle environment is not loaded from an external data set, but rather programmed in.

Random obstacles are created at three different densities:

Environment - Obstacle Density

 Low - 10% 
 
 Medium - 20% 
 
 High - 30% 

There are no obstructions at the start or goal positions.

## UGV Movement

The UGV has 8 degrees of freedom for movement:

- Up
- Down
- Left
- Right
- Four diagonal directions

The travel expenses are:

- Horizontal/vertical movement = 1 km
- Diagonal movement = √2 km

## Measures of Effectiveness

The performance of the algorithm is evaluated using:

1. Path Distance – Path traveled by the UGV.
2. Path length: Number of cells in the path.
3. Expanded Nodes – Number of nodes expanded by A*.
4. Execution Time – the amount of time it takes to find the path.
5. Path Success – True if the UGV reached the goal.

## Visualization

The obstacle maps created and the path computed for the UGV is shown for all three densities.

This enables the impact of the increase in obstacles on path planning to be seen.

## Complexity

When using a priority queue for a search for A*:

**Time Complexity:**  
O((V + E) log V)

**Space Complexity:**  
O(V + E)

where:

V = number of nodes in a network grid
The number of connections between nodes (E):


## Conclusion

A* search algorithm was used to develop the shortest path for an UGV in a 70 km × 70 km grid with obstacles placed randomly.

The algorithm was evaluated in low and medium obstacle density and high obstacle density. The resulting paths and Measures of Effectiveness show the impact of obstacle density on path planning, search effort and execution time.
