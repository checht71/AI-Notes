Gives a estimated possible reward for an action taken in a given state.
This function weighs every reward tree by the probability of that path being taken (state-transition function).
$$Q_\pi (s,a) = \sum_n P(s_n',r_n'|S_na_n)(G_t)$$

Here's an example for a tree with 2 layers ahead of $s$:
$$Q_\pi (s,a) = \sum_n P(s_n',r_n'|S_na_n)(r_n+\gamma r_n')$$


For some problems where we have only the number of successes and failures, the Q function is just the successes divided by the failures. In other words, its the experimental results.
