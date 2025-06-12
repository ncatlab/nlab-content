
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition 

A **rectangular band** or **nowhere commutative semigroup** is a [[semigroup]] which satisfies any of these equivalent conditions

* it is *nowhere commutative* in the sense that $a b = b a$ implies that $a = b$ for all $a$ and $b$. 

* $a b a = a$ for all $a$ and $b$

* $a a a = a$ and $a b c = a c$ for all $a$, $b$, and $c$

However, despite its name, there exist [[commutative semigroup|commutative]] nowhere commutative semigroups, such as the [[empty set|empty]] semigroup and the [[trivial group]]. 

## Properties

* A rectangular band is indeed a [[band]] since the defining identity implies $ x y z = x z$ for all $x,y,z$ whence by taking $y=z=x$ one gets $x x x = x x$ and from the defining identity $x x x=x$ hence $x x = x$. In order to get the first equation expand $x y z$ by substituting $ x z x$ for $x$: $x y z = (x z x) y z = x (z (xy) z) = x z \; .$

* If $S$ is a rectangular band, then there exist [[inhabited set|non-empty sets]] $I$ and $J$ such that $S$ is [[isomorphism|isomorphic]] as a [[semigroup]] to $I\times J$ equipped with the [[multiplication]]
$(i, j)(p,q) = (i,q)$ for $i,p\in I$ and $j,q\in J$.

* Every [[band]] $S$ has a decomposition as a [[disjoint union]] $\coprod_{x\in L} R_x$ where $L$ is a semilattice, each $R_x$ is a [[subobject|sub]]-semigroup that is a rectangular band, and $R_x R_y \subseteq R_{x y}$ for every $x$ and $y$. This is a bit weaker than saying we have a [[functor]] from the [[poset]] $L$ to the [[category]] of rectangular bands, because we lack connecting morphisms $R_x \to R_y$.

## The category of rectangular bands

Let $Rect$ be the category of rectangular bands with semigroup homomorphisms as morphisms.

* Since rectangular bands are an equationally defined subclass of the class of all semigroups, $Rect$ is a subvariety of the variety $SGr$ of semigroups and hence enjoys all the usual (co)completeness properties of a variety.

* Since $Rect$ is the 2-valued [[collapsed topos|collapse]] of the [[topos]] $Set\times Set$ it is even a [[cartesian closed category|cartesian closed]] variety. Since the [[distributive law]] holds for (finite) coproducts in cartesian closed categories, $Rect$ is a [[distributive category]]. Since it is not [[locally cartesian closed category|locally cartesian closed]] it is neither a topos nor even  an [[extensive category]]. For more on this see Johnstone ([1990](#Johnstone90)).

## Related concepts

* [[semigroup]]

* [[band]] 

* [[semilattice]]

* [[distributive category]]

* [[reader monad]]

* [[graphic category|graphic monoid]]

* [[collapsed topos]]

## References

* {#Howie76} J. Howie, _An introduction to semigroup theory_, Academic Press 1976.

* {#Johnstone90}[[Peter Johnstone]], _Collapsed toposes and cartesian closed varieties_ , JPAA **129** (1990) pp.446-480.

* N. Kimura, _The structure of idempotent semigroups I_ , Pacific Journal of Mathematics **8** no.2 (1958) pp.257-275. ([pdf](http://msp.org/pjm/1958/8-2/pjm-v8-n2-p07-p.pdf))

See also:

* Wikipedia, *[Nowhere commutative semigroup](https://en.wikipedia.org/wiki/Nowhere_commutative_semigroup)*


[[!redirects rectangular band]]
[[!redirects rectangular bands]]

[[!redirects nowhere commutative semigroup]]
[[!redirects nowhere commutative semigroups]]
