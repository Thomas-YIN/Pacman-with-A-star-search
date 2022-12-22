# Pacman with A* search

## Project description
This repository is for the Assignment #2 in COMP3211 Artificial Intelligence, HKUST. In this homework, I implemented the A* search algorithm that enables the pacman to navigate to a fixed location in the map in the shortest path. Additionally, the Corners Problem is formulated, which asks the pacman to traverse the four corners of the map in the shortest path. I then solved the Corners Problem with a tailored heuristic function.

## Tasks
- [A* Search](#astar)
- [Corners Problem: Formulation](#corner1)
- [Corners Problem: A* Heuristic](#corner2)

### A* Search <a name="astar"></a>

In this task, I implemented the `aStarSearch` function in `search.py`. To test my implementation, run `python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar, heuristic=manhattanHeuristic`

### Corners Problem: Formulation <a name="corner1"></a>

In this task, I formulated the Corners Problem which requires the pacman to find the shortest path through the maze that touches all four corners. I encoded all necessary information by implementing the `CornersProblem` class in `searchAgents.py`. To test my implementation, run `python pacman.py -l tinyCorners -p SearchAgent -a fn=bfs, prob=CornersProblem` and `python pacman.py -l mediumCorners -p SearchAgent\
  -a fn=bfs,prob=CornersProblem`.

### Corners Problem: A* Heuristic <a name="corner2"></a>

In this task, I implemented a tailored heuristic function for solving the Corners Problem using A* search. To be specific, I defined the heuristic to be the sum of the Manhattan distances from the current location to all the corners that hasn't been visited and implemented the `cornersHeuristic` in `searchAgents.py`. To test my implementation, run `python pacman.py -l mediumCorners -p AStarCornersAgent -z 0.5`. Note that it is equivalent to run `python pacman.py -l mediumCorners -p SearchAgent -a fn=aStarSearch, prob=CornersProblem, heuristic=cornersHeuristic`.
