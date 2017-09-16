Given a [[semi-free differential graded algebra]] $\Omega^\bullet A$ over $k$-algebra $A$, a __connection__ in $A$-module $M$ is a $k$-linear map 

$$
\nabla : M\otimes_A\Omega^\bullet A \to M\otimes_A\Omega^{\bullet+1} A
$$

such that for any homogenous element $\omega\in\Omega^k A$ and an element $\chi\in\Omega A$ 

$$
\nabla (\omega\chi) = \nabla(\omega)\chi + (-1)^k\omega\nabla(\chi)
$$

The curvature $F_\nabla$ of the connection $\nabla$ is the restriction of the connection squared to $M$:

$$\nabla\circ\nabla|_M : M\to M\otimes_A\Omega^2 A. $$ 

A connection is __flat__ iff its curvature vanishes. 

+--{.query}

[[Eric]]: I like this algebraic definition. Do you know who it can be traced back to? Koszul? I've come across it via [Dimakis and Muller-Hoissen](http://arxiv.org/abs/gr-qc/9808023).

=--