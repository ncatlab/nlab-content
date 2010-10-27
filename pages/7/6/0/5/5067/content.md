
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}



Very incomplete!


(I wasn't sure how to title this page, so the name just mentions projective Banach(able) spaces, even though I hope to eventually get onto injective Banach(able) spaces.)

## Definition

Let $P$ be a [[Banach space]] and let $C$ be a strictly positive constant. We say $P$ is **C-projective** or **projective with constant $C$** if, whenever $Y$ is a Banach space, $X$ is a closed subspace of $Y$, and $f:P\to Y/X$ is a continuous linear map, there exists a continuous linear map $g:P\to X$ with $\Vert g \Vert \leq C\Vert f\Vert$ and $qg=f$, where $q:Y\to Y/X$ is the canonical quotient map.


Semadeni (see below for reference) gives a slightly different definition. Slightly paraphrased, it reads as follows: $F$ is a $Ban_1$-projective space if, for any short linear map $\phi: F\to H$ and any short linear map $\pi: G\to H$ which satisfies $\phi(Ball(G))=Ball(H)$, there exists a short linear map $\psi:F\to G$ such that $\phi=\psi\pi$. Here, $Ball(\cdot)$ denotes the closed unit ball of a given Banach space.

The condition that $\phi(Ball(G))=Ball(H)$ is stronger than requiring the canonical induced map $G/\ker\phi \to H$ to be an isometric isomorphism. For instance, let us work momentarily with real Banach spaces, and consider the map $\phi:c_0 \to {\mathbb R}$ defined by $\phi((x_n)) = \sum_{n=1}^\infty x_n/2^n$, where $\mathbb R$ is normed by saying that $1$ has norm $1$. Clearly this is a surjective, short linear map, and one can check that the induced map from $c_0/\ker(\phi)$ to $\mathbb R$ is an isometry. But a little thought shows that $1\notin \phi(Ball(c_0))$.


## Examples

Let $S$ be any [[set]] and let $\ell^1(S)$ be the [[free functor|free]] Banach space on $S$. 
That is: let $Bang$ denote the category of [[Banach space]]s and short linear maps, and let $Ball$ be the functor $Bang\to Set$ which sends a Banach space $X$ to its closed unit ball $Ball(X)$. Then $\ell^1$ is [[left adjoint]] to $Ball$.

In particular, for any set $S$ and Banach space $V$,
$$ Bang(\ell^1(S), V) \cong Set(S, Ball(V)) $$
(This is the more precise version of the statement "bounded linear maps from $\ell^1(S)$ to $V$ correspond to bounded $V$-valued functions on $S$.)

...

Then $\ell^1(S)$ is a $C$-projective Banach space for any $C\gt1$. (When $S$ is uncountable this definitely needs Choice; I guess that when $S$ is countably infinite this can be relaxed to countable Choice.)

...


It turns out that every projective Banach(able) space is [[isomorphic]] as a Banach(able) space to $\ell^1(S)$ for some set $S$. In the separable case this is more or less a consequence of a standard machine which applies more generally and goes by the name of "block bases plus Pelczynski decomposition". The non-separable case was thrashed out a bit later by K&#246;the (citation needed). 

YC has often wondered if this result has any meaningful kinship with the [[Nielsen-Schreier theorem]]. He usually ends up deciding "probably not".


## Comments on attempts at equivalent formulations ##

In an [[abelian category]] $C$ one sometimes (often?) sees the following definition of a [[projective object]]: an object $P$ is projective in $C$ if the [[hom-functor]] $C(P,\cdot)$ is (right) [[exact functor|exact]]. (I think it is always left exact?)

> Urs: yes, because the hom-functor preserves all limits.

Now the [[categories]] of Banach spaces and Banachable spaces each possess notions of [[zero object]], [[kernel]] and [[cokernel]]. So we could define exactness in terms of these. But now 'exactness' in this sense of a [[short exact sequence]] of Banach(able) spaces does not imply exactness of the underlying short exact sequence of [[vector spaces]]!

Put another way: as we (will) have defined it above, projectivity of a Banach space $P$ is different from asking that the functor $\operatorname{hom}(P,\cdot)$ preserves [[epimorphism]]s...

+--{: .query}
[[David Roberts]]: I suppose it's about asking what you want to do with said projective objects - projective resolutions? Calculate some sort of cohomology? Know that every epimorphism (or analogous map - perhaps the quotient map of a ses?) to a projective object splits?

[[Yemon Choi]]: Good question, David. The answer is "sort of" - my original background is in Hochschild cohomology of Banach algebras, so I am more concerned about Banach modules (over a fixed Banach algebra) that are projective/injective/flat _in some appropriate sense_ ... Now if one looks up Hochschild coho in something like Weibel's book, defined for R-bimodules where R is a k-algebra, then the theory works much better if all short exact sequences in k-bimod split. This is fine, with Choice, if k is a field (i.e. we are working with vector spaces and usual algebras) but does not hold in general; and really what makes things work is that every object of Vect is projective in the presence of Choice, i.e. you always have a linear section.

Now to get back to your question: it has been found from experience that the Banach version of Hochschild coho is more likely to behave like the classical case when your algebra and module both have underlying Banach space "toplinearly isomorphic" to $\ell^1$, and maybe even $L^1$ is OK in some circumstances. What seems to be going on here is that $\ell^1$ is a projective Banach space and $L^1$ a flat Banach space... hence my interest, hence this page.

=--

## Properties

### Projective in which category? ##

### K&#246;the's theorem? 


## Terminology: "metrically projective" and "metrically injective"

## Injective Banach spaces ##

Theorem of Kelley-Nachbin and others?

## References

* Z. Semadeni, _Banach spaces of continuous functions, Vol. 1._ Warsaw, 1971