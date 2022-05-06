
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Bimonoids
* table of contents
{: toc}

## Idea 

A bimonoid is something which is both a monoid and a comonoid in a compatible way. The  compatibility is easy to formulate in symmetric monoidal categories and much harder in a nonsymmetric setup. 

## Definition in symmetric monoidal categories

In a [[symmetric monoidal category]], a __bimonoid__ (or __bimonoid object__) is an object $B$ equipped with a structure of a [[monoid]] and a [[comonoid]] which are compatible in one of two equivalent ways: the comultiplication and the counit are morphisms of monoids or the multiplication and the unit are morphisms of comonoids.  The symmetry of the monoidal structure is involved in the definition of the tensor product $B\otimes B$ as monoids and as comonoids.  In terms of [[string diagrams]], the equations expressing the compatibility of the monoidal and comonoidal structures on $B$ may be represented as follows:

<center>
<img src="/nlab/files/bimonoid-eq1.png" height="100" align="middle"> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/nlab/files/bimonoid-eq2.png" height="60" align="middle">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/nlab/files/bimonoid-eq3.png" height="60" align="middle">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="/nlab/files/bimonoid-eq4.png" height="50" align="middle">
</center>

A bimonoid that additionally has an [[antipode]] (a map $s \colon B\to B$ satisfying an axiom that makes it act like "inverses" in a group) is called a **[[Hopf monoid]]**; a Hopf monoid in [[Vect]] is a [[Hopf algebra]].

A bimonoid that is both a [[commutative monoid]] and a [[cocommutative comonoid]] is called **bicommutative**.

## Examples

* A bimonoid in [[Vect]] (with its usual [[tensor product]]) is generally called a __[[bialgebra]]__.

