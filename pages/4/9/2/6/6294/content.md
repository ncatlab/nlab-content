
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For $C$ a [[cartesian monoidal category]] (a category with [[finite products]]), an __internal ring__ or a __ring object__ in $C$ is an [[internalization]] to the category $C$ of the notion of a [[ring]].

This is a [[monoid|monoid object]] internal to the category of  [[abelian group|abelian]] [[group object]]s internal to $C$.

Ring objects can be defined in more general [[symmetric monoidal categories]] as the corresponding module over a [[ring operad]]. 


## Definition 

Let $T$ be the [[Lawvere theory]] for rings, viz. the category [[opposite category|opposite]] to the category of [[finitely generated object|finitely generated]] [[free object|free]] rings (which are non-commutative [[polynomial rings]] $\mathbb{Z}\langle X_1, \ldots, X_n\rangle$) and ring maps between them. Then for $C$ a category with finite products, a _ring object_ in $C$ may be identified with a product-preserving functor $T \to C$. 

The more traditional definition, based on a traditional presentation of the [[equational theory]] of rings, is that a ring object consists of an object $R$ in $C$ together with morphisms $a: R \times R \to R$ (addition), $m: R \times R \to R$ (multiplication), $0: 1 \to R$ (zero), $e: 1 \to R$ (multiplicative identity), $-: R \to R$ (additive inversion), subject to [[commutative diagrams]] in $C$ that express the usual ring axioms. 

## Examples

* A ring object in [[Top]] is a [[topological ring]].

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
