
> This page is about the notion of poly-morphism introduced by Shinichi Mochizuki. For the concept in computer science see [[polymorphism]]. Or see [[universe polymorphism]] for the concept in type theory.

## Idea

For a category $C$, a **poly-morphism** is a collection of morphisms with common source and target, considered as a morphism in a new category $C^{poly}$ with the same objects, but with hom-sets $C^{poly}(a,b) := P(C(a,b))$, the [[power set]] of the original hom-sets.

These play a substantive rôle in [[Shinichi Mochizuki]]'s [[inter-universal Teichmüller theory]].

## Abstract approach

In the following, fix a [[monoidal category]] $V$ and a $V$-[[enriched category]] $C$. Examples to keep in mind for $V$ are the category [[Set]] of sets considered as a [[cartesian monoidal category]], or the category [[G-set]] for a given group $G$, again with the cartesian monoidal structure.

+-- {: .num_defn}
###### Definition

For $P\colon V\to V$ a [[lax monoidal functor]], the **$P$-poly category** $C^{P poly}$ is the $V$-category with the same objects as $C$, and where the $V$-hom object $C^{P poly}(a,b) := P(C(a,b))$.

=--

That $C^{P poly}$ really is a $V$-category, i.e. that it has a composition map (that is associative etc) follows from the lax monoidal structure on $P$. Composition is defined to be
$$
C^{P poly}(a,b) \otimes C^{P poly}(b,c) = P(C(a,b)) \otimes P(C(b,c)) \to P(C(a,b)\otimes B(b,c)) \to P(C(a,c)) = C^{P poly}(a,c)
$$
and this is associative, using the definitions of lax monoidal functor and enriched category. The unit map
$$
I \to P(I) \to P(C(a,a)) = C^{P poly}(a,a)
$$
satisfies the required conditions again from the properties of $P$.


Examples of such functors $P$ are:

* For $V=Set$ with the cartesian monoidal structure, $C$ an arbitrary category, take $P\colon Set \to Set$ the covariant [[power set]] functor. This is lax monoidal since every pair of subsets $U \subseteq S$ and $V\subseteq T$ gives a subset $U\times V \subseteq S\times T$.

* For $G$ a group, $V=GSet$ with the cartesian model structure, $C$ a category enriched in $G$-sets, let $P\colon GSet \to GSet$ also be the covariant power set functor, but for $S$ a $G$-set, equip $P(S)$ with the $G$-action
$$
U\mapsto g\cdot U = \{g\cdot x \in S \mid x\in U\}.
$$

When we are in the first case, $V=Set$ and $P$ the power set functor, so that $C$ is a plain category, then we shall refer to $C^{P poly}$ as just $C^{poly}$, and its morphisms as **poly-morphisms**.

A **poly-isomorphism** of $C$ is defined to be a poly-morphism of the [[core]] of $C$, so that it is a collection of _invertible_ arrows of $C$. Note that these are **not** the isomorphisms in $C^{poly}$: all the isomorphisms in $C^{poly}$ come from $C$.

## References

Poly-morphisms in the case of ordinary categories are introduced in section 0 of:

* [[Shinichi Mochizuki]], _Inter-universal Teichm&#252;ller theory I, Construction of Hodge theaters_ (2012) ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20I.pdf))

