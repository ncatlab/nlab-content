
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **Freyd cover** of a [[category]] -- sometimes known as the **Sierpinski cone** or "scone" --  is a special case of Artin gluing: 

given a category $\mathcal{T}$ and a [[functor]] $F: \mathcal{T} \to Set$, the Artin gluing of $F$ is the [[comma category]] $Set \downarrow F$ whose objects are triples $(X, \xi, U)$ where:

* $X$ is a set
* $U$ is an object of $\mathcal{T}$
* $\xi$ is a function $X \to F(U)$.

So the Freyd cover is the special case $F = \mathcal{T} (1, -)$.

## References

You can find more on Artin gluing in this important (and nice) paper:

* Aurelio Carboni, Peter Johnstone, _Connected limits, familial representability and Artin glueing_ , Mathematical Structures in Computer Science 5 (1995), 441--459

plus

* Aurelio Carboni, Peter Johnstone, _Corrigenda to 'Connected limits...'_ , Mathematical Structures in Computer Science 14 (2004), 185--187.

Some of the above material is taken from 

* [[Tom Leinster]], [reply at MathOverflow](http://mathoverflow.net/questions/12136/freyd-cover-of-a-category) 