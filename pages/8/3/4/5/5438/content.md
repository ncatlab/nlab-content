A __Banach bundle__ is an open surjective continuous map of topological Hausdorff spaces $p:Y\to B$ whose fibers carry a structure of complex Banach spaces, continuous as the fiber moves (in other words, global operations of multiplication with a scalar $\mathbb{C}\times Y\to Y$, addition $Y\times_B Y\to Y$ and norm $Y\to \mathbb{R}$ are continuous) and such that for every [[net]] $\{y_\alpha\}_{\alpha\in A}$, if  $\|y_{\alpha}\|\to 0$ and $p(y_\alpha)\to b$, then $y_\alpha\to 0 = 0_b\in p^{-1}(b)$. 

Distinguish a different concept of __Banach algebraic bundle__ where the base space $B$ is also an algebra and the multiplication is defined as a map $\cdot : Y\times Y\to Y$ (not only $Y\times_B Y\to Y$), that is we can multiply the points in different fibers and $p(a\cdot b) = p(a)\cdot p(b)$. 

A Banach bundle is a __Hilbert bundle__ if each fiber is a separable Hilbert space. The inner product can be obtained by the polarization formula $(x,y) = \frac{1}{4}(\|x+y\|^2-\|x-y\|^2)$ from a norm of a Banach space if the norm satisfies the parallelogram identity. From this formula we infer that for Hilbert bundles, the inner product is continuous as a map $Y\times_B Y\to\mathbb{C}$. Hilbert bundles are important in the study of induced representations of locally compact groups, and Mackey theory in particular; more recently their study is connected to the study of [[Hilbert module]]s.

A __morphism of Banach bundles__ $(p:Y\to B)\to (p':Y'\to B)$ over the same base is a morphism of total spaces commuting with the projections, $\mathbb{C}$-linear in each fiber and preserving the norm. A Banach bundle is sometimes said to be Hilbertizable if it is isomorphic to an underlying Banach bundle of a Hilbert bundle.

One also consider Banach &#8727;-algebraic bundles, where an antilinear involution &#8727; preserving the norm is involved, is continuous as a global map $Y\to Y$ and is an antihomomorphism of algebras satisfying $p(y^\ast) = p(y^{-1})$.  

* wikipedia: [Banach bundle](http://en.wikipedia.org/wiki/Banach_bundle_%28non-commutative_geometry%29)

For Banach bundles see ch. 13 in vol. 1 (from page 125; def. 13.4 on p. 127) and for Banach algebraic bundles see from 783 on in vol. 2 of 

* J. M. G. Fell, R. S. Doran, _Representations of &#8727;-algebras, locally compact groups, and Banach &#8727;-algebraic bundles_, Vol. 1. Basic representation theory of groups and algebras. Pure and Applied Mathematics, __125__, Academic Press 1988. xviii+746 pp. [MR90c:46001](http://www.ams.org/mathscinet-getitem?mr=936628) Vol. 2, Banach &#8727;-algebraic bundles, induced representations, and the generalized Mackey analysis. Pure and Applied Mathematics __126__, Acad. Press 1988. pp. i&#8211;viii and 747&#8211;1486, [MR90c:46002](http://www.ams.org/mathscinet-getitem?mr=936629)

[[!redirects Banach bundles]]
[[!redirects Banach algebraic bundle]]