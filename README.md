Controls:
Left Click: Place Start / End / Barriers
Right Click: Erase
Space: Run the Visualizer
C: Clear the Grid

I developed this project to gain a deeper understanding of how pathfinding algorithms work in a 2D environment. While many games use A* logic for NPC movement, I wanted to build a tool that actually shows the process in real-time. Using Pygame, I created an interactive grid where users can place a start point, an end point, and draw walls or obstacles. The program then calculates the most efficient route between the two points, visually highlighting the search area and the final path discovered by the algorithm.

The heart of the project is the A* algorithm, which is more efficient than a standard Breadth-First Search because it uses a heuristic to "guess" the distance to the target. I implemented this using a Manhattan distance formula to calculate the cost of moving between nodes. To keep the search efficient, I utilized a priority queue that always evaluates the most promising nodes first. I also structured the project around a custom Node class, which manages its own state—whether it is an obstacle, a visited area, or part of the final shortest path.

Building a visual tool required more than just the algorithm logic; I had to manage the relationship between the mouse position and the grid coordinates. I wrote a translation function to convert pixels on the screen into specific row and column indices so that users could "draw" barriers smoothly. Another challenge was ensuring the UI remained responsive while the algorithm was running, which I solved by passing a draw function as a lambda into the search loop so the screen could update at every step of the calculation.

In the future, I plan to add more pathfinding options like Dijkstra’s algorithm so that users can compare the speed and efficiency of different methods side by side. I am also looking into adding a feature that allows users to save and load custom maze layouts from a file. This project was a great way to bridge the gap between abstract mathematical concepts and tangible graphical feedback, and it has definitely changed the way I think about navigation in my other game development projects.
