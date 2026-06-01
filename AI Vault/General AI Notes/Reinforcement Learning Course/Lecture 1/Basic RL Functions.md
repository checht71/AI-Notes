## Transition Probability Function
Input the current <span style="color:rgb(0, 112, 192)">state (s)</span> and possible <span style="color:rgb(255, 0, 0)">action (a)</span>, predict the <span style="color:rgb(0, 112, 192)">next state (s')</span> and <span style="color:rgb(0, 176, 80)">reward (r)</span>.
$$P(s',r|s,a) = P(s_{t+1}=s', r_{t+1}=r|s_t=s, a_t=a)$$


## State-Transition Function
Given the a state and an action, what are the chances of some specific state $s'$ being next in the sequence?
$$ P^a_{ss'} = P(s'|s,a) $$
This can also be set to include a reward:
$$P(s',r'|s,a) $$



## Reward Function
Input the <span style="color:rgb(0, 112, 192)">state</span> and <span style="color:rgb(255, 0, 0)">action</span>, predict the next <span style="color:rgb(0, 176, 80)">reward</span>.
$$R(s,a) = E(r|s,a) = \sum r \times \sum P(s',r|s,a)$$

## Return Function
Predicted future <span style="color:rgb(0, 176, 80)">rewards</span>.
$$ G_t = \sum_{k=0} \gamma^k r$$
Where $\gamma$ is the *discount factor*. This is a modifier for uncertainty. It ranges from 0 to 1. The more uncertain or risky a behavior is, the higher the discount factor.
Bonds would have a *lower* discount factor than stocks, for instance.
$k$ is the <span style="color:rgb(255, 192, 0)">episode</span>.

Here's an example for 3 episodes with a discount factor of 0.5:
$$G_t = 0.5^0 r_1 +0.5^1 r_2 +0.5^2 r_3$$



## Q-Function (<span style="color:rgb(255, 0, 0)">Action</span>-Value Function)
Gives a estimated possible reward for an action taken in a given state.
This function weighs every reward tree by the probability of that path being taken (state-transition function).
$$Q_\pi (s,a) = \sum_n P(s_n',r_n'|S_na_n)(G_t)$$

Here's an example for a tree with 2 layers ahead of $s$:
$$Q_\pi (s,a) = \sum_n P(s_n',r_n'|S_na_n)(r_n+\gamma r_n')$$

## V-Function (<span style="color:rgb(0, 112, 192)">State</span>-Value Function)
The V-Function is a probability-based weighted average of the Q-Functions. It is the average predicted reward for the current policy from state $s_t$ forward.
$$ V_\pi (s_t) = \sum_{n=1}^{n_{max}} Q_\pi(s_t, a^n_{t+1}) \cdot P(a^n_{t+1}|s_t)$$
Multiply the Q-Function of $s_t$ by the probability of each next action, then sum them all together.

Alternative function:
$$ V_\pi(s) = E_\pi (G_t|s_t=s)$$


## A-Function (Advantage Function)
The A function is an assessment of each action taken by subtracting the v function from the q function.
$$a_\pi(s,a) = Q_\pi(s,a)-V_\pi(s)$$