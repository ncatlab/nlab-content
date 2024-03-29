
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

If $T \colon X\to Y$ is an [[additive functor]] between [[abelian category|abelian categories]] with sufficiently many [[projective object|projectives]] and [[injective object|injectives]], then one defines its __right satellite__ $S^1 T$ and __left satellite__ $S^{-1}T=S_1 T:C\to D$ via the formulas
$$
S^1 T (A) = ker(T(M)\to T(P))
$$
$$
S_1 T (A) = coker(T(Q)\to T(N))
$$
where $0\to M\to P\to A\to 0$ and $0\to A\to Q\to N\to 0$ are short [[exact sequence]]s where $P$ is projective and $Q$ is injective in $X$. 

This definition does not depend on the choice of these exact sequences, and moreover $S^1$ and $S_1$ extend to functors. 

Higher satellites are defined by $S^n T = (S^1)^n T$ and $S^{-n} T = S_n T = (S_1)^n T$ for $n\geq 0$. For every exact sequence $0\to A\to A'\to A''\to 0$ there are natural connecting morphisms such that $S^n T$ (with $-\infty\lt n\lt\infty$) evaluated at $A,A',A''$ compose a long [[exact sequence]].

## Properties

If $T$ is [[exact functor|right exact]] then $S^n T=0$ for all $n\gt 0$ and if $T$ is left exact then $S^n T =0$ for all $n\lt 0$. If $T$ is covariant and $A$ projective then $(S^n T)(A)=0$ for $n\lt 0$, for contravariant $T$ or injective $A$ replace $n\lt 0$ with $n\gt 0$ in the conclusion. 

## References

There is also an axiomatic definition of satellites and their relation to [[derived functor]]s in the case when $T$ is half exact. See 

* [[Henri Cartan]], [[Samuel Eilenberg]], _Homological algebra_, Princeton UP 1953, chapter 3.

There are generalizations to non-[[additive category|additive categories]]. See

* [[George Janelidze|G. Z. Janelidze]], On satellites in arbitrary categories, Bull. Georgian Acad. Sci. __82__ (1976), no. 3, 529-532, in Russian, with a reprint translated in English at [arXiv:0809.1504](http://front.math.ucdavis.edu/0809.1504).

for early work; and also in a bit different setup recent

* [[Alexander Rosenberg|A. Rosenberg]], [Homological algebra of noncommutative 'spaces' I](http://www.mpim-bonn.mpg.de/preprints/send?bid=3623), 199 pages, preprint Max Planck, Bonn: MPIM2008-91. 

or for a shorter presentation, Ch. 3 or so of the survey

* [[Alexander Rosenberg|A. Rosenberg]], _Topics in noncommutative algebraic geometry, homological algebra and K-theory_, preprint MPIM Bonn 2008-57 [pdf](http://www.mpim-bonn.mpg.de/preprints/send?bid=3589)

[[!redirects satellites]]