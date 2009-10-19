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

* If $X^Y$ exists, then we say that $X$ __exponentiates__ $Y$.

* If $Y$ is such that $X^Y$ exists for all $X$, we say that $Y$ is __exponentiable__.  Then $C$ is __[[cartesian closed category|cartesian closed]]__ if it has a [[terminal object]] and every object is exponentiable.

* More generally, a morphism $Y \to A$ is __exponentiable__ when it is exponentiable in the [[over category]] $C/A$.  Then $C$ is __[[locally cartesian closed category|locally cartesian closed]]__ if every morphism is exponentiable.

* Conversely, if $X$ is such that $X^Y$ exists for all $Y$, we say that $X$ is __exponentiating__.  Again, $C$ is __cartesian closed__ if it has a terminal object and every object is exponentiating.  (The reader should beware that some authors say "exponentiable" for what is here called "exponentiating.")

Dually, a __coexponential object__ in $C$ is an exponential object in the [[opposite category]] $C^{op}$.  A __[[cocartesian coclosed category]]__ has all of these (and an [[initial object]]).

+--{: .query}
_David_: How should entries involving the cocartesian property be organised? How many of the eight possibilities (co)cartesian (co)monoidal (co)closed are worth mentioning? Sixteen with (co)category?

_Toby_:  Potentially all of them, but in practice only the ones that come up.  This one only came up since I wanted to say what a coexponential object was and (in context) it was natural to ask what is a category that has all of these.  But that doesn\'t mean that anybody actually has to create the page, much less the others.  On the other hand, if there\'s something interesting to say about them, then we should have them!

[[Mike Shulman|Mike]]: One place where coexponential objects occur naturally is in algebraic categories whose opposites are viewed as categories of spaces.  So for instance [[ring]]s, or [[frame]]s, or the categories of [[locus|loci]] used in [[synthetic differential geometry]], have some interesting coexponential objects (although none of them is actually cocartesian coclosed).

There is no difference between monoidal and comonoidal (there is a bijection between monoidal structures on $C$ and on $C^{op}$), so your eight possibilities are really only four.  And there aren't many cocartesian closed (or cartesian coclosed) categories; that would mean you have an object $[Y,X]$ and an isomorphism
$$C(Z,[Y,X]) \cong C(Z\sqcup Y, X) \cong C(Z,X) \times C(Y,X)$$
Taking $Z$ to be the initial object, we see that $C(Y,X)\cong *$ for any objects $X,Y$.  So the only cocartesian closed categories are [[(-1)-category|(-1)-categories]].
=--


# Examples #

Of course, in any cartesian closed category every object is exponentiable and exponentiating.  In general, exponentiable objects are more common and important than exponentiating ones, since the existence of $X^Y$ is usually more related to properties of $Y$ than properties of $X$.

* In [[Top]] (the category of _all_ topological spaces), [[locally compact Hausdorff space]]s are exponentiable.  Note, though, that most [[nice category of spaces|nice categories of spaces]] are cartesian closed.

* There are similar characterizations of exponentiable [[locale]]s and [[topos]]es.

* In [[algebraic set theory]] one often assumes that only small objects (and morphisms) are exponentiable.  This is  analogous to how in material [[set theory] one can talk about the class of functions $Y\to X$ when $Y$ is a set and $X$ a class, but not the other way round.

* In a [[type theory]] with [[dependent product]]s, every display morphism is exponentiable in the category of [[context]]s ---even in a type theory without identity types, so that not every morphism is display and the relevant slice category need not have all products.

However, exponentiating objects do matter sometimes.

* In [Abstract Stone Duality](http://www.paultaylor.eu/ASD/), [[Sierpinski space]] is exponentiating.

* [[Toby Bartels]] has [argued](http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html#c023187) that [[predicative mathematics]] can have a set of [[truth value]]s as long as this set is not exponentiating (or even exponentiates only [[finite set]]s).


# Properties #

As with other internal homs, the __currying__ isomorphism
$$ hom_C(Z,X^Y) \cong hom_C(Z \times Y,X) $$
is a [[natural isomorphism]] of sets.  By the usual [[Yoneda lemma|Yoneda]] arguments, this isomorphism can be internalized to an isomorphism in $C$:
$$ (X^Y)^Z \cong X^{Y\times Z}. $$
Similarly, $X \cong X^1$, where $1$ is a [[terminal object]].  Thus, a product of exponentiable objects is exponentiable.

Other natural isomorphisms that match equations from ordinary algebra include:
*  $(X \times Y)^Z = X^Z \times Y^Z$;
*  $1^Z \cong 1$.

These show that, in a cartesian monoidal category, a product of exponentiating objects is also exponentiating.

Now suppose that $C$ is a [[distributive category]].  Then we have these isomorphisms:
*  $X^{Y + Z} \cong X^Y \times X^Z$;
*  $X^0 \cong 1$.

Here $Y + Z$ is a [[coproduct]] of $Y$ and $Z$, while $0$ is an [[initial object]].  Thus in a distributive category, the exponentiable objects are closed under coproducts.

Note that any cartesian closed category with finite coproducts must be distributive, so all of the isomorphisms above hold in any closed [[2-rig]] (such as [[Set]], of course).


[[!redirects exponential objects]]
[[!redirects exponentiable object]]
[[!redirects exponentiable objects]]