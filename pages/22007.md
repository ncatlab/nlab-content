

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

... [[idempotent]] [[semigroup]] ...

## Definition 

Recall that a _[[band]]_ is a [[semigroup]] in which every [[element]] is [[idempotent]]. 

[[commutative magma|Commutative]] bands are usually known as _[[semilattices]]_. This is the semigroup-theoretic definition, but there is also an [[order theory|order theoretic]] definition: given a semilattice $L$ in this semigroup-theoretic sense, it has a canonical [[partial order]] given by $e\precreq f$ when $e f = e$. So semilattices are also [[posets]].

Finitely generated bands are finite: see [Howie 76, Section IV.4](#Howie76).

Now a _rectangular band_ may be described as a [[semigroup]] satisfying the identity $a b a = a$ for all elements $a$ and $b$. 

## Properties

* A rectangular band is indeed a [[band]] since the defining identity implies
$ x y z = x z$ for all $x,y,z$ whence by taking $y=z=x$ one gets $x x x = x x$ and from the defining identity $x x x=x$ hence $x x = x$. In order to get the first equation expand $x y z$ by substituting $ x z x$ for $x$: $x y z = (x z x) y z = x (z (xy) z) = x z \; .$

* If $S$ is a rectangular band, then there exist [[inhabited set|non-empty sets]] $I$ and $J$ such that $S$ is [[isomorphism|isomorphic]] as a [[semigroup]] to $I\times J$ equipped with the [[multiplication]]
$(i, j)(p,q) = (i,q)$ for $i,p\in I$ and $j,q\in J$.

* Every [[band]] $S$ has a decomposition as a [[disjoint union]] $\coprod_{x\in L} R_x$ where $L$ is a semilattice, each $R_x$ is a [[subobject|sub]]-semigroup that is a rectangular band, and $R_x R_y \subseteq R_{x y}$ for every $x$ and $y$. This is a bit weaker than saying we have a [[functor]] from the [[poset]] $L$ to the [[category]] of rectangular bands, because we lack connecting morphisms $R_x \to R_y$.

## The category of rectangular bands

Let $Rect$ be the category of rectangular bands with semigroup homomorphisms as morphisms.

* Since rectangular bands are an equationally defined subclass of the class of all semigroups, $Rect$ is a subvariety of the variety $SGr$ of semigroups and hence enjoys all the usual (co)completeness properties of a variety.

* Since $Rect$ is the 2-valued [[collapsed topos|collapse]] of the [[topos]] $Set\times Set$ it is even a [[cartesian closed category|cartesian closed]] variety. Since the [[distributive law]] holds for (finite) coproducts in cartesian closed categories, $Rect$ is a [[distributive category]]. Since it is not [[locally cartesian closed category|locally cartesian closed]] it is neither a topos nor even  an [[extensive category]]. For more on this see Johnstone ([1990](#Johnstone90)).

## Some ramifications

* A band $S$ satisfying the [[graphic category| graphic identity]] $x y x = x y$ for all $x$ and $y$ is said to be _left-regular_. Left-regular bands can arise from hyperplane arrangements and there has been work studying [[random walk|random walks]] on these hyperplane arrangements by analysing the semigroup algebras of the associated bands: see [Brown 00](#Brown00) and [Margolis-Saliola-Steinberg 15](#MargolisSaliolaSteinberg15). Left-regular band monoids are also called _graphic monoids_ which are examples of 1-object [[graphic category|graphic categories]].

## Related concepts

* [[distributive category]]

* [[reader monad]]

* [[graphic category|graphic monoid]]

* [[collapsed topos]]

## References

* {#Howie76} J. Howie, _An introduction to semigroup theory_, Academic Press 1976.

* {#Brown00} K. S. Brown, _Semigroups, Semirings, and Markov Chains_, J. Theor. Prob. **13** no.3 (2000) pp.871-938. ([arXiv:math/0006145](https://arxiv.org/abs/math/0006145))


* {#Johnstone90}[[Peter Johnstone]], _Collapsed toposes and cartesian closed varieties_ , JPAA **129** (1990) pp.446-480.

* N. Kimura, _The structure of idempotent semigroups I_ , Pacific Journal of Mathematics **8** no.2 (1958) pp.257-275. ([pdf](http://msp.org/pjm/1958/8-2/pjm-v8-n2-p07-p.pdf))

* {#MargolisSaliolaSteinberg15}  Stuart Margolis, Franco Saliola, [[Benjamin Steinberg]], _Cell complexes, poset topology and the representation theory of algebras arising in algebraic combinatorics and discrete geometry_ ([arXiv:1508.05446](https://arxiv.org/abs/1508.05446))



[[!redirects rectangular bands]]

[[!redirects band]]
[[!redirects bands]]
