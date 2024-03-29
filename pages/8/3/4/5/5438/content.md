
# Banach bundles
* table of contents
{: toc}

## Idea

A Banach bundle is a [[bundle]] in which every [[fibre]] is a [[Banach space]].  Certain other conditions apply.


## Definitions

A __Banach bundle__ is an [[open map|open]] (necessarily [[surjection|surjective]]) [[continuous map]] of [[Hausdorff topological spaces]] $p\colon Y\to B$, each of whose [[fibers]] carries a structure of a [[complex number|complex]] [[Banach space]], this structure being continuous in the base point (in other words, the global operations $\mathbb{C} \times Y \to Y$ of multiplication by a scalar, $Y \times_B Y \to Y$ of addition and $Y \to \mathbb{R}$ of taking the norm are continuous) and such that for every [[net]] $\{y_\alpha\}_{\alpha\in A}$, if ${\|y_{\alpha}\|} \to 0$ and $p(y_\alpha) \to b$, then $y_\alpha \to 0 = 0_b \in p^{-1}(b)$.

We distinguish a different concept of __Banach algebraic bundle__, where the base space $B$ is also a [[Banach algebra]] and the multiplication is defined as a map $\cdot\colon Y\times Y \to Y$ (not only $Y \times_B Y \to Y$), that is we can multiply the points in different fibers, and $p(a \cdot b) = p(a) \cdot p(b)$.

A Banach bundle is a __Hilbert bundle__ if each fiber is a [[separable space|separable]] [[Hilbert space]]. As usual, the inner product can be obtained by the polarization formula $(x,y) \coloneqq \frac{1}{4}({\|x+y\|^2} - {\|x-y\|^2})$ from the norm of a Banach space if the norm satisfies the parallelogram identity.  From this, we infer that for Hilbert bundles, the inner product is continuous as a map $Y \times_B Y \to \mathbb{C}$. Hilbert bundles are important in the study of [[induced representations]] of [[locally compact group]]s, and [[Mackey theory]] in particular; more recently their study is connected to the study of [[Hilbert module]]s.

A __morphism of Banach bundles__ $(p\colon Y \to B)\to (p'\colon Y' \to B)$ over the same base is a morphism of total spaces commuting with the projections, $\mathbb{C}$-linear in each fiber, and preserving the norm. A Banach bundle is sometimes said to be Hilbertizable if it is isomorphic to the underlying Banach bundle of a Hilbert bundle; structurally, there is no difference between a Hilbert bundle and a Hilbertizable Banach bundle (again using the polarisation formula to prove that being a Hilbert space is a [[property-like structure]]).

One also considers Banach $*$-[[star-algebra|algebraic]] bundles, where an antilinear [[involution]] $*$ preserving the norm is involved, is continuous as a global map $Y \to Y$ and is an [[antihomomorphism]] of algebras satisfying $p(y^\ast) = p(y^{-1})$.  


## References

* Wikipedia: [Banach bundle](http://en.wikipedia.org/wiki/Banach_bundle_%28non-commutative_geometry%29)

For Banach bundles see ch. 13 in vol. 1 (from page 125; def. 13.4 on p. 127) and for Banach algebraic bundles see from 783 on in vol. 2 of 

* J. M. G. Fell, R. S. Doran, _Representations of $*$-algebras, locally compact groups, and Banach $*$-algebraic bundles_, Vol. 1. Basic representation theory of groups and algebras. Pure and Applied Mathematics, __125__, Academic Press 1988. xviii+746 pp. [MR90c:46001](http://www.ams.org/mathscinet-getitem?mr=936628) Vol. 2, Banach $*$-algebraic bundles, induced representations, and the generalized Mackey analysis. Pure and Applied Mathematics __126__, Acad. Press 1988. pp. i--viii and 747--1486, [MR90c:46002](http://www.ams.org/mathscinet-getitem?mr=936629)


[[!redirects Banach bundle]]
[[!redirects Banach bundles]]

[[!redirects Banach algebraic bundle]]
[[!redirects Banach algebraic bundles]]

[[!redirects Hilbert bundle]]
[[!redirects Hilbert bundles]]
