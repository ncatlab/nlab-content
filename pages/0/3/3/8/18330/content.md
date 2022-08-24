+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definitions

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[categories with the same collection of objects]] $(A, B) \coloneqq (Ob, Mor_A, Mor_B)$ is a [[functor between categories with the same collection of objects|functor between categories]] $A \coloneqq (Ob, Mor_A)$ and $B \coloneqq (Ob, Mor_B)$ that has as its underlying object function $F_{ob}$ the [[identity function]] on the collection of objects. 
\end{definition}

In type theory, [[identity functions]] do not necessarily violate the [[principle of equivalence]], because the [[identity type]] $id(x) =_Ob x$ for object $x:A$ is not necessarily a proposition, and in the presence of [[univalence]], is necessarily required to satisfy the [[principle of equivalence]]. However, in a [[material set theory]] or [[structural set theory]] or a type theory with [[axiom K]], the above definition violates the [[principle of equivalence]], so instead they use the following definition which does satisfy the principle of equivalence:

\begin{definition}
An **identity-on-objects functor** $F: A\to B$ between [[categories with the same collection of objects]] $(A, B) \coloneqq (Ob, Mor_A, Mor_B)$ is a family of functions $F_{x, y}:Mor_A(x, y) \to Mor_B(x, y)$ indexed by objects $x:Ob$ and $y:Ob$. 
\end{definition}

...

There are a number of different ways to define two categories with the same collection of objects:

### With propositional equality or equivalence

In set theory, the objects of a category are required to be a set. In [[material set theories]], one could postulate the condition that $Ob = ob(A) = ob(B)$. However, it mentions equality of sets, which means that the definition is not even definable in a [[structural set theory]] such as [[SEAR]] or [[ETCS with elements]], where there is no notion of equality of sets, only equality of [[functions]], [[relations]], and [[elements]]. In structural set theories, instead of talking about equality of sets, one talks about having [[bijection]] between sets $a:Ob \cong ob(A)$, $b:Ob \cong ob(B)$, and $F_{ob}:ob(A) \cong ob(B)$. This yields a [[bijective-on-objects functor]]. 

In type theories, the objects of a category do not form a set, but a type. The categories whose type of objects is a set is a strict category, and as a result, the above definitions are only valid for [[strict categories]]. However, there is a generalization of both material set theory equality of sets and structural set theory bijection of sets to type theory: identity types and equivalence of types. 

For identity types, one postulates the existence of [[identifications]] $a:Ob =_\mathcal{U} ob(A)$ and $b:Ob =_\mathcal{U} ob(B)$, resulting in an identification $a^{-1} b: ob(A) =_\mathcal{U} ob(B)$. This is what is called an **identity-on-objects functor** in type theory. For equivalences, one postulates the existence of [[equivalence in homotopy type theory|equivalence]] $a:Ob \simeq_\mathcal{U} ob(A)$ and $b:Ob \simeq_\mathcal{U} ob(B)$, and $F_{ob}:ob(A) \simeq_\mathcal{U} ob(B)$. This yields an [[equivalent-on-objects functor]]. If the background universe $\mathcal{U}$ is an [[univalent universe]], then equivalent-on-objects functors and identity-on-objects functors are equivalent to each other. If the categories are strict, then both equivalent-on-objects functors and identity-on-objects functors are equivalent to bijective-on-objects functors. 

However, in general categories, all these definitions still nevertheless violate the [[principle of equivalence]]. What one actually needs are [[essentially surjective functors]]. Only in [[univalent categories]] are essentially surjective functors the same as equivalent-on-object functors, and additionally only when both the source and target univalent categories are in a [[univalent universe]] are essentially surjective functors between univalent categories identity-on-object functors. 

### With judgmental equality

There is another notion of equality in type theory, [[judgmental equality]], which is a metatheoretic [[judgment]] rather than a [[type]] or [[propositional equality]]. In this case, the underlying object types of the two categories $A$ and $B$ are judgmentally equal, $ob(A) \equiv ob(B)$, and we could similarly judge that they are judgmentally equal to a third type $Ob$, $Ob \equiv ob(A)$ and $Ob \equiv ob(B)$. By the definition of identity function in type theory ($id_{Ob} \coloneqq \lambda x.x:Ob \to Ob$), given an object $x:Ob$, $id_{Ob}(x)$ is judgmentally equal to $x$:
$$\Gamma, x:Ob \vdash id_{Ob}(x) \equiv x:Ob$$
This results in the following definition:

\begin{definition}
An **identity-on-objects [[functor]]** $F: A\to B$ between [[categories]] $A$ and $B$ whose type of [[objects]] are [[judgmental equality|judgmentally equal]] to a third type $Ob$, i.e. $Ob \equiv ob(A)$ and $Ob \equiv ob(B)$, is a functor between categories which has as its underlying object function $F_{ob}: Ob \to Ob$ the [[identity function]] on $Ob$. 
\end{definition}

This definition does not violate the [[principle of equivalence]], because judgmental equality is a judgment, and thus does not result in (propositional) equality of objects. 

This is additionally the same as postulating that there is only one type $Ob$ with two [[type families]] on $Ob$, $A(x,y)$ and $B(x,y)$ for $x,y\in Ob$, with additional composition, identity, associativity, and unital laws for morphisms, making each of $(Ob, A)$ and $(Ob, B)$ into a category, plus a family of functions $A(x,y) \to B(x,y)$ which commuting with these category structures. This is the approach used in two separate definitions of [[dagger categories]] on the nLab. 

More abstractly, this can be defined as a category [[enriched category|enriched]] over the [[arrow category]] $Set^\to$.  See also [[M-category]] and [[F-category]].

## Alternative: using displayed categories

...

## Examples

* A [[dagger category]] is a category $\mathcal{C}$ with a [[contravariant functor|contravariant endofunctor]] $\dagger:\mathcal{C}^\op \to \mathcal{C}$ that is an identity-on-objects functor, such that for all objects $A:\mathcal{C}$ and $B:\mathcal{C}$ and morphisms $f:Hom(A,B)$, $(f^\dagger)^\dagger = f$. 

## Related pages

* [[bijective-on-objects functor]]
* [[equivalent-on-objects functor]]
* [[essentially surjective functor]] 
* [[displayed category]]
* [[Freyd category]]
* [[Freyd multicategory]]
* [[dagger category]]
* [[principle of equivalence]]

## References

For the definition of isomorphism of categories and adjoint equivalence of univalent categories: 

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

For the use of [[displayed categories]] instead of [[identity-on-objects functors]] in definitions:

* Benedikt Ahrens, Peter LeFanu Lumsdaine, *Displayed Categories*, ([arXiv:1705.04296](https://arxiv.org/abs/1705.04296))

[[!redirects identity-on-objects]]
[[!redirects identity on objects]]

[[!redirects identity-on-objects functor]]
[[!redirects identity-on-objects functors]]
[[!redirects identity on objects functor]]
[[!redirects identity on objects functors]]
[[!redirects io functor]]
[[!redirects io functors]]
[[!redirects i.o. functor]]
[[!redirects i.o. functors]]
