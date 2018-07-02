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
1. Value Iteration Agent: an offline planner, not a reinforcement learning
agent, and so the relevant training option is the number of iterations of
value iteration it should run (option -i) in its initial planning phase.
This ends up becoming similar to a Reflex Agent.
```bash
$ python gridworld.py -a value -i 5
```

2. Q-Learning Agent: Q-learning agent, which does very little on construction,
but instead learns by trial and error from interactions with the environment
through its update(state, action, nextState, reward) method.

```bash
$ python gridworld.py -a q -k 100
```

We can also use a Q-Learning agent to play Pac-Man!
```bash
$ python pacman.py -p PacmanQAgent -x 2000 -n 2010 -l smallGrid
```

3. Approximate Q-Learning Agent: learns weights for features of states,
where many states might share the same features.

```bash
$ python pacman.py -p ApproximateQAgent -a extractor=SimpleExtractor -x 50 -n 60 -l mediumGrid
```


## Tracking
Pacman spends his life running from ghosts, but things were not always so.
Legend has it that many years ago, Pacman's great grandfather Grandpac learned
to hunt ghosts for sport. However, he was blinded by his power and could only
track ghosts by their banging and clanging! We implement a particle filter
so that Grandpac can hear the ghosts and track them down! Options include:
ExactInference, ParticleFilter, and MarginalInference

```None
$ python busters.py -k 10 -p GreedyBustersAgent -a inference=MarginalInference
```

## Classification

## Credits
