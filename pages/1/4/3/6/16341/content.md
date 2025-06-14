
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Generalizing the classical notion of [[monoid]], one can define a _monoid_ (or _monoid object_) in any [[monoidal category]] $(C,\otimes,I)$.
Classical monoids are of course just monoids in [[Set]] with the [[cartesian product]].

By the [[microcosm principle]], in order to define monoid objects in $C$, $C$ itself must be a "categorified monoid" in some way.  The natural requirement is that it be a [[monoidal category]].  In fact, it suffices if $C$ is a [[multicategory]].  Contrast this with a [[group object]], which can only be defined in a [[cartesian monoidal category]] (or a [[cartesian multicategory]]).

## Definition

Namely, a **monoid in $C$** is an object $M$ equipped with a multiplication $\mu: M \otimes M \to M$ and a unit $\eta: I \to M$ satisfying the **associative law**:

$$
\array{
  & (M \otimes M) \otimes M
    & \stackrel{\alpha}{\longrightarrow}
  & M \otimes (M \otimes M)
    & \stackrel{1 \otimes \mu}{\longrightarrow}
  & M \otimes M
  \\
  & {}_{\mu \otimes 1}\searrow
    &&
    && \swarrow_{\mu}
  &
  \\
  &&
  M \otimes M
    & \stackrel{\mu}{\longrightarrow}
  M
  &&
}
$$

and the **left and right unit laws**:

$$
\array{
  & I \otimes M
  & \stackrel{\eta \otimes 1}{\longrightarrow}
  & M \otimes M
  & \stackrel{1 \otimes \eta}{\longleftarrow}
  & M \otimes I
  \\
  &
  & {}_{\lambda}\searrow
  & {}_{\mu}\downarrow
  & \swarrow_{\rho}
  &
  \\
  &
  &
  & M
  &
  &
}
$$

Here $\alpha$ is the [[associator]] in $C$, while $\lambda$ and $\rho$ are the left and right [[unitor|unitors]].

## Morphism of monoids

The analogue of a monoid homomorphism, called a morphism of monoids, is a morphism, $\f: M \to M'$  between two monoid objects, satisfying the equations;


$f \circ \mu = \mu' \circ (f \otimes f)$

$f \circ \eta = \eta'$

corresponding to the commutative diagrams;

