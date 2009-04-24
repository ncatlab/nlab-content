# Idea #

An __exponential object__ $X^Y$ is an [[internal hom]] $[Y,X]$ in a [[cartesian closed category]].  It generalises the notion of [[function set]], which is an exponential object in [[Set]].


# Definition #

The above is actually a complete definition, but here we spell it out.

Given objects $X$ and $Y$ of a [[category]] $C$ with binary [[product]]s, an __exponential object__ is an object $X^Y$ equipped with an __evaluation map__ $ev: X^Y \times Y \to X$ which is universal in the sense that, given any object $Z$ and map $e: Z \times Y \to X$, there exists a unique map $u: Z \to X^Y$ such that
$$ Z \times Y \stackrel{u \times id_Y}\to X^Y \times Y \stackrel{ev}\to X $$
equals $e$.  Note that all [[product]]s with $Y$ must exist if this is to make sense.

As with other [[universal construction]]s, an exponential object, if any exists, is [[generalized the|unique up to unique isomorphism]].


# Related notions #

If $X^Y$ exists, then we say that $X$ __exponentiates__ $Y$ or that $Y$ is __exponentiable__ by $X$.

More generally, an object $Y$ of a category $C$ is __exponentiable__ if all products with $Y$ exist and $X^Y$ exists for every object $X$ of $C$.  Then $C$ is __[[cartesian closed category|cartesian closed]]__ if it has a [[terminal object]] and every object is exponentiable.

More generally, a morphism $Y \to A$ is __exponentiable__ when it is exponentiable in the [[over category]] $C/A$.  Then $C$ is __[[locally cartesian closed category|locally cartesian closed]]__ if every morphism is exponentiable.

+--{: .query}
Wow, really?  I don\'t really use that word, but the other concept seems more important to me.  Although I suppose that this concept gives you theorems like the closure of exponentiable objects under coproduct in a lextensive category.

No matter.  But is there a term for the other way around?  ---[[Toby Bartels]]

[[Mike Shulman|Mike]]: Why do you say the other concept seems more important?  I think in most cases, the existence of $X^Y$ is more related to properties of $Y$ than properties of $X$.  For instance, in [[Top]] $X^Y$ exists whenever $Y$ is locally compact Hausdorff.  Similar characterizations hold for locales and toposes.  In [[algebraic set theory]] one often assumes that only small objects (and morphisms) are exponentiable, analogously to how in material set theory you can talk about the class of functions $Y\to X$ when $Y$ is a set and $X$ a class, but not the other way round.  But no examples come immediately to mind of an object $X$ in a non-cartesian-closed category such that $X^Y$ exists for all $Y$ (other than stupid examples like $X=0$ and $X=1$).

_Toby_:  Yeah, I think was getting things backwards.  But here\'s an example for the other version:  in [Abstract Stone Duality](http://www.paultaylor.eu/ASD/), Sierpinski space exponentiates (to coin a term).  Similarly, a recent comment of mine on the Caf&#233; argued that predicative mathematics can have a set of truth values as long as it doesn\'t exponentiate (or even exponentiates only finite sets).

In fact, I thought of some properties, so I\'m going to go ahead and define my new term.
=--

Conversely, an object $X$ of a [[cartesian monoidal category]] $C$ __exponentiates__ if $X^Y$ exists for every object $Y$ of $C$.  Again, $C$ is __cartesian closed__ if every object is exponentiates.

A __coexponential object__ in $C$ is an exponential object in the [[opposite category]] $C^op$.  A __[[cocartesian closed category]]__ has all of these.

# Properties #

As with other internal homs, the __currying__ isomorphism
$$ hom_C(Z,X^Y) \cong hom_C(Z \times Y,X) $$
is a [[natural isomorphism]] of sets.  By the usual [[Yoneda lemma|Yoneda]] arguments, this isomorphism can be internalized to an isomorphism in $C$:
$$ (X^Y)^Z \cong X^{Y\times Z}. $$
Similarly, $X \cong X^1$, where $1$ is a [[terminal object]].  Thus, a product of exponentiable objects is exponentiable.

Other natural isomorphisms that match equations from ordinary algebra include:
*  $(X \times Y)^Z = X^Z \times Y^Z$;
*  $1^Z \cong 1$.

These show that, in a cartesian monoidal category, a product of exponentiating objects also exponentiates.

Now suppose that $C$ is an [[extensive category]].  Then we have these isomorphisms:
*  $X^{Y + Z} \cong X^Y \times X^Z$;
*  $X^0 \cong 1$.

Here $Y + Z$ is a [[coproduct]] of $Y$ and $Z$, while $0$ is an [[initial object]].  Thus in an extensive category, the exponentiable objects are closed under coproducts.  Note that any cartesian closed category with finite coproducts must be extensive, so all of these isomorphisms hold in any closed [[2-rig]].