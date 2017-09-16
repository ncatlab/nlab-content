In general, let $U = (U_i)_{i: I}$ and $V = (V_j)_{j: J}$ be two families of [[objects]] of some [[category]] $C$.  We say that $V$ is a __refinement__ of $U$ if there are a [[function]] $f: J \to I$ of indices and a [[morphism]] $V_j \to U_{f(j)}$ for each $j$.


## Examples ##

Very often we do this in the [[slice category]] $C/X$ for some object $X$.  If you spell this out, then you have families $(U_i \to X)_i$ and $(V_j \to X)_j$ of morphisms to $X$; $V$ is a refinement of $U$ if there are a function $f: J \to I$ and a commutative diagram
\[ \label{slice}
  \array{ 
    V_j &&\to&& U_{f(j)}
    \\
    & \searrow && \swarrow
    \\
    && X
  }
\]
for each $j$.


More specifically, apply this to the poset of [[subobjects]] of $X$.  Then you have families $(U_i \hookrightarrow X)_i$ and $(V_j \hookrightarrow X)_j$ of subobjects of $X$; $V$ is a refinement of $U$ if there are a function $f: J \to I$ and a commutative diagram (eq:slice) for each $j$.


Yet more specifically, apply this to the lattice of [[subsets]] of some set $X$.  Then you have families $(U_i \subseteq X)_i$ and $(V_j \subseteq X)_j$ of subsets of $X$; $V$ is a refinement of $U$ if there is a function $f: J \to I$ such that each $V_j$ is contained in $U_{f(j)}$.


Yet more specifically, let the families of subsets be indexed by themselves.  Then have collections $U \subseteq \mathcal{P}X$ and $V \subseteq \mathcal{P}X$ of subsets of $X$; $V$ is a refinement of $U$ if for each $j$ there is an $i$ such that $V_j$ is contained in $U_i$.

+-- {: .query}
Actually, this definition is slightly weaker than the previous one in the absence of the [[axiom of choice]].  Perhaps in that case the general definition should say that for each $j$ there is an $i$ and a morphism $V_j \to U_i$.
=--


Special cases of this last example include refinement of [[filter]]s and refinement of [[open cover]]s.


On the other hand, you might want to generalise the case of open covers to [[cover]]s or covering [[sieve]]s on a [[site]].  In that case, the general definition still applies; you have covering families $(U_i \to X)_i$ and $(V_j \to X)_j$ of some object $X$; $V$ is a refinement of $U$ if there are a map $f: J \to I$ and a commutative diagram (eq:slice) for each $j$.


[[!redirects refinement of a cover]]