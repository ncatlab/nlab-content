> This page is about [[distributive lattices]] equipped with a contravariant involution.  For [[Heyting algebras]] satisfying [[de Morgan's law]], which are also sometimes called "De Morgan algebras", see [[De Morgan Heyting algebra]].

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

## Related concepts

* [[De Morgan duality]]

* De Morgan algebras are used in one form of [[cubical type theory]]

[[!redirects De Morgan algebra]]
[[!redirects de Morgan algebra]]
[[!redirects de morgan algebra]]
[[!redirects De Morgan algebras]]
[[!redirects de Morgan algebras]]
[[!redirects de morgan algebras]]
