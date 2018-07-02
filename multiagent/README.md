# MultiAgent
</br>
<img src="/multiagent/imgs/pacman_multi_agent.png" alt="MA" width="200px"/>
</br>
## Reflex Agent
A reflex agent will have to consider both food locations and ghost locations
to perform well. This agent acts on actions rather than states
## Minimax Agent
An adversarial search agent that evaluates states based on the Minimax algorithm
which assumes we are playing an adversary that performs optimally
## Alpha-Beta Agent
An adversarial search agent that evaluates states based on the Minimax algorithm
which assumes we are playing an adversary that performs optimally. However, by
using Alpha-Beta pruning, we can explore this tree more efficiently
## Expectimax Agent
As adversarial search agent that evaluates states similar to the Minimax
algorithm (this is a specialized version of the Minimax algorithm) which does
not make the same assumptions. In addition to "min" and "max" nodes of the
traditional minimax tree, this variant has "chance" nodes, which take the
expected value of an event occurring. This also works well with games of chance.
