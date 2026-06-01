Thompson sampling is where you just test and test until you can fit a predicted distribution to the actual distribution. It is literally just self-supervised machine learning.

$\mu$ = the mean of the distribution
$\sigma$ = the standard deviation (width) of the distribution

Take a sample (some random point) along a normal distribution and we pretend its the mean. Then you test it and get the actual score. Then you compare the actual score with the sample score to predict how far away your predicted mean is from the actual mean.

You can predict this using the posterior standard deviation $\sigma$. There's an equation for this in the slides.

Then you update the posterior distribution $\mathcal{N}$ using these values. You can think of $\mathcal N$ as our updated prediction of what the actual distribution looks like.
$$ \mathcal N (\mu, \sigma)$$

## Algorithm

$$ \sigma_s = \sqrt{(\frac{1}{100^2}+n)^{-1}}$$
$$ \mu = \sigma_s (\sum^n_{j=1}s_j)$$

Where
$\sigma_s$ = standard deviation of distribution
$\mu$ = mean of distribution
$n$ = number of samples being calculated
$s_j$ = satisfaction score