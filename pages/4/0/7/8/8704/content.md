## Idea

A *categorical distribution* is the generic distribution of a random variable with finite image.

## Definition

+-- {: .num_defn}
###### Definition
A random variable $X$ whose image consists of precisely $n\in \mathbb{N}_0$ elements is called to obey a *categorical distribution*.
=--

By definition every random variable with finite image is categorically distributed.

A Bernoulli distribution is precisely a categorical distribution of a random variable whose image-size is $2$.

A categorical distribution is precisely a multinomial distribution $B(n,p_1,...,p_k)$ with $n=1$

Categorical distribution is to multinomial distribution like Bernoulli distribution is to binomial distribution.

The  possible probabilities of a random variable with image-cardinalty $n$ are precisely the points of the standard $(n-1)$-[[nLab:simplex]] embedded into $\mathbb{R}^n$ since we have $1=\sum_{i=0}^{n-1} p_i$. From this viewpoint we see that for a time-homogenous Markov-chain with finite state space the exists  a stationary distribution $\pi$ which is a fixed point of the linear (hence continuous) transformation on the unit simplex associated to the transition matrix $P$ of the chain since any continuous transformation in the unit simplex has a fixed point.

## References

* [wikipedia](http://en.wikipedia.org/wiki/Markov_chain#Finite_state_space)