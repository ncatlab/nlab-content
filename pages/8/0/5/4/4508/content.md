Given a $k$-Lie algebra $\mathfrak{g}$ over a commutative unital [[ring]] $k$ which is free as a $k$-module, the __Chevalley--Eilenberg chain complex__ is a particular [[projective resolution]] $V_*(\mathfrak{g})\to k$ of the trivial $\mathfrak{g}$-module $k$ in the [[abelian category]] of $\mathfrak{g}$-modules (what is the same as $U\mathfrak{g}$-modules, where $U\mathfrak{g}$ is the universal enveloping algera of $\mathfrak{g}$). Graded components of the underlying $k$-module this resolution is given by

$$
V_p(\mathfrak{g}) = U(\mathfrak{g})\otimes_k \Lambda^p{\mathfrak{g}}
$$

and it has the obvious $U\mathfrak{g}$-module structure by multiplication in the first tensor factor, because $\Lambda^p{\mathfrak{g}}$ is free as a $k$-module.

If $u \in U\mathfrak{g}$ and $x_i\in \mathfrak{g}$ then the differnetial is given by

$$
d(u\otimes x_1 \wedge \cdots \wedge x_p) = 
$$

$$
 = \sum_{i = 1}^p (-1)^{i+1} ux_i \otimes x_1 \wedge \cdots \wedge \hat{x}_i\wedge \cdots \wedge x_p  
+ \sum_{i\lt j} (-1)^{i+j} u\otimes [x_i, x_j] \wedge \cdots \wedge \hat{x}_i\cdots \wedge \hat{x}_j\cdots \wedge x_p 
$$

See also [[Lie algebra homology]], [[Lie algebra cohomology]], [[Chevalley–Eilenberg cochain complex]] and [[Chevalley–Eilenberg algebra]]. 


[[!redirects Chevalley-Eilenberg chain complex]]
[[!redirects Chevalley-Eilenberg chain complexes]]
[[!redirects Chevalley–Eilenberg chain complex]]
[[!redirects Chevalley–Eilenberg chain complexes]]
[[!redirects Chevalley--Eilenberg chain complex]]
[[!redirects Chevalley--Eilenberg chain complexes]]
