+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Additive analytic geometry
+--{: .hide}
[[!include Additive analytic geometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}



## Idea

Additive analytic geometry over the complex number is an analog of classical (multiplicative) complex analytic geometry obtained by replacing the convolution algebra $\ell^1(\N,\C)$ of converging power series of radius $1$ (discrete Mellin transforms) by the algebra $L^1(\R_+,\C)$ of integrable functions (continuous Mellin transforms).
The analog of the complex unit disc $D_m(0,1)=D(0,1)$ is the hyperbolic/additive unit disc
$$D_a(-\infty,0)=\{s,Re(s)\leq 0\}\cup \{-\infty\},$$
and the analog of the affine line $A^1_m=\C$ is the additive affine line
$$A^1_a=\{-\infty\}\cup \C.$$
The main interest of this new geometry is that it has a built in flow (action of $\R_+$ on itself) and its functions are given by Mellin transforms, so that it seems adapted to the spectral study of zeroes of Mellin transforms in a geometric context.

One needs to use Dirac measures/distributions to relate directly the above two types of analytic geometries, by the relation on coordinates given by $z=e^s$ in an archimedean context, and $z=p^{-s}$ in a non-archimedean context.

Higher dimensional spaces may also be considered but the relation with higher dimensional arithmetic schemes is not yet clear, even if these ones may be seen as living in the classical multiplicative context, and probably having additive alter-ego, at least in an adelic formulation of the corresponding Mellin transforms of series of Dirac deltas. It is however not possible to define directly non-discrete Mellin transform with coefficients in a Banach ring such as the ring of integers, so that the relation between arithmetic geometry and multiplicative analytic geometry probably requires an adelic formulation.

Additive analytic geometry also has a non-commutative and automorphic extension
(formulated in spectral terms), that may be useful to study and formulate some problems of automorphic representation theory in a geometric context. For example, the functional equation looks like a kind of pasting of two Mellin automorphic spectrum along the usual automorphic spectrum, in this context.

## A simple example

It is easy to paste two additive unit discs along their boundary $\R$,
that is the spectrum of $L^1(\R)$, to get the multiplicative version of
the projective space $P^1_a(\C)=\{-\infty\}\cup \C\cup \{+\infty\}$ and
the exponential map sends $P^1_a(\C)$ to the usual (multiplicative) projective space $P^1(\C)$. One may also paste two different discs along an annulus.

A full complex geometry with various topologies seems to emerge from these simple considerations.

The zeroes of Mellin transforms define closed subspaces of such spaces, whose complement are stable by the given flow on additive coordinate algebras and on differential forms, so that one may try to develop a Hodge theory in this context (working with real analytic additive functions in the $s$ and $\bar{s}$ coordinates, i.e., Mellin transforms with respect to $x^s x^{\bar{s}}$, and the corresponding analog of the Laplacian; the formal theory with Sobolev spaces seems to carry through to this context, but one still has to check this out since the analog of the Kähler metric remains a bit allusive in our discussion), to try to prove a natural positivity result for the Poincaré duality pairing.




