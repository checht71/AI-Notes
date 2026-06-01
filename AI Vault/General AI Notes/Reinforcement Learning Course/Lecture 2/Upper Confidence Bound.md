The Upper Confidence Bound (UCB) measures the potential of an action. The math symbol for the Upper Confidence Bound is $U_t$.

$$ Q(a) \leq \hat{Q_t}(a) + U_t(a)$$
Where
$Q$ is the actual<span style="color:rgb(0, 176, 80)"> reward</span> value (found after experiment)
$\hat{Q}t$ is the predicted <span style="color:rgb(0, 176, 80)">reward</span> value (Q-Value) using the [[Q-Function]] at time $t$
$U_t$ is the upper confidence bound.

### UCB Algorithm
$$ a^{UCB}_{t+1} = \text{argmax} \hat{Q_t}(a)+ U_t(a)$$

### Finding $U_t$
$$P(Q(a)+\hat{Q_t}(a)+U_t(a)) \leq e^{-2tU_t(a)^2}$$
The higher the number of visits, the lower the upper confidence bound.

$$ U_t(a) = \sqrt{\frac{2 \text{ln}(t-1)}{N_t(a)}}$$
Where $N_t$ = number of trials (AKA number of visits) to a certain action.
