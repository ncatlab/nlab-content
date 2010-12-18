# Two-sided fibrations

* table of contents
{:toc}

## Idea

Just as a [[Grothendieck fibration]] $E\to B$ is an alternate way to encode a [[pseudofunctor]] $B^{op}\to Cat$, a *two-sided fibration* $A \leftarrow E \to B$ is a way to encode a pseudofunctor $A\times B^{op}\to Cat$.

## Definition

A **two-sided discrete fibration** is a span $q \colon E \to A$, $p \colon E \to B$ of [[categories]] and [[functors]] such that 
1. each $b \to pe$ in $B$ has a unique lift in $E$ that has codomain $e$ and is in the fiber over $q e$
1. each $qe \to a$ in $A$ has a unique lift in $E$ that has domain $e$ and is in the fiber over $p e$
1. for each $f\colon e \to e'$ in $E$, the codomain of the lift of $qf$ equals the domain of the lift of $p f$ and their composite is $f$.

A **two-sided fibration** is a span $q \colon E \to A$, $p \colon E \to B$ such that
1. each $b \to pe$ in $B$ has a [[cartesian morphism|cartesian]] lift in $E$ with codomain $e$ and lying in the fiber over the identity at $q e$
1. each $qe \to a$ in $A$ has an opcartesian lift in $E$ with domain $e$ and lying in the fiber over the identity at $p e$
1. for each $f \colon e \to e'$ in $E$ the canonical arrow between the codomain of any opcartesian lift of $q f$ as in (2) and the domain of the cartesian lift of $pf$ as in (1) is an [[isomorphism]].

## References

* [[Ross Street]], *Fibrations in bicategories* and other papers

[[!redirects two-sided fibrations]]
[[!redirects two-sided discrete fibration]]
[[!redirects two-sided discrete fibrations]]
