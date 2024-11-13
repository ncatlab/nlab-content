
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[forgetful functor]] from a [[category]] of [[actions]]/[[representations]] to the underlying [[sets]]/[[spaces]] is often called a _fiber functor_, notably in the context of [[Tannaka duality]] and [[Galois theory]].

The archetypical example which gives rise to the term is the following. If one has the  [[category]] $Et(X)$ of [[covering spaces]]  of a (nice enough) [[topological space]] $X$, then after picking any point $x \in X$ the operation of forming the [[fibre]] over that point gives a [[functor]] $fib_x \colon Et(X)\to Set$ to the category [[Set]] of [[sets]]. The [[natural automorphisms]] of this functor form the (algebraic) [[Chevalley fundamental group|fundamental group]], $\pi_1(X)$. The main theorem of the [[Galois theory|Galois-Poincaré theory]] of [[covering spaces]] can be viewed as stating that this sets up an [[equivalence of categories]] between that category of covering spaces and the category of $\pi_1$[[permutation representation|-sets]]. This equivalence is compatible with the chosen fibre functor and the further [[forgetful functor]] from $\pi_1-Sets$ to $Sets$. Extracting from this situation, that forgetful functor is thought of as being a _fibre functor_ as well.  Any category of [[G-sets]], for $G$ a [[group]], gives a [[monoidal category]], and the forgetful functor is a [[monoidal functor]]; of course, the category of [[G-sets]] corresponds to the category of [[permutation representations]] of $G$, and generalising this basic example leads to the following idea.

The [[forgetful functor|forgetful]] [[strict monoidal functor]] from a [[monoidal category]] to some standard monoidal category, usually the category [[Vect]] of [[vector spaces]] over a field is called the __fiber functor__ in some contexts, especially in [[Tannaka reconstruction]] in which the symmetry object is reconstructed from the (object of) endomorphisms of the fiber functor. In mixed Tannaka duality, a single fiber functor does not suffice for reconstruction, but rather a family of fiber functors to different bases. 




Historically, the notion was used extensively, starting in the 1960s by [[Grothendieck]] and his collaborators. The terminology is from the [[Grothendieck Galois theory]]: namely Grothendieck reconstructs the ([[profinite group|profinite]]) [[fundamental group]] in algebraic geometry from a fiber functor: the fundamental group acts on a covering by deck transformations and by monodromy transformation for bundles over the covering, algebraic analogues of such a picture can thus be used to define a fundamental group, not by using some idea of loops which are often hard to define in abstract setups, but by a form of Tannakian reconstruction. Grothendieck also introduced the idea of using many "base points" that is, many fibre functors, thus giving an abstract analogue of the  [[fundamental groupoid]] of a space.

## Warning

Please do not confuse the terminology with the case of a functor which is a [[Grothendieck fibration]] (i.e. a fibered category); nor with a fiber ("preimage" of a sort) of a functor. These are related ideas but are best kept separate.

## Properties

### Tannaka duality

[[!include structure on algebras and their module categories - table]]

## See also

* [[Tannakian category]]

## References


* [[P. Cartier]], _A mad day's work: from Grothendieck to Connes and Kontsevich The evolution of concepts of space and symmetry_, Bull. Amer. Math. Soc. __38__ (2001), 389-408, [pdf](http://www.ams.org/bull/2001-38-04/S0273-0979-01-00913-2/S0273-0979-01-00913-2.pdf)

* [[P. Deligne]], _[[Catégories Tannakiennes]]_

For [[fusion 2-categories]]:

* {#DY23} [[Thibault Decoppet]], [[Matthew Yu]]. *Fiber 2-Functors and Tambara-Yamagami Fusion 2-Categories*. (2023) &lbrack;[arXiv:2306.08117](https://arxiv.org/abs/2306.08117)&rbrack;



[[!redirects fiber functors]]
[[!redirects fibre functor]]
[[!redirects fibre functors]]