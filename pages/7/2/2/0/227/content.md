#Contents#
* automatic table of contents goes here
{:toc}

#Definition#

[The usual definition of ring](http://en.wikipedia.org/wiki/Ring_mathematics#Definition) is equivalent to all of the following:

A (unital, non-commutative) **ring** is (equivalently)

* a [[monoid]] [[internalization|internal to]] [[Ab]].  
* a [[enriched category|category enriched over]] [[Ab]] with one object.
* a [[ringoid]] with one object.

Here $Ab$ is the category of [[abelian group|abelian groups]], made into a monoidal category using the tensor product of abelian groups.  A **commutative** (unital) ring is an [[abelian monoid]] object in [[Ab]].

In usual ring theory people often talk about **nonunital** rings as well: multiplicative [[semigroup]]s with additive [[abelian group]] structure where the multiplication is distributive toward addition; these are semigroup objects in $Ab$.  As in the unital case, if the semigroup is abelian then the ring is said to be **commutative nonunital**.  Note the adjective 'nonunital' is an example of the [[red herring principle]].

#Generalizations#

It is possible to [[internalization|internalise]] the notion of ring in at least two different ways.  Either one can replace the [[Set|category of sets]] in the classical definition with another category $C$, or one can replace $Ab$ in the fancy definition with another category $M$.

## Internalising the sets ##

If $C$ is a [[cartesian monoidal category]], then any [[Lawvere theory]] may be internalised in $C$.  The theory of rings is an example, so we can speak of _ring objects_ in $C$.  Then a ring object in $Set$ is simply a ring.  (This works whether your rings are unital or nonunital, commutative or noncommutative, etc.)  However, not every notion of internal ring takes this form.

The theory of rings is a combination of a monoid (or semigroup, if nonunital) and an abelian group structure. Thus, ring objects are algebras over a composed [[operad]] (or [[monad]]) of a monoid operad and an abelian group operad, using a standard [[distributive law]] for that situation in the sense of operads (or monads), which corresponds to the usual distributive law in the classical definition of a ring.

A particular example of this is a ring in a [[topos]]. In a topos one usually alternatively defines a ring object by the standard set-theoretic definition of a ring, and interpret the formulas in the sense of topos-theoretic semantics. 

Picking a ring object $R$ in a [[topos]] $\mathcal{T}$ promotes it into a [[ringed topos]].

In cartesian categories one can also define the structure of an (abelian) group object as the lifting of the correspoding [[representable presheaf]] to a presheaf into (abelian) groups. This kind of lifting of some algebraic structure in sets to algebraic structure in a cartesian category makes sense when some category of algebras creates the limits needed to define them in sets. 

## Internalising the abelian groups ##

If $M$ is a [[monoidal category]], then we can speak of [[monoid objects]] in $M$.  However, we usually want $M$ to be somewhat like $Ab$ to think of monoid objects in $M$ as internal rings.  For example, if $M$ is the category of abelian [[group objects]] in a cartesian monoidal category $C$, then we recreate the notion of ring object in $C$ from above.  Or, if $M$ is any [[Ab-enriched category]], then it behaves enough like $Ab$ that we may consider its monoid objects as internal rings.  There are yet other examples, however: a [[ring spectrum]] is a monoid object in [[spectra]], even though these are not $Ab$-enriched.

Other examples are [[simplicial ring]]s (as monoids in [[simplicial abelian group]]s) and [[dg-ring]]s, as well as the $A$-rings below.

## Rings over a ring ##

If $K$ is a commutative ring (or especially a [[field]]), then an [[associative algebra]] over $K$ is a monoid object in $K$-[[Mod]]; this is a special case of the previous section.

If $A$ is a noncommutative ring, then a __ring over $A$__, or simply an __$A$-ring__, is a monoid object $R$ in $A$-[[Bimod]] (that is, in $_K Mod _K$).  Every $A$-ring is a ring in the usual sense, in the sense that there is an obvious [[forgetful functor]] to the usual rings. In fact the unit map $A \to R$ is a morphism of rings, and the category of $A$-rings is precisely the [[coslice category]] or under-category $A/Ring$. Thus by category-theoretic rules, one might be led to unconventionally call $A$-rings "rings *under* $A$". Unfortunately, standard name for $A$-rings is "rings *over* $A$", like conventionally calling $k$-algebras the "algebras *over* $K$". 

Unlike for the $k$-algebras, the multiplication $R\times R\to R$ which is the morphism of $A$-bimodules, is not (left) $A$-linear in the *second* factor, but only $A^{op}$-linear (that is, $A$-linear on the right). In other words, the axiom for $K$-algebras $k (r s) = r (k s)$ is not true, for $k\in A$, $r,s\in R$, although $k (r s) = (k r) s$ and $(r s) k = r (s k)$ do hold.  

Both for a discussion for under-over and also for this difference between $K$-algebras and $A$-rings see the Caf&#233;\'s [quick algebra quiz](http://golem.ph.utexas.edu/category/2008/12/a_quick_algebra_quiz.html).

A dual notion to an $A$-ring is an $A$-[[coring]]. 

## Higher rings ##

By replacing in the sentence "a ring is a [[monoid]] in [[Ab]]" the [[abelian category]] [[Ab]] with a [[higher category theory|higher category]] of _symmetric monoidal_ higher groupoids, one obtains higher notion of rings.

Of particular interest is the maximal case of symmetric monoidal [[∞-groupoid]]s and, even more generally, that of [[spectrum|spectra]]. A [[monoid in an (∞,1)-category]] in the [[stable (∞,1)-category of spectra]] is an [[A-infinity-ring]] or [[associative ring spectrum]]. The commutative case is a [[commutative monoid in an (∞,1)-category]]: an [[E-infinity ring]] or [[commutative ring spectrum]].


[[!redirects rings]]
[[!redirects unital ring]]
[[!redirects unital rings]]
[[!redirects associative ring]]
[[!redirects associative rings]]
[[!redirects associative unital ring]]
[[!redirects associative unital rings]]
[[!redirects commutative ring]]
[[!redirects commutative rings]]
[[!redirects commutative unital ring]]
[[!redirects commutative unital rings]]
