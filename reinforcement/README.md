# Reinforcement Learning

## Value Iteration
This is an offline planner, not a reinforcement learning agent, and so the
relevant training option is the number of iterations of value iteration
it should run in its initial planning phase.

IMG

Note that our value iteration agent does not actually learn from experience.
Rather, it ponders its MDP model to arrive at a complete policy before
ever interacting with a real environment. When it does interact with the
environment, it simply follows the precomputed policy (e.g. it becomes a
reflex agent). This distinction may be subtle in a simulated environment
like a Gridword, but it's very important in the real world, where the real
MDP is not available

Hence enter Q-Learning!!

## Q-learning
Q-learning agent, which does very little on construction, but instead learns by
trial and error from interactions with the environment through its
update(state, action, nextState, reward) method.

IMG

However PacMan fails to win on larger layouts because each board configuration
is a separate state with separate Q-values. He has no way to generalize that
running into a ghost is bad for all positions. Obviously, this approach
will not scale. Hence, we generate an Approximate Q-Learning Agent

## Approximate Q-Learning Agent
This agent learns weights for features of states, where many states might
share the same features. This is most like a neural network without having
to do lots of computations.

The approximate Q-function
takes the following form:
\[
Q(s,a) = \Sum_{i=1}^{n} f_{i}(s,a)w_{i}
\]

where each weight wi is associated with a particular feature fi(s,a). This is
how our Approximate Q-Learning Agent updates:

\[
w_i \leftarrow w_i + \alpha \times difference⋅f_i(s,a)
\]

Note that the difference term is the same as in normal Q-learning, and r
is the experienced reward
