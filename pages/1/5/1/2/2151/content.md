A __family of supports__ in a [[topological space]] $X$ is a family $\phi$ of closed subsets $S\subset X$ such that

1. if $S_1,S_2\in \phi$ then $S_1\cup S_2\in \phi$;
2. if $S_1\in \phi$ and $S_2\subset S_1$ is _closed_, then $S_2\in \phi$.

In other words, it is an [[ideal]] in the lattice of closed subsets.


Families of supports are used to introduce a variant of __[[sheaf cohomology]] with supports in $\phi$__ and also for developing certain [[homology]] theories using sheaves (see the book by Bredon, Sheaf theory). Especially useful are the so-called paracompactifying families of supports on non-[[paracompact space]]s. 


Let $F$ be a sheaf of [[abelian groups]] over a topological space $X$. Denote by $\Gamma_\phi(X,F)$ the subset of the space of all sections $f\in \Gamma(X,F) = F(X)$ for which $supp\,f\in \phi$. This gives rise to a covariant [[left exact functor]] $F\mapsto \Gamma_\phi(X,F)$. Its right-[[derived functor]]s 

$$H_\phi^k(X,F) := R^k\Gamma_\phi(X,F)$$

are called the __cohomology groups of $X$ with coefficients in the sheaf $F$ and with supports in the family $\phi$ of supports__. Or sometimes one simply says __sheaf cohomology with supports__. 


[[!redirects sheaf cohomology with supports]]