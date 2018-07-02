# Artificial Intelligence for the Pacman Game

## Intro

## Search
1. BFS, DFS, UCS, A*
```bash
$ python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=dfs
$ python pacman.py -l bigMaze -p SearchAgent -a fn=bfs -z .5
$ python pacman.py -l bigMaze -p SearchAgent -a fn=ucs
$ python pacman.py -l bigMaze -z .5 -p SearchAgent -a fn=astar,heuristic=manhattanHeuristic
```

2. Corner Problem, Corner Heuristic
```bash
$ python pacman.py -l mediumCorners -p SearchAgent -a fn=bfs,prob=CornersProblem
$ python pacman.py -l mediumCorners -p AStarCornersAgent -z 0.5
```

3. Eating all the Dots
```bash
$ python pacman.py -l trickySearch -p SearchAgent -a fn=astar,prob=FoodSearchProblem,heuristic=foodHeuristic
```

4. SubOptimal Search
```bash
$ python pacman.py -l bigSearch -p ClosestDotSearchAgent -z .5
```

## Multi-Agent
1. Reflex Agent
```bash
$ python pacman.py -p ReflexAgent -l testClassic
```

2. Minimax Agent
```bash
$ python pacman.py -p MinimaxAgent -l minimaxClassic -a depth=4
```

3. Alpha-Beta Pruning
```bash
$ python pacman.py -p AlphaBetaAgent -a depth=3 -l smallClassic
```

4. Expectimax Agent
```bash
$ python pacman.py -p ExpectimaxAgent -l minimaxClassic -a depth=3
```

## Reinforcement Learning

## Tracking

## Classification

## Credits
