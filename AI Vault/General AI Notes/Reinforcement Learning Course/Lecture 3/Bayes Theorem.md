$$ P(y|x) = \frac{P(x|y)P(y)}{P(x)} \propto P(x|y)P(y)$$

$P(y|x)$ = The probability after new evidence. AKA the <span style="color:rgb(255, 192, 0)">posterior </span>
$P(x|y)$ = Some new data that we learn from a test. AKA the <span style="color:rgb(0, 112, 192)">likelihood</span>. 
$P(y)$ = What we go into the equation thinking about $y$. AKA the <span style="color:rgb(0, 176, 80)">prior</span>. 

Multiple measurements improve the testing accuracy.

$P(\bar y)$ is the probability of the second option. For instance, if $P(y) = 70 \%$, $P(\bar y) = 30 \%$

We can use $P(\bar y)$ to calculate $P(x)$ as well.
$$ P(x) = P(x|y)\times P(y) + P(x|\bar y) \times P(\bar y)$$




