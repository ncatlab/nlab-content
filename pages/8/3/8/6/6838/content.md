+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The notion of _dg-schemes_ was introduced by [[Maxim Kontsevich]] as
the first approach to [[derived algebraic geometry]], and was further
developed by [[Mikhail Kapranov]] and [[Ionut Ciocan-Fontanine]].

## Definition

A **differential graded scheme** (**dg-scheme**) is a [[scheme]] $(X,
O_X)$ together with a [[sheaf]] $O_X^\bullet$ of nonnegatively graded
commutative [[dg-algebra|differential graded]] $O_X$-[[dg-algebra|algebras]], such that $O_X \to H^0(O_X^\bullet)$ is
[[surjective]].

## Examples

[[Ciocan-Fontanine]] and [[Kapranov]] construct $RQuot(X, F)$, a
derived enhancement of the classical [[Quot scheme]] parametrizing
subsheaves of a given [[coherent sheaf]] $F$ on a smooth projective
[[variety]] $X$ [(1999)](#CiKa1).  Similarly they also construct a
dg-scheme $RHilb_h(X)$, a derived enhancement of the [[Hilbert
scheme]] parametrizing [[subschemes]] of a given [[projective scheme]]
$X$ with [[Hilbert polynomial]] $h$ [(2000)](#CiKa2).  As an
application they construct the [[derived moduli stack]] of [[stable
maps]] of [[curves]] to a given [[projective variety]].

## Relation with derived stacks

There is a [[functor]] from the [[category]] of dg-schemes to the
category of [[derived stacks]] of [[Bertrand Toen]] and [[Gabriele
Vezzosi]].  It takes values in the [[full subcategory]] of 1-geometric
derived stacks, but is not known (or expected) to be [[fully
faithful]].

In particular, the dg-schemes $RQuot(X, F)$ and $RHilb_h(X)$,
discussed above, also induce [[derived stacks]] in the modern sense.

## Related concepts

* [[dg-manifold]]
* [[dg-geometry]]
* [[derived stack]]

## References

A prediction of [[derived moduli spaces]] is spelled out (in a bit different language) in

* M. Kontsevich, _Enumeration of rational curves via torus actions_. The moduli space of curves (Texel Island, 1994), 335--368, Progr. Math. __129__, Birkh&#228;user 1995. MR1363062 (97d:14077), [hep-th/9405035](http://arxiv.org/abs/hep-th/9405035).
{#KontsevichEnum}

The first examples of [[derived moduli spaces]], using dg-schemes, are constructed in

* [[Ionut Ciocan-Fontanine]], [[Mikhail Kapranov]], _Derived Quot
schemes_, 1999,
[arXiv:math/9905174](http://arxiv.org/abs/math/9905174).
{#CiKa1

* [[Ionut Ciocan-Fontanine]], [[Mikhail Kapranov]], _Derived Hilbert
schemes_, 2000,
[arXiv:math/0005155](http://arxiv.org/abs/math/0005155).
{#CiKa2}

* M. Kapranov, _Injective resolutions of BG and derived moduli spaces of local systems_,  J. Pure Appl. Algebra  155  (2001),  no. 2-3, 167--179; [math/alg-geom/9710027](http://arxiv.org/abs/alg-geom/9710027), MR1801413 (2002b:18017)
 {#Kapranov}

* [[Kai Behrend]], _Differential graded schemes I: prefect resolving
algebras_ ([arXiv:0212225](http://arxiv.org/abs/math/0212225))

* [[Kai Behrend]], _Differential Graded Schemes II: The 2-category of
Differential Graded Schemes_
([arXiv:0212226](http://arxiv.org/abs/math/0212226))


[[!redirects dg-schemes]]
[[!redirects dg scheme]]
[[!redirects dg schemes]]
[[!redirects differential graded scheme]]
[[!redirects differential graded schemes]]