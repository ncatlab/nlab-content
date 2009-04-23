# Idea #

An __exponential object__ $X^Y$ is an [[internal hom]] $[Y,X]$ in a [[cartesian closed category]].  It generalises the notion of [[function set]], which is an exponential object in [[Set]].


# Definition #

The above is actually a complete definition, but here we spell it out.

Given objects $X$ and $Y$ of a [[category]] $C$ with binary [[product]]s, an __exponential object__ is an object $X^Y$ equipped with an __evaluation map__ $ev: X^Y \times Y \to X$ which is universal in the sense that, given any object $Z$ and map $e: Z \times Y \to X$, there exists a unique map $u: Z \to X^Y$ such that
$$ Z \times Y \stackrel{u \times id_Y}\to X^Y \times Y \stackrel{ev}\to X $$
equals $e$.

As with other [[universal construction]]s, an exponential object, if any exists, is [[generalized the|unique up to unique isomorphism]].


# Subsidiary notions #

An object $Y$ of a category $C$ with finite products is __exponentiable__ if $X^Y$ exists for every object $X$ of $C$.  Thus $C$ is cartesian closed just when every object is exponentiable.  More generally, a morphism $Y\to A$ is __exponentiable__ when it is exponentiable in the [[over category]] $C/A$; thus $C$ is [[locally cartesian closed category|locally cartesian closed]] just when every morphism is exponentiable.

+--{: .query}
Wow, really?  I don\'t really use that word, but the other concept seems more important to me.  Although I suppose that this concept gives you theorems like the closure of exponentiable objects under coproduct in a lextensive category.

No matter.  But is there a term for the other way around?  ---[[Toby Bartels]]

[[Mike Shulman|Mike]]: Why do you say the other concept seems more important?  I think in most cases, the existence of $X^Y$ is more related to properties of $Y$ than properties of $X$.  For instance, in [[Top]] $X^Y$ exists whenever $Y$ is locally compact Hausdorff.  Similar characterizations hold for locales and toposes.  In [[algebraic set theory]] one often assumes that only small objects (and morphisms) are exponentiable, analogously to how in material set theory you can talk about the class of functions $Y\to X$ when $Y$ is a set and $X$ a class, but not the other way round.  But no examples come immediately to mind of an object $X$ in a non-cartesian-closed category such that $X^Y$ exists for all $Y$ (other than stupid examples like $X=0$ and $X=1$).
=--

A __coexponential object__ in $C$ is an exponential object in the [[opposite category]] $C^op$.

As with other internal homs, the __currying__ isomorphism
$$ hom_C(Z,X^Y) \cong hom_C(Z \times Y,X) $$
is a [[natural isomorphism]] of sets.  By the usual [[Yoneda lemma|Yoneda]] arguments, this isomorphism can be internalized to an isomorphism in $C$:
$$ (X^Y)^Z \cong X^{Y\times Z}. $$
