
$$V(s_t) = r_{t+1} + \gamma V(S_{t+1})$$
$r_{t+1} =$ immediate reward of action
$\gamma V(S_{t+1}) =$ the discounted value of successor state.
You can also do this for multiple layers.

$$V(s) = r_s + \gamma \sum P(s'|s) V(s')$$

The Bellman Equation can also be expressed using matrix form:

$$ \vec v = \vec r + \gamma \vec P \vec v'$$

Also
$$\vec r = \vec v (\vec I - \gamma \vec P)$$
Where $\vec I$ is an identity matrix (diagonal 1s).
The Bellman equation has a high computational complexity.
