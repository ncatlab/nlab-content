
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Distributivity for monoidal structures


There are many variations on what it means for one [[monoidal category|monoidal structure]] on a [[category]] to *distribute* over another.  Here we collect a list of them and remark on their relationships.  Note that our terminology is by no means universal.

The following notions of distributivity exist in a linear hierarchy of less to more general.

* A [[distributive category]] has [[finite product]]s and [[coproducts]] (hence is both [[cartesian monoidal category|cartesian]] and [[cocartesian monoidal category|cocartesian]] monoidal), and the former [[distributive law|distribute]] over the latter, in that the canonical [[morphism]] $(X\times Y) + (X\times Z) \to X\times (Y+Z)$ is an [[isomorphism]].

* A [[distributive monoidal category]] is a [[monoidal category]] with coproducts whose tensor product preserves coproducts in each variable separately.  If it is [[cartesian monoidal category|cartesian monoidal]], then it is exactly a distributive category as above.

* A [[rig category]] (also called a [[bimonoidal category]]) is a category with two monoidal structures, say $\otimes$ and $\oplus$, together with coherent natural distributivity isomorphisms such as $X\otimes (Y\oplus Z) \cong (X\otimes Y) \oplus (X\otimes Z)$.  Generally one requires $\oplus$ to be [[symmetric monoidal category|symmetric]].  If $\oplus$ is a cocartesian structure, then it is exactly a distributive monoidal category as above.

  * A [[bipermutative category]] is a "semistrict" symmetric rig category: both $\otimes$ and $\oplus$ are [[permutative categories]] (symmetric strict monoidal categories) and one of the distributivity isomorphisms is an identity.

* A [[colax-distributive rig category]] is like a rig category, but the distributivity morphisms are not assumed to be invertible.

There are also the following related notions which are not comparable in generality.

* [[2-fold monoidal categories]] and [[duoidal categories]] have two monoidal structures, but rather than a "distributivity" morphism as above, they have transformations $(X\star Y)\odot (Z\star W) \to (X\odot Z) \star (Y\odot W)$.

* A [[linearly distributive category]] also has two monoidal structures, but its comparison morphisms have the form $X\otimes (Y\bullet Z) \to (X\otimes Y)\bullet Z$.

* A [[2-rig]] can mean a lot of different things, perhaps a [[distributive monoidal category]] but perhaps also including [[additive and abelian categories|additivity]] or [[cocomplete category|cocompleteness]].

## Related entries

* [[distributive law]]

* [[distributivity for monoidal structures]]

  * [[distributive monoidal category]]

  * [[bipermutative category]]

  * [[linearly distributive category]]

  * [[rig category]]


