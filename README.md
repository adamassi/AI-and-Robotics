🤖 AI and Robotics

This repository contains solutions and implementations of various algorithms and tasks explored in the "AI and Robotics" course. Each assignment is organized into separate directories.

📁 Repository Structure

HW1-AIR/

Implementation of search algorithms and pathfinding techniques such as BFS, DFS, A*, and heuristic-based search.

HW2/

Implementation of search- and sampling-based motion planning algorithms in 2D environments.

Includes planners like RCS (Resolution Complete Search), RRT (Rapidly-exploring Random Tree), and RRT*.

🧠 Implemented Algorithms

🔍 HW1 - Search Algorithms

Breadth-First Search (BFS): Explored graph-based search for shortest paths.

Depth-First Search (DFS): Implemented for path exploration and backtracking.

A* Search: Employed heuristics for efficient shortest-path calculation.

🚀 HW2 - Motion Planning Algorithms

RRT (Rapidly-Exploring Random Tree):

Biased sampling technique for goal-directed planning.

Two extension modes:

E1: Extend directly to sampled point.

E2: Extend towards sampled point in fixed step sizes (e.g., 10 units).

Evaluated performance with different goal biases (5% and 40%).

RRT*:

Extension of RRT with rewiring and cost optimization.

Uses k-nearest neighbor approach to improve the cost of the solution tree.

RCS (Resolution Complete Search):

Search-based algorithm using coarse-to-fine strategy.

Operates on an 8-connected grid with two resolution levels:

Coarse movement (e.g., steps of 2 units).

Fine refinement steps (e.g., steps of 1 unit).

Tracks rank and expands the node list based on minimum rank.

🖼️ Results & Visualizations

Below are example outputs of the planning algorithms on the test maps:

🗺️ RCS Result Example (map1)



🟨 Yellow: Obstacles

⚪ White Tree: Explored nodes

🔵 Blue Line: Final path from start to goal

🧭 The RCS planner took both coarse and fine steps to navigate narrow corridors.

🗺️ RRT Result Example (map2)



📐 Demonstrates biased sampling with E2 extension (step size = 10).

🌳 Tree explores feasible regions and connects to the goal efficiently.

📝 Notes

🐍 All planners are implemented in Python using NumPy and Matplotlib.

🧱 Grid-based collision checking and distance metrics are provided in the MapEnvironment.py file.

🔄 RCS is deterministic, while RRT and RRT* are stochastic and averaged over multiple runs.




