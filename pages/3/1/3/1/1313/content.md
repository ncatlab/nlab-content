# Idea #

An __exponential object__ $X^Y$ is an [[internal hom]] $[Y,X]$ is a [[cartesian closed category]].  It generalises the notion of [[function set]], which is an exponential object in [[Set]].

# Definition #

The above is actually a complete definition, but here we spell it out.

Given objects $X$ and $Y$ of a [[category]] $C$ with binary [[product]]s, an __exponential object__ is an object $X^Y$ equipped with an __evaluation map__ $ev: X^Y \times Y \to X$ which is universal in the sense that, given any object $Z$ and map $e: Z \times Y \to X$, there exists a unique map $u: Z \to X^Y$ such that
$$ Z \times Y \stackrel{u \times id_Y}\to X^Y \times Y \stackrel{ev}\to X $$
equals $e$.

As with other [[universal construction]]s, an exponenetial object, if any exists, is [[generalized the|unique up to unique isomorphism]].

# Subsidiary notions #

An object $X$ of a category $C$ is __exponentiable__ if $X^Y$ exists for every object $Y$ of $C$.

A __coexponential object__ in $C$ is an exponential object in the [[opposite category]] $C^op$.

As with other internal homs, the __currying__ isomorphism
$$ hom_C(Z,X^Y) \cong hom_C(Z \times Y,X) $$
is a [[natural isomorphism]].