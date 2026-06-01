$\epsilon$ greedy algorithm takes the best action most of the time bust does exploration occasionally (with probability $\epsilon$). The range of $\epsilon$ is 0 to 1.

If $\epsilon = 1$, explore only.
If $\epsilon = 0$, exploit only.

$$ Q_t(a) = \frac{1}{N_t(a)}\sum_{\tau =1}^t r_\tau \prod (a_\tau = a)$$
This algorithm basically just tries a strategy until it stops working and then moves on.


## Problems with the Algorihm
We explore randomly. Due to this, we can end up exploring a bad action we have already explored in the past.
