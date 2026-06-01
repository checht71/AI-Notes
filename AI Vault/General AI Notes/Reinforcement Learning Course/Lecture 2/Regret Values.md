Regret is the difference between the optimal reward and the exploration only reward. This is denoted by $\mathcal{L}$, which reminds me off loss.

$$ \mathcal{L} = \text{optimal} - \text{exploration only}$$

### Calculating the Exploration Only Reward
For this example let's pretend we have 100 chances (episodes) to choose 4 slot machines.
```
machine a: 50%
machine b: 25%
machine c: 75%
machine d: 60%
```
1. Divide the maximum number of episodes by the number of choices. This is the episodes per choice.
	For this example, it would be 100/4 = 25.
$$E/C = \frac{episodes}{choices}$$
2. Multiply that number by the probability of each choice and sum them. It's that simple!
$$r_{exploration} = \sum_c^{C_{max}} \frac{E}{C}P_c$$
$$ r_{exploration} = 25(50\%) + 25(25\%) + 25(75\%) + 25(60\%)$$
$$ = 13.5+6.25+18.75+15$$
