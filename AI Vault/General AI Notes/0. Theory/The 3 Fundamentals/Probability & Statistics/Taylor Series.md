# [Taylor Series:](https://www.youtube.com/watch?v=9YAaCEA08yM) Approximation on Steroids
#Taylor-Series-Approximation 
- This is how the majority of math is done behind the scenes on computers
- There are a ton of equations such as $e^x$ which can be very difficult to figure out the exact value of for a given $x$ (think of finding even $e^2$).
- The way that calculators find these tricky numbers is to create new, simpler equations which approximate the original in the range of that given x value.
	- Generally, these equations will be more accurate the higher degree of polynomial they are. $$1 + c_1x + c_2x^2 + c_3x^3 + c_nx^n...$$
	_Where $c$ is a constant and $x$ is the value we are trying to approximate at_
	
	That degree number $n$ is called the _order_.
		The #first-order-approximation would look like this:
		$$1 + c_1x^1$$
		The #second-order-approximation would look like this:
		$$1+c_1x+c_2x^2$$
		and so on and so forth... 


- The Taylor Series is how we find these simpler polynomials. 
- The original and approximation should have the same slope and the same y value at a given x.

## Taylor Series Equation:
$$f(x) = \sum_{n=0} ^{\infty} c_n(x-a)^n$$
Where
$$c_n = \frac{f^n(a)}{n!}$$


- $a$ is the $x$ _around_ which I'm approximating
- $x$ is the $x$ value which I would like to determine
- $n$ is the #order to which I would like to approximate (Higher order = more accuracy but also more complexity).



Keep in mind that Taylor Series approximations only work within a very limited range of your x value (this increases slightly with higer orders).