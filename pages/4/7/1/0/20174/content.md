* table of contents
{: toc}

## Definition

Let $J$ be a set of [[morphisms]] in a [[category]] $C$.  An **algebraically $J$-injective object** is an object $X\in C$ equipped with the [[stuff, structure, property|structure]] of, for every morphism $i:A\to B$ in $J$ and every morphism $f:A\to X$, a specified morphism $g:B\to X$ such that $g \circ i = f$.

## Properties

### Algebras for a pointed endofunctor

Assuming that $C$ is [[locally small category|locally small]] and [[cocomplete]] (and $J$ is a small set), given an object $X$, let $F_J X$ be the following pushout:
$$
\array{
\coprod_{i:A\to B} (C(A,X) \cdot A) & \to & X \\
\downarrow & & \downarrow \\
\coprod_{i:A\to B} (C(A,X) \cdot B) & \to & F_J X
}
$$
where $\cdot$ represents the [[copower]] of $C$ over [[Set]].  Then $F_J$ is a [[pointed endofunctor]] of $C$, such that the (pointed) [[algebra for an endofunctor|endofunctor algebras]] of $F_J$ are precisely the algebraically $J$-injective objects.

### Monadicity

When $C$ is locally small and cocomplete as before, if the [[algebraically-free monad]] on the pointed endofunctor $F_J$ exists, then by definition the algebraically $J$-injective objects are its [[algebra for a monad|monad algebras]].  In particular, they are [[monadic functor|monadic]] over $C$.

### Solidity

...

## Related pages

* [[injective object]]
* [[algebraic small object argument]]
* [[algebraically fibrant object]]

## References

* {#Bourke17} [[John Bourke]], _Equipping weak equivalences with algebraic structure_, 2017, [arxiv](https://arxiv.org/abs/1712.02523)

* {#Bourke18} [[John Bourke]], _Iterated algebraic injectivity and the faithfulness conjecture_, 2018, [arxiv](https://arxiv.org/abs/1811.09532)

[[!redirects algebraically injective objects]]
[[!redirects algebraic injective]]
[[!redirects algebraic injectives]]
