This Python (3.6) project shows examples of search algorithms through Pac-Man.

To play a regular game of Pac-Man, run command "python pacman.py"

To see Pac-Man find a fixed food dot with DFS, run commands:
python pacman.py -l tinyMaze -p SearchAgent
python pacman.py -l mediumMaze -p SearchAgent
python pacman.py -l bigMaze -z .5 -p SearchAgent

To see Pac-Man find a fixed food dot with BFS, run commands:
python pacman.py -l mediumMaze -p SearchAgent -a fn=bfs
python pacman.py -l bigMaze -p SearchAgent -a fn=bfs -z .5

To see Pac-Man use UCS with differing cost functions, run commands:
python pacman.py -l mediumMaze -p SearchAgent -a fn=ucs
python pacman.py -l mediumDottedMaze -p StayEastSearchAgent
python pacman.py -l mediumScaryMaze -p StayWestSearchAgent

To see Pac-Man traverse a maze with A* search and Manhattan distance heuristic, run command:
python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic

To see the difference in efficiency between A* and BFS when making Pac-Man find all corners, run commands:
python pacman.py -l tinyCorners -p SearchAgent -a fn=bfs,prob=CornersProblem
python pacman.py -l mediumCorners -p SearchAgent -a fn=bfs,prob=CornersProblem
python pacman.py -l mediumCorners -p AStarCornersAgent -z 0.5

To see Pac-Man find the optimal solution in eating all food pellets in a maze with A* and a certain nontrivial, non-negative, consistent heuristic, run command:
python pacman.py -l trickySearch -p AStarFoodSearchAgent

To see Pac-Man eat all dots with the suboptimal action of eating the closest pellet, run command:
python pacman.py -l bigSearch -p ClosestDotSearchAgent -z .5
