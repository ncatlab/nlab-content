Given a ring $R$, for any left ideal $I\subset R$ and a set $S\ubset R$ define 
$$ (I : S) = \{ r \in R \,|\, rS \subset I \}. $$
This is clearly a left ideal again. The special case $(I:R)$ is a two-sided ideal, namely the maximal ideal of $R$ contained in $I$. If $r\in R$ then we write $(I:r):=(I:\{r}\})$.

A [[filter]] $F$ in the lattice of left ideals in a ring $R$ is a __uniform filter__ if $I\in F$ implies $(I:r)\in F$ for any $r\in R$.  Equivalently, the [[Gabriel composition of filters]] satisfies $F\subset F\bullet \{R\}$.
The Gabriel composition of uniform filters is a uniform filter.
Uniform filters are also called topologizing, because a non-empty set of left ideals of $R$ is a uniform filter iff it is the family of left ideals of $R$, which form an open neighborhood of $0$ in a "linear topology" on $R$. 

The uniform filters of ideals in a ring $R$ bijectively correspond to [[kernel functor]]s on $R$-$\mathrm{Mod}$ (left exact subfunctors of the identity functor). The correspondence goes as follows. If $F$ is a uniform filter, and $M$ in $R$-$\mathrm{Mod}$, define $\sigma_F M$ as the set of all $m\in M$ such that they are annihilated by some left ideal $I$ in $F$. Conversely, given a kernel functor $\sigma$, define a uniform filter $F^\sigma$ to be the filter whose members are all left ideals $I$ such that $\sigma(R/I)=R/I$.

The most important class of uniform filters are [[Gabriel filter]]s.