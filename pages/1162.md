If $T:X\to Y$ is an additive functor between abelian categories with sufficiently many projectives and injectives, then one defines its right satellite $S^1 T$ and left satellite $S^{-1}T=S_1 T:C\to D$ via formulas
$$
S^1 T (A) = ker(T(M)\to T(P))
$$
$$
S_1 T (A) = coker(T(Q)\to T(N))
$$
where $0\to M\to P\to A\to 0$ and $0\to A\to Q\to N\to 0$ are short exact sequences where $P$ is projective and $Q$ is injective object in $X$. This definition does not depend on choice of these exact sequences, and moreover $S^1$ and $S_1$ extend to functors. 

Higher satellites are defined by $S^n T = (S^1)^n T$ and $S^{-n} T = S_n T = (S_1)^n T$ for $n\geq 0$. For every exact sequence
$0\to A\to A'\to A''\to 0$ there are natural connecting morphisms such that $S^n T$ (with $-\infty\lt n\lt\infty$) evaluated at $A,A',A''$ compose a long exact sequence.

If $T$ is right exact then $S^n T=0$ for all $n\gt 0$ and if $T$ is left exact then $S^n T =0$ for all $n\lt 0$. If $T$ is covariant and $A$ projective then $(S^n T)(A)=0$ for $n\lt 0$, for contravariant $T$ or injective $T$ exchange $n\lt 0$ with $n\gt 0$ in the conclusion. 

There is also an axiomatic definition of satellites and relation to derived functors in the case when $T$ is half exact. See 

H. Cartan, S. Eilenberg, Homological algebra, Princeton UP 1953, chapter 3.

There are generalizations to non-additive categories. See

G. Z. Janelidze, On satellites in arbitrary categories, Bull. Georgian Acad. Sci. 82 (1976), no. 3, 529-532, in Russian, with a reprint translated in English at <a href="http://front.math.ucdavis.edu/0809.1504">arXiv:0809.1504</a>

for early work; and also in a bit different setup recent

and also 
A. Rosenberg, <a href="http://www.mpim-bonn.mpg.de/preprints/send?bid=3623"> Homological algebra of noncommutative 'spaces' I</a>, 199 pages, preprint Max Planck, Bonn: MPIM2008-91. 