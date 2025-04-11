> This page is about [[distributive lattices]] equipped with a contravariant involution.  For [[Heyting algebras]] satisfying [[de Morgan's law]], which are also sometimes called "De Morgan algebras", see [[De Morgan Heyting algebra]].

----

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--

# De Morgan algebras

* table of contents
{: toc}

## Definition

A **De Morgan algebra** is a [[distributive lattice]] $D$ equipped with a [[contravariant functor|contravariant]] [[involution]], i.e. a map $\neg : D^{op}\to D$ such that $\neg\neg A = A$.  This implies that $\neg$ satisfies De Morgan's laws: $\neg(A\wedge B) = \neg A \vee \neg B$ and $\neg (A\vee B) = \neg A \wedge \neg B$.

## Examples

* Any [[Boolean algebra]] is a De Morgan algebra, with $\neg$ the logical negation.
* Any [[star-autonomous category|star-autonomous poset]] that happens to be a [[distributive lattice]] is a De Morgan algebra, with $\neg$ the star-autonomous involution $(-)^*$.
* The unit interval $[0,1]$ is a De Morgan algebra, with $\neg x = (1-x)$.
* The four-point algebra with two parallel lines: $\{0, a, b, 1\}$ with $\neg a = a$, $\neg b = b$, $a \vee b = 1$ and $a \wedge b = 0$ is a small example of a De Morgan algebra which is not Boolean.
* The [[set]] $\{(P, Q) \in \Omega \times \Omega \vert \neg (P \wedge Q) = \top\}$ of [[mutually exclusive propositions]] in [[constructive mathematics]] is a De Morgan algebra where the [[distributive lattice]] structure is given by the [[additive conjunction]] and [[additive disjunction]] of the [[affine logic]] of mutually exclusive propositions, and the [[involution]] is given by the [[linear negation]]. See [[antithesis interpretation]] for more details. 
* More generally, given any [[Heyting algebra]] $L$, the [[set]] $\{(a, b) \in L \times L \vert \neg (a \wedge b) = \top\}$ is a De Morgan algebra where the [[distributive lattice]] structure is given by $\top \coloneqq (\top, \bot)$, $\bot \coloneqq (\bot, \top)$, $(a, b) \sqcap (c, d) \coloneqq (a \wedge c, b \vee d)$ and $(a, b) \sqcup (c, d) \coloneqq (a \vee c, b \wedge d)$, and the [[involution]] is given by $\neg (a, b) \coloneqq (b, a)$. 

## Category of de Morgan algebras

The category of de Morgan algebras is a category whose [[objects]] are de Morgan algebras and whose [[morphisms]] are [[lattice homomorphisms]] that preserve the [[involution]] as well. 

The [[opposite category]] of the category of Morgan algebras is the category of "compact totally ordered-disconnected ordered topological spaces which possess an involutorial homeomorphism that is also a dual order-isomorphism" ([Cornish & Fowler 77](#CF77), [Cornish & Fowler 79](#CF79)). 

## Related concepts

* [[De Morgan duality]]

* De Morgan algebras are used in one form of [[cubical type theory]]

## References

* {#CF77} [[William H Cornish]], [[Peter R Fowler]], *Coproducts of de morgan algebras*, Bulletin of the Australian Mathematical Society, 16(01):1–13, 1977. ([pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/D86F551CF77BE8374CD4BFB1A73F73B6/S0004972700022966a.pdf/coproducts-of-de-morgan-algebras.pdf))

* {#CF79} [[William H Cornish]], [[Peter R Fowler]], *Coproducts of kleene algebras*, Journal of the Australian Mathematical Society (Series A), 27(02):209–220, 1979 ([pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/AAD3D8E6D208205C39C54D0873AEB883/S1446788700012131a.pdf/div-class-title-coproducts-of-kleene-algebras-div.pdf))

* *What's the deal with De Morgan algebras and Kleene algebras?*, MathOverflow ([web](https://mathoverflow.net/questions/483035/whats-the-deal-with-de-morgan-algebras-and-kleene-algebras))

[[!redirects De Morgan algebra]]
[[!redirects de Morgan algebra]]
[[!redirects de morgan algebra]]
[[!redirects De Morgan algebras]]
[[!redirects de Morgan algebras]]
[[!redirects de morgan algebras]]
