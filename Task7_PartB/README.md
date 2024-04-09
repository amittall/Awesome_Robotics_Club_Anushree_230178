- First, the grid.png was converted to a NumPy array 5X5 by grayscaling and slicing. This binary grid (adjacency matrix) goes from a start point to a goal point, where 0 represents a free space (yellow colour), and 1 represents an obstacle (blue colour). 

- Used the Breadth-First Search (BFS) algorithm to find the shortest path (other algorithms like Dijkstra and A* can also be used).

- Directions: vectors with possible movements (up, right, down, left) from any position on the grid.
- visited: A set datatype to keep track of the visited nodes 
- queue: A queue that stores tuples of the current position and the path taken to reach that position.

So, while the queue is not empty
  - for dx, dy in directions: next_pos = (current[0] + dx, current[1] + dy) ##adding to x coordinate and y coordinate respectively the operation.
  - then, we check three conditions for next_pos (1) within grid boundaries. 
					         (2) It is a free space (0, not 1). 
					         (3) not in the visited set ( so that we do not revisit and move forward to the goal)
  - update visited, path in queue
- next loop next_pos becomes new current.

BFS used layer-by-layer analysis to see all possibilities


- later adjusted to 1-based indexing (changing the origin[top left corner] from 0,0 to 1,1)
-
- ![WhatsApp Image 2024-04-09 at 23 17 02_dff8525a](https://github.com/amittall/Awesome_Robotics_Club_Anushree_230178/assets/153276096/7c6d5076-b8bb-4b58-8f48-5040311757c0)


referred video -   [https://www.youtube.com/watch?v=KiCBXu4P-2Y] on [Breadth First Search grid shortest path | Graph Theory]
