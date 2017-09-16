# Idea #

An __exponential object__ $X^Y$ is an [[internal hom]] $[Y,X]$ in a [[cartesian closed category]].  It generalises the notion of [[function set]], which is an exponential object in [[Set]].


# Definition #

The above is actually a complete definition, but here we spell it out.

Let $X$ and $Y$ be objects of a [[category]] $C$ such that all binary [[product]]s with $Y$ exist.  (Usually, $C$ actually has all binary products.)  Then an __exponential object__ is an object $X^Y$ equipped with an __evaluation map__ $ev: X^Y \times Y \to X$ which is universal in the sense that, given any object $Z$ and map $e: Z \times Y \to X$, there exists a unique map $u: Z \to X^Y$ such that
$$ Z \times Y \stackrel{u \times id_Y}\to X^Y \times Y \stackrel{ev}\to X $$
equals $e$.

As with other [[universal construction]]s, an exponential object, if any exists, is [[generalized the|unique up to unique isomorphism]].


# Related notions #

As before, let $C$ be a category and $X,Y\in C$.

+--{: .query}
Mike, you keep insisting that $C$ must have finite products, but $Y$ can be exponentiable as long as all products with *it* exist.  For an example (where $C$ is a slice category), every display morphism (which I haven\'t yet written about at [[context]]) is exponentiable in a dependent type theory with dependent products but (to prevent finite products) without identity types, even though (since not every morphism is display) the relevant slice category lacks some products (since the category of contexts lacks some pullbacks).  ---[[Toby Bartels]]

[[Mike Shulman|Mike]]: Okay.
=--

* If $X^Y$ exists, then we say that $X$ __exponentiates__ $Y$ or that $Y$ is __exponentiable__ by $X$.

* If $Y$ is such that $X^Y$ exists for all $X$, we say that $Y$ is __exponentiable__.  Then $C$ is __[[cartesian closed category|cartesian closed]]__ if it has a [[terminal object]] and every object is exponentiable.

* More generally, a morphism $Y \to A$ is __exponentiable__ when it is exponentiable in the [[over category]] $C/A$.  Then $C$ is __[[locally cartesian closed category|locally cartesian closed]]__ if every morphism is exponentiable.

* Conversely, if $X$ is such that $X^Y$ exists for all $Y$, we say that $X$ __exponentiates__.  Again, $C$ is __cartesian closed__ if it has a terminal object and every object exponentiates.

Dually, a __coexponential object__ in $C$ is an exponential object in the [[opposite category]] $C^{op}$.  A __[[cocartesian closed category]]__ has all of these (and an [[initial object]]).

+--{: .query}
[[Mike Shulman|Mike]]: Is 'cocartesian closed' really good terminology?  The intended interpretation is of course co-(cartesian closed), but it sounds to me more like a cocartesian monoidal category which is closed monoidal.  What about 'cocartesian coclosed?'
=--


# Examples #

Of course, in any cartesian closed category every object is exponentiable and exponentiates.  In general, exponentiable objects are more common and important than exponentiating ones, since the existence of $X^Y$ is usually more related to properties of $Y$ than properties of $X$.

* In [[Top]] (the category of _all_ topological spaces), locally compact Hausdorff spaces are exponentiable.  Note, though, that most [[nice category of spaces|nice categories of spaces]] are cartesian closed.

* There are similar characterizations of exponentiable [[locale]]s and [[topos]]es.

* In [[algebraic set theory]] one often assumes that only small objects (and morphisms) are exponentiable.  This is  analogous to how in material [[set theory] one can talk about the class of functions $Y\to X$ when $Y$ is a set and $X$ a class, but not the other way round.

* In a [[type theory]] with [[dependent product]]s, every display morphism is exponentiable in the category of [[context]]s ---even in a type theory without identity types, so that not every morphism is display and the relevant slice category need not have all products.

However, exponentiating objects do matter sometimes.

* In [Abstract Stone Duality](http://www.paultaylor.eu/ASD/), [[Sierpinski space]] exponentiates.

* [[Toby Bartels]] has [argued](http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html#c023187) that [[predicative mathematics]] can have a set of [[truth value]]s as long as this set doesn\'t exponentiate (or even exponentiates only [[finite set]]s).


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

Now suppose that $C$ is a [[distributive category]].  Then we have these isomorphisms:
*  $X^{Y + Z} \cong X^Y \times X^Z$;
*  $X^0 \cong 1$.

Here $Y + Z$ is a [[coproduct]] of $Y$ and $Z$, while $0$ is an [[initial object]].  Thus in a distributive category, the exponentiable objects are closed under coproducts.  Note that any cartesian closed category with finite coproducts must be distributive, so all of these isomorphisms hold in any closed [[2-rig]].
