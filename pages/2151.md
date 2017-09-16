A __family of supports__ in a toplogical space $X$ is a family $\phi$ of closed subsets $S\subset X$ such that

(i) if $S_1,S_2\in \phi$ then $S_1\cup S_2\in \phi$;

(ii) if $S_1\in \phi$ and $S_2\subset S_1$ is _closed_, then $S_2\in \phi$.

Families of supports are used to introduce a variant of [[sheaf cohomology]] __with supports in $\phi$__ and also for developing certain homology theories, using sheaves (see the book by Bredon, Sheaf theory). Especially useful are the so-called paracompactifying families of supports on non-paracompact spaces. 

Let $F$ be a sheaf of abelian groups over a topological space $X$. Denote by $\Gamma_\phi(X,F)$ the subset of the space of all sections $f\in \Gamma(X,F) = F(X)$ for which $supp\,f\in \phi$. This gives rise to a covariant left exact functor $F\mapsto \Gamma_\phi(X,F)$. Its right-derived functors 

$$H_\phi^k(X,F) := R^k\Gamma_\phi(X,F)$$

are called the groups of cohomology of $X$ with coefficients in the sheaf $F$ and with supports in the family $\phi$ of supports. Or sometimes one simply says sheaf cohomology with supports. 