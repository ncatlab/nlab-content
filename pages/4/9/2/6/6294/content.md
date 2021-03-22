
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For $C$ a [[cartesian monoidal category]] (a category with [[finite products]]), an *internal ring* or a *ring object* in $C$ is an [[internalization]] to the category $C$ of the notion of a [[ring]].

Under some reasonable assumptions on $C$ that allow one to construct a ([[symmetric monoidal category|symmetric]]) [[monoidal category|monoidal]] [[tensor product]] on the [[category]] of [[abelian group|abelian]] [[group objects]] $Ab(C)$ [[internalization|internal]] to $C$, a ring object can also be defined as a [[monoid object]] internal to that monoidal category $Ab(C)$. 

Sometimes one might take this last point of view a little further, especially in certain contexts of [[stable homotopy theory]] where a [[stable (∞,1)-category]] of [[spectra]] is already something like an [[(∞,1)-category]]-analogue of a [[category of abelian groups]]. With the understanding that a [[symmetric smash product of spectra]] plays a role analogous to [[tensor products of abelian groups]], monoids with respect to the [[smash product]] are often referred to as "$xyz$-rings" of one sort or another (as mentioned at "[[ring operad]]"). Thus we have carry-over phrases from the early days of stable homotopy theory, such as "[[A-∞ rings]]" (for monoids) and "[[E-∞ rings]]" (commutative monoids). Here it is understood that the monoid multiplication on spectra is an $(\infty, 1)$-refinement of a multiplicative structure on a corresponding [[cohomology theory]], with various forms of [[K-theory]] providing archetypal examples. 


## Definition 

Let $T$ be the [[Lawvere theory]] for rings, viz. the category [[opposite category|opposite]] to the category of [[finitely generated object|finitely generated]] [[free object|free]] rings (which are non-commutative [[polynomial rings]] $\mathbb{Z}\langle X_1, \ldots, X_n\rangle$) and ring maps between them. Then for $C$ a category with finite products, a _ring object_ in $C$ may be identified with a product-preserving functor $T \to C$. 

The more traditional definition, based on a traditional presentation of the [[equational theory]] of rings, is that a ring object consists of an object $R$ in $C$ together with morphisms $a: R \times R \to R$ (addition), $m: R \times R \to R$ (multiplication), $0: 1 \to R$ (zero), $e: 1 \to R$ (multiplicative identity), $-: R \to R$ (additive inversion), subject to [[commutative diagrams]] in $C$ that express the usual ring axioms. 

## Examples

* A ring object in [[Top]] is a [[topological ring]].

* A ring object in [[Ho(Top)]] is an [[H-ring]].

* A [[topos]] equipped with a ring object is called a [[ringed topos]], see there for more details.

* The [[affine line]] (see there) is a ring object in the given ambient [[topos]].

## Related concepts

* [[monoid]], [[monoid object]],

* [[group]], [[group object]], [[group object in an (∞,1)-category]]

* [[ring]], **ring object**


[[!redirects ring object]]
[[!redirects ring objects]]
[[!redirects internal ring]]
[[!redirects internal rings]]