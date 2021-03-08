> This page is about a [[categorification]] of the notion of [[polynomial functor]].  For the notion of "polynomial $\infty$-functor" used in [[Goodwillie calculus]], see [[n-excisive (∞,1)-functor]].

# Polynomial $(\infty,1)$-functors

* table of contents
{: toc}

## Idea

A **polynomial $(\infty,1)$-functor** is a [[categorification]] of the notion of [[polynomial functor]].

## Definition

Recall that a map of spaces $f\colon I\to J$
induces an adjoint triple
$$f_!\dashv f^*\dashv f_*,$$
where $f^*\colon S/J\to S/I$ is the base change functor.

A __polynomial $(\infty,1)$-functor__ is a functor $S/I\to S/J$
equivalent to a functor of the form $t_! p_* s^*$,
where
$$I \leftarrow E \to B\to J$$
are maps of spaces.

Polynomial functors are closed under compositions ([GHK, Theorem 2.1.8](#GHK)).

A functor $F\colon S/I\to S/J$
is polynomial
if and only if it is [[accessible functor|accessible]] and preserves weakly contractible limits,
the latter referring to limits indexed by categories whose [[nerve]]
is a weakly contractible [[simplicial set]],
see ([GHK, Theorem 2.2.3(ii)](#GHK)).

Recall that an $(\infty,1)$-functor $F\colon C\to D$
is a local right adjoint functor
if for any object $X\in C$ the induced functor
$$C/X\to D/F(X)$$
is a [[right adjoint functor]].

A functor $F\colon S/I\to S/J$
is polynomial if and only if it is a [[local right adjoint]] functor,
see ([GHK, Theorem 2.2.3(iii)](#GHK)).



## Related pages

* [[(∞,1)-operad]]

## References

{#GHK} [[David Gepner]], [[Rune Haugseng]], [[Joachim Kock]], _∞-Operads as Analytic Monads_, ([arXiv:1712.06469](https://arxiv.org/abs/1712.06469))

[[!redirects polynomial ∞-functors]]
[[!redirects polynomial (∞,1)-functor]]
[[!redirects polynomial (∞,1)-functors]]
[[!redirects polynomial infinity-functor]]
[[!redirects polynomial infinity-functors]]
[[!redirects polynomial (infinity,1)-functor]]
[[!redirects polynomial (infinity,1)-functors]]