* In a category with [[biproducts]], with the biproduct as the monoidal product, every object is a bimonoid in a unique way ([Caf&#233; post](http://golem.ph.utexas.edu/category/2010/09/bimonoids_from_biproducts.html)).  This bimonoid is bicommutative.

* More generally, in a [[cartesian monoidal category]], every monoid object is a bimonoid in a unique way, with comultiplication being the diagonal map.    Dually, every comonoid object in a cocartesian monoidal category is a bimonoid in a unique way.

* A bimonoid is said to be **special** if comultiplication followed by multiplication is the identity.   The category [[Rel]] has biproducts so every object is a bicommutative bimonoid, but these bimonoids are also special.  The category [[FinRel]] is the free symmetric monoidal category on a special bicommutative bimonoid, namely $1$ with its diagonal as comultiplication and fold map as multiplication.

## Monoidal structure on modules
{#MonoidalStructureOnModules}

If $B$ is a bimonoid in $\mathcal{C}$, then the category $Mod_B$ of $B$-[[modules]] inherits a [[monoidal category|monoidal structure]] such that the [[forgetful functor]] $Mod_B \to \mathcal{C}$ (the "[[fiber functor]]") is a [[strong monoidal functor]].  For $B$-modules $M$ and $N$, we equip the [[tensor product]] $M\otimes N$ in $\mathcal{C}$ with the $B$-action given by
$$
B\otimes (M\otimes N) \xrightarrow{\Delta}
(B\otimes B) \otimes (M\otimes N) \xrightarrow{\cong}
(B\otimes M) \otimes (B\otimes N) \xrightarrow{act \otimes act}
M\otimes N
$$
where $\Delta$ denotes the comultiplication of $B$ as a comonoid.  The bimonoid compatibility axioms are exactly what is needed to make this a $B$-module structure, and coassociativity makes it associative.  Similarly, we use the counit $B\to I$ of $B$ to give the unit object $I$ a $B$-module structure.

If $B$ moreover a [[Hopf monoid]], then $Mod_B$ also inherits a [[closed monoidal category|closed]] monoidal structure if $\mathcal{C}$ has one; see at _[[Hopf monoid]]_.

These relations are known as _[[Tannaka duality]]_ [for monoids/algebras](Tannaka%20duality#ForAlgebraModules), see at _[[structure on algebras and their module categories - table]]_.


## Non-symmetric variants

It is interesting how to generalize this notion in various nonsymmetric situations, for example involving [[braided monoidal category|braidings]], or more generally in [[duoidal categories]], or in relative situations over noncommutative rings (e.g. Takeuchi bialgebroids). In the completely noncommutative situation of the monoidal category of endofunctors, one can look at various compatibilities between [[monad]]s and comonads or monads and tensor products, for example involving distributive laws.

## Related concepts

* [[Hopf monoid]], [[Frobenius monoid]]

## References

As far as compatibility with tensor product is concerned, there is a notion of a bimonad and involves a version of [[distributive law]]s, hence it is related to a lifting problem:

* [[Ieke Moerdijk]], _Monads on tensor categories_, Category theory 1999 (Coimbra), J. Pure Appl. Algebra 168 (2002), no. 2-3, 189--208 (MR2003e:18012)

* Korn&#233;l Szlach&#225;nyi, _The monoidal Eilenberg&#8211;Moore construction and bialgebroids_, J. Pure Appl. Algebra 182, no. 2--3 (2003) 287--315; _Adjointable monoidal functors and quantum groupoids_, [math.QA/0301253](http://arxiv.org/abs/math/0301253)

Szlach&#225;nyi uses earlier analysis of 

* P. Schauenburg, _Bialgebras over noncommutative rings, and a structure theorem for Hopf bimodules_, Applied Categorical Structures __6__, 193-222 (1998) [doi](http://dx.doi.org/10.1023/A:1008608028634)

* H.E. Porst, _On categories of monoids, comonoids and bimonoids_, Quaest. Math. __31__ (2008) 127-139 [MR2010d:18010](http://www.ams.org/mathscinet-getitem?mr=2529129) [doi](http://dx.doi.org/10.2989/QM.2008.31.2.2.474) 

For a dual version see 

* P. Mac Crudden, Opmonoidal monads, Theory Appl. Cat., Vol. 10, 2002, No. 19, pp 469-485, [link](http://www.tac.mta.ca/tac/volumes/10/19/10-19abs.html)

There is also a more subtle notion also called Hopf monad in

* R. Wisbauer, B. Mesablishvili, Bimonads and Hopf monads on categories, [arXiv:0710.1163](http://arxiv.org/abs/0710.1163)

In some of these generalized cases, one does not have a good notion of of antipode, so that the difference between bimonoids and Hopf monoids has to be stated in different terms.  A similar case is in the case of [[Hopf algebroid]]s over a noncommutative base:

* [[Brian Day]], [[Ross Street]], _Monoidal bicategories and Hopf algebroids_, Advances in Math. __129__, 1 (1997) 99--157 

* [[Gabi Böhm]], _Hopf algebroids_, (a chapter of) Handbook of algebra, [arxiv:math.RA/0805.3806](http://arxiv.org/abs/0805.3806); _An alternative notion of Hopf algebroid_; in "Hopf algebras in noncommutative geometry and physics",  31--53, Lec. Notes in Pure and Appl. Math. __239__, Dekker, New York 2005; [math.QA/0301169](http://arxiv.org/abs/math.QA/0301169)

The fact that a skeleton of [[FinRel]] is the [[PROP]] for special bicommutative bimonoids is Theorem 7.2 in Coya and Fong, based on techniques from Lack's paper on distributive laws for PROPs:

* Brandon Coya and [[Brendan Fong]], _Corelations are the prop for extraspecial commutative Frobenius monoids_, Theory and Applications of Categories, Vol. 32, 2017, No. 11, pp. 380-395.   ([arxiv](https://arxiv.org/abs/1601.02307))

* [[Steve Lack]], Composing PROPs, Theory and Applications of Categories 13(9):147–163, 2004. ([pdf](http://www.tac.mta.ca/tac/volumes/13/9/13-09.pdf))

[[!redirects bimonoid]]
[[!redirects bimonoids]]
[[!redirects bimonoid object]]
[[!redirects bimonoid objects]]
