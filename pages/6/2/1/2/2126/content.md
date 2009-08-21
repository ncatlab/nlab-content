For $X$ a [[topological space]], let $\Pi(X)_\bullet := X^{\Delta_{Top}^\bullet}$ be the [[simplicial set]] of $n$-[[simplex|simplices]] in $X$ -- the [[fundamental ∞-groupoid]] of $X$.

+-- {: .query}
_[[RonnieBrown]]_ Query: Why is the notation $\Pi(X)$ used here? The old notation $S(X)$ or $S^\Delta(X)$ is perfectly clear. The notation $\Pi(X)$ suggests it is some kind of $\infty$-groupoid, but the precise statement of such properties are unclear, and it conflicts with older use of $\Pi$ where some homotopy classes are taken in a more structured situation (filtered spaces, $n$-cubes of spaces) to give well defined strict structures closely related to classical construtions (relative homotopy groups, $n$-adic homotopy groups). 

There should also be some analysis of why globular or simplicial constructions are used rather than cubical ones. 
The case needs to be made, as this analysis of aims is useful. 
=--


For $R$ some [[ring]], let $Maps(\Pi(X),R)^{\bullet}$ be the [[simplicial object|simplicial]] [[ring]] of $R$-valued functions on the spaces of $n$-simplices. The corresponding [[Moore complex|Moore cochain complex]] $C^\bullet(X)$ is the cochain complex whose [[chain homology and cohomology|cochain cohomology]] is the __singular cohomology__ of the space $X$:

+-- {: .standout}
a homogeneous element $\omega_p \in C^p(X)$ is a function on $p$-simplices in $X$.
=--


These form a ring themselves under the [[cup product]].