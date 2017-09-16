#Definition#

A [[stack]] $X$ is _presented_ by a [[groupoid]] $G$, if it is the stack (then [[differentiable stack|usually]] regarded as a stack on the [[site]] [[Top]] or [[Diff]]) which assigns to each test domain $U$ the category of $G$-principal bundles over $U$

$$
  X := G-Bund(-) : U \mapsto \{G-principal bundles on U\}
  \,.
$$


#Formulation in terms of nonabelian cohomology#

This can be reformulated as follows: for $X$ a [[manifold]] let
$hom(X,G)$ denote the [[internal hom]] of [[groupoid]]s (or of categories with topological or smooth structure), with $X$ regarded as the [[discrete category|discrete]] groupoid over $X$. We can regard this as the groupoid of _trivial_ $G$-principal bundles over $X$:

This is contravariantly functorial in $X$ and indeed yields a groupoid-valued presheaf

$$
  G-TrivBund : X  \mapsto hom(X,G)
$$

the presheaf of trivial $G$-principal bundles.

So the stack presented by $G$ is the [[stackification]] of this groupoid-valued presheaf.

In yet other words this means nothing but that the stack presented by $C$ is the [[nonabelian cohomology]] $H(-,G)$ with coefficients in $G$:

$$
  G-Bund(-) := H(-,G)
  \,.
$$

#Further resources#

There is discussion of this and related aspects in [[Schreiber:Differential Nonabelian Cohomology]] in the [private part](http://ncatlab.org/schreiber/show/HomePage) of the $n$Lab.