For $n$ a [[natural number]], the double factorial $(2n+1)!!$ is defined to be the product $(2n+1)(2n-1)\ldots 1$. Alternatively, 

$$(2n-1)!! = \frac1{2^n} \frac{(2n)!}{n!}$$ 

so that in particular, $(-1)!!$ is defined to be $1$. 

Double-factorials have a number of applications in [[enumerative combinatorics]]. They are particularly prone to appear whenever dealing with [[binomial coefficients]] 

$$\binom{x}{n} = \frac{x(x-1)\ldots (x-n+1)}{n!}$$ 

in the case $x = 1/2$ or $x = -1/2$, or when dealing with middle binomial coefficients $\binom{2n}{n}$, or when dealing with the values of the [[Gamma function]] at half-integers. 

The exponential generating function of $a_n = (2n-1)!!$ is 

$$\sum_{n \geq 0} \frac{a_n x^n}{n!} = \exp(x^2/2)$$ 

which means the double-factorials also tend to crop up in calculations dealing with [[Gaussian integrals]] such as 

$$\int_0^\infty p(x) e^{-x^2/2}\; d x$$ 

for even polynomials $p$, with consequent applications in [[quantum mechanics]]. 

## Combinatorial interpretation 

The double-factorials $a_n = (2n-1)!!$ count the number of [[involutions]] without [[fixed points]] on a set with $2n$ elements, or the number of [[partitions]] of a $(2n)$-element set into $2$-element sets. This follows readily from the exponential generating function expression above, and is related to the [[species]] composition of the exponential species $\exp$ (the terminal object in the category of species) with the species $x^2/2$, defined to be terminal at $2$-element sets and empty at others. 