$$
\array{
  & M \otimes M
  & \stackrel{f \otimes f}{\longrightarrow}
  & M' \otimes M'
  \\
  & {}_{\mu}\downarrow
  &
  & \downarrow_{\mu'}
  \\
  & M
  & \stackrel{f}{\longrightarrow}
  & M'
}
$$

$$
\array{
  & I
  & \stackrel{\eta}{\longrightarrow}
  & M
  \\
  &
  & {}_{\eta'}\searrow
  & \downarrow_{f}
  \\
  &
  &
  & M'
}
$$

## As categories with one object

Just as the category of regular [[monoid|monoids]] is equivalent to the category of locally small (i.e. Set-enriched) categories with one object, the category of monoids in $C$ (with the obvious morphisms) is equivalent to the category of $C$-[[enriched category|enriched categories]] with one object.


## Properties

### Preservation by lax monoidal functors

Monoid structure is preserved by [[lax monoidal functors]]. Comonoid structure by [[oplax monoidal functors]]. See [[lax monoidal functor]] for more details.

### Category of monoids

For special properties of categories of monoids, see [[category of monoids]].


## Examples

\begin{example}
\label{AssociativeAlgebras}
A monoid in a [[monoidal category|monoidal]] [[category of modules]] [[Mod|$R Mod$]] (over any [[ground ring]] $R$ and equipped with the [[tensor product of modules]]) is an [[associative unital algebra]] over $R$.
\end{example}

\begin{example}\label{Rings}
As the special case of Exp. \ref{AssociativeAlgebras} for $R = \mathbb{Z}$ the [[integers]]:

A monoid object in the [[monoidal category]] [[Ab]] of [[abelian groups]] with the [[tensor product of abelian groups]],  is a *[[ring]]*.
\end{example}



\begin{example}
As the special case of Exp. \ref{AssociativeAlgebras} for $R = k$ a [[field]]:

 A monoid object in the category [[Vect]] of [[vector spaces]] (over any [[ground field]] $k$) with the [[tensor product of vector spaces]] is an *[[associative unital algebra]]* over $k$.
\end{example}



* A monoid object in [[Top]] (with cartesian product as the tensor product) is a [[topological monoid]].
* A monoid object in [[Ho(Top)]] is an [[H-monoid]].
* A monoid object in the category of monoids (with cartesian product as the tensor product) is a [[commutative monoid]].  This is a version of the [[Eckmann-Hilton argument]].
* A monoid object in the category of complete join-[[semilattice]]s (with its tensor product that represents maps preserving joins in each variable separately) is a unital [[quantale]].
* The category of [[pointed set]]s has a monoidal structure given by the [[smash product]]. A monoid object in this monoidal category is an [[absorption monoid]].
* Given any monoidal category $C$, a monoid in the monoidal category $C^{op}$ is called a [[comonoid]] in $C$.
* In a [[cocartesian monoidal category]], every object is a monoid object in a unique way.
* For any category $C$, the [[endofunctor]] category $C^C$ has a monoidal structure induced by composition of endofunctors, and a monoid object in $C^C$ is a [[monad]] on $C$.

These are examples of monoids internal to monoidal categories.  More generally, given any [[bicategory]] $B$ and a chosen object $a$, the [[hom-category]] $B(a,a)$ has the structure of a monoidal category.  So, the concept of monoid makes sense in any [[bicategory]] $B$: we define a **monoid in $B$** to be a monoid in $B(a,a)$ for some object $a \in B$.  This often called a [[monad]] in $B$.  The reason is that a monad in [[Cat]] is the same as monad on a category.

A monoid in a bicategory $B$ may also be described as the [[hom-object]] of a $B$-[[enriched category]] with a single object. 


## Related concepts

* [[monoid]]

* [[commutative monoid in a symmetric monoidal category]]

* [[idempotent monoid in a monoidal category with diagonals]]

* [[semilattice in a symmetric monoidal category with diagonals]]

* [[idempotent monoid in a monoidal category]]

* [[module over a monoid]]

* [[category of monoids]]

* [[monoid in a monoidal (infinity,1)-category]]

[[!include reader-writer (co)monads -- table]]



## References

Original references (including the case of a [[commutative monoids in a symmetric monoidal category]], but see there for more):

* [[Jean Bénabou]], _Algèbre élémentaire dans les catégories_ (1964), C. R. Acad. Sci. Paris **258** (1964) pp.771-774, [gallica](https://gallica.bnf.fr/ark:/12148/bpt6k40102/f817)

* [[Saunders MacLane]], Sections III.6 & VII.3 in: *[[Categories for the Working Mathematician]]*, Springer  (1979, 2nd ed.) &lbrack;[doi:10.1007/978-1-4757-4721-8](https://link.springer.com/book/10.1007/978-1-4757-4721-8)&rbrack;

* [[Hans-Joachim Baues]], [[Mamuka Jibladze]], [[Andy Tonks]], *Cohomology of monoids in monoidal categories*, in: *Operads: Proceedings of Renaissance Conferences*, Contemporary Mathematics **202**, AMS (1997) 137-166 &lbrack;[doi:10.1090/conm/202](https://doi.org/10.1090/conm/202), preprint:[pdf](https://archive.mpim-bonn.mpg.de/id/eprint/1484/1/preprint_1995_121.pdf)&rbrack;


* [[Francis Borceux]], [[George Janelidze]], [[Gregory Maxwell Kelly]], p. 7 in: _Internal object actions_, Commentationes Mathematicae Universitatis Carolinae (2005) Volume: 46, Issue: 2, page 235-255 ([dml:249553](https://eudml.org/doc/249553))


Discussion for [[commutative monoids in a symmetric monoidal category]] including proof that/when the category of [[module objects]] is itself [[closed symmetric monoidal category|closed symmetric monoidal]]:

* [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], pp. 15 in: *Symmetric spectra*, J. Amer. Math. Soc. **13** (2000) 149-208 &lbrack;[arXiv:math/9801077](http://arxiv.org/abs/math/9801077), [doi:10.1090/S0894-0347-99-00320-3](https://doi.org/10.1090/S0894-0347-99-00320-3)&rbrack;

See also:

* [MO:180673](http://mathoverflow.net/questions/180673/category-of-modules-over-commutative-monoid-in-symmetric-monoidal-category).

* [[Florian Marty]], Sections 1.2, 1.3 in: _Des Ouverts Zariski et des Morphismes Lisses en G&#233;om&#233;trie Relative_, Ph.D. Toulouse (2009) &lbrack;[theses:2009TOU30071](https://www.theses.fr/2009TOU30071), [[Marty-DesOuverts.pdf:file]]&rbrack;

* [[Martin Brandenburg]], Section 4.1 of: _Tensor categorical foundations of algebraic geometry_ ([arXiv:1410.1716](http://arxiv.org/abs/1410.1716))


Lecture notes:

* [[Urs Schreiber]]: *[Algebras and Modules](Introduction+to+Stable+homotopy+theory+--+1-2#AlgebrasAndModules)*, in *[[Introduction to Stable Homotopy Theory]]* 1.2: *[[Introduction to Stable homotopy theory -- 1-2|Structured Spectra]]* 

In [[cartesian monoidal categories]]:

* [[John Michael Boardman]], *Algebraic objects in categories*, Chapter 7 of: _Stable Operations in Generalized Cohomology_ &lbrack;[pdf](https://math.jhu.edu/~wsw/papers2/math/28a-boardman-stable.pdf), [[Boardman-StableOperations.pdf:file]]&rbrack; in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_ Oxford 1995 ([doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7))

and here formalized as [[mathematical structures]] in [[proof assistants]]:

in a context of plain [[Agda]]:

* [[Martín Escardó]], *[The Types of Magmas and Monoids](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html#magmasandmonoids)*, §4 in: *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580),  [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html)&rbrack;

in a context of [[cubical type theory|cubical]] [[Agda]]:

* [[1lab]]: *[Algebra.Monoid](https://1lab.dev/Algebra.Monoid.html)*


[[!redirects monoids in a monoidal category]]
[[!redirects monoids in monoidal categories]]

[[!redirects monoid object in a monoidal category]]
[[!redirects monoid objects in a monoidal category]]
[[!redirects monoid objects in monoidal categories]]


[[!redirects monoid object]]
[[!redirects monoid objects]]
[[!redirects internal monoid]]
[[!redirects internal monoids]]

[[!redirects algebra object]]
[[!redirects algebra objects]]

