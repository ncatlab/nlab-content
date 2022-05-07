## Idea

Partial model categories are one of the many intermediate notions
between [[relative categories]] and [[model categories]].

They axiomatize those properties of [[model categories]]
that only involve weak equivalences.

## Definition

A __partial model category__ is a [[relative category]] $(C, W)$
that satisfies the [[2-out-of-6 property]]
(if $s r$ and $t s$ are weak equivalences, then so are $r$, $s$, $t$, $t s r$)
and admits a [[3-arrow calculus]],
i.e., there are [[subcategories]]
$U, V \subseteq W$ of the weak equivalences (which can be thought of as analogues of acyclic cofibrations
and acyclic fibrations)
such that $U$ is closed under [[cobase changes]] along arbitrary morphisms of $C$ (which are required to exist),
$V$ is closed under [[base changes]] along arbitrary morphisms of $C$,
and any weak equivalence can be functorially factored as the composition $v u$
for some $u\in U$ and $v\in V$.

## Properties

If $(C,W)$ is a partial model category,
then any Reedy fibrant replacement
of the [[Rezk nerve]] $N(C,W)$ is a [[complete Segal space]].

## Related concepts

* [[model category]]

* [[relative category]]

* [[semimodel category]]

* [[weak model category]]

* [[premodel category]]

* [[homotopical category]]

## References

* [[Clark Barwick]], [[Daniel M. Kan]], _Partial model categories and their simplicial nerves_, [arXiv](https://arxiv.org/abs/1102.2512v2).
