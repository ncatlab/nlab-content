
> This page is about the notion of poly-morphism considered by [[Shinichi Mochizuki]]. For the concept in [[computer science]] see [[polymorphism]]. Or see [[universe polymorphism]] for the concept in [[type theory]].

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

For a [[category]] $C$, a **poly-morphism** is a collection of [[morphisms]] with common [[source]] and [[target]], considered as a morphism in a new category $C^{poly}$ with the same [[objects]], but with [[hom-sets]] $C^{poly}(a,b) \coloneqq P(C(a,b))$, the [[power set]] of the original hom-sets.

These play a substantive rôle in [[Shinichi Mochizuki]]'s [[inter-universal Teichmüller theory]] ([Mochizuki 12, section 0](#Mochizuki12)). Here we put these into the broader context of [[change of enriching categories]] along [[lax monoidal functors]] $F$ as the special case that $F$ is a [[power set]]-functor, or an [[G-set|equivariant]] version thereof.

## Abstract approach

In the following, fix a [[monoidal category]] $V$ and a $V$-[[enriched category]] 

$$
  C \in V Cat
  \,.
$$

Examples to keep in mind for $V$ are the category [[Set]] of sets considered as a [[cartesian monoidal category]], or the category [[G-set]] for a given [[group]] $G$, again with the cartesian monoidal structure.

Recall:

+-- {: .num_defn #ChangeOfEnrichingCategory}
###### Definition
**([[change of enriching category]] from $V$ to itself)**

For $F\colon V\to V$ a [[lax monoidal functor]] from $V$ to itself, the image $F_\ast(C)$ of $C$ under the corresponding [[change of enriching category]] is the $V$-category with the same [[objects]] as $C$, and with $V$-[[hom objects]] given by 

$$
  F_\ast(C)(a,b) \coloneqq F(C(a,b))
  \,.
$$ 

The [[composition]]-, [[unit]]-, [[associator]]- and [[unitor]]-[[morphisms]] of $F_\ast(C)$ are the [[images]] of those of $C$ under $P$ suitably composed with the structure morphisms of the lax monoidal functor $P$.

=-- 
 
For the case of poly-morphisms the relevant [[lax monoidal functors]] are [[power set]]-functors

+-- {: .num_example #PowerSetFunctors}
###### Examples
**([[lax monoidal functor|lax monoidal]] [[power set]]-[[functors]])

* For $V=$[[Set]] equipped with its [[cartesian monoidal category]] [[structure]], $C$ an arbitrary category, take $F \coloneqq P \;\colon\; Set \to Set$ the covariant [[power set]] functor. This is lax monoidal since every [[pair]] of [[subsets]] $U \subseteq S$ and $V\subseteq T$ gives a subset $U\times V \subseteq S\times T$.

* For $G$ a group, $V=$[[GSet]] with the [[cartesian monoidal category]] [[structure]], $C$ a [[enriched category|category enriched in]] [[G-sets]], let $F \coloneqq P\;\colon\; GSet \to GSet$ also be the covariant [[power set]] functor, but for $S$ a $G$-set, equip $P(S)$ with the $G$-[[action]]
$$
  U\mapsto g\cdot U 
  = 
  \{g\cdot x \in S \mid x\in U\}
  \,.
$$

=--

+-- {: .num_defn #PolyMorphisms}
###### Definition
**(pol-morphisms)**

For $C$ a plain category and $F \coloneqq P \colon Set \to Set$ the [[power set]]-functor (Def. \ref{PowerSetFunctors}), we write

$$
  C^{poly}
  \;\coloneqq\;
   P_\ast(C)
$$

for the image of $C$ under the [[change of enriching category]] (Def. \ref{ChangeOfEnrichingCategory}) along $P$.

We say that the [[morphisms]] of $C^{poly}$ are the **poly-morphisms** of $C$.

Explicitly, this means [[composition]] is defined to be
$$
C^{poly}(a,b) \otimes C^{poly}(b,c) = P(C(a,b)) \otimes P(C(b,c)) \to P(C(a,b)\otimes B(b,c)) \to P(C(a,c)) = C^{P poly}(a,c)
$$
and the [[unit]] map is
$$
  I \to P(I) \to P(C(a,a)) = C^{P poly}(a,a)
  \,.
$$


A **poly-isomorphism** of $C$ is defined to be a poly-morphism of the [[core]] of $C$, hence a morphism of $(Core(C))^{poly}$.
Hence a poly-isomorphism is a collection of _[[invertible morphisms]]_ of $C$. 
(Note that these are **not** in general the [[isomorphisms]] in $C^{poly}$: all the isomorphisms in $C^{poly}$ are actual isomorphisms in $C$.)

=--

## References

Poly-morphisms are considered in section 0 of:

* {#Mochizuki12} [[Shinichi Mochizuki]], _Inter-universal Teichm&#252;ller theory I, Construction of Hodge theaters_ (2012) ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20I.pdf))


[[!redirects poly-morphisms]]
