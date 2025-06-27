* table of contents
{: toc}

## Idea 

A _weak representation of a functor_ $P : C^o \to Set$ ([[presheaf]]) is like a [[representable functor]] but only satisfying the representability condition up to [[retract]] rather than [[isomorphism]]. Unlike a representable, this structure is not unique up to isomorphism, and so we speak of _representations_ as [[structure]] rather than _representability_ as a [[property]].

In [[type theory|type theoretic]] terms, this is an object that only satisfies the $\beta$ equation of a universal property and not the $\eta$ equation.

## Definition

A weak representation of a presheaf $P : C^o \to Set$ consists of

1. An object $X$ in $C$
2. [[natural transformation|natural transformations]] $s : P(\Gamma) \to C(\Gamma, X)$ and $r : C(\Gamma, X) \to P(\Gamma)$ such that $r$ is a [[retract]] of $s$.

Equivalently, by the [[Yoneda lemma]], a weak representation is

1. An object $X$
2. A "weak universal morphism" $\epsilon : P(X)$
3. A natural transformation $I : P(\Gamma) \to C(\Gamma, X)$ that is a [[section]] of $P(-)(\epsilon) : C(\Gamma, X) \to P(\Gamma)$

## Relation to Representable Functors

A weak representation $(X, \epsilon, I)$ of $P$ induces an [[idempotent]] $e$ on the representable sets $C(-, X)$ such that $P$ is the [[idempotent splitting]] of the representable $C(-,X)$ in the presheaf category. By the Yoneda lemma, this induces an idempotent $e$ on $X$ in $C$, and an object $Y$ represents $P$ if and only if $Y$ is the idempotent splitting of $e$. As a consequence, a representable $Y$ has a canonical section to any weak representation $X$.

In type theoretic terms, the idempotent performs [[eta expansion|$\eta$ expansion]], and so this says that a representable can be constructed from a weak representable as the [[fixed points]] of $\eta$ expansion, or dually as a quotient equating the $\eta$ expansion with the identity.

## Related Concepts

* [[weak adjoint]]
* [[weak limit]]
* [[semifunctor]]
* [[lax idempotent 2-adjunction]]