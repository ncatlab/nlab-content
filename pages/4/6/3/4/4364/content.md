# Sublocales
* table of contents
{: toc}

## Idea

A sublocale is a [[subspace]] of a [[locale]].

It is important to understand that, even for a [[topological locale]] $X$ (which can be identified with a [[sober space|sober]] [[topological space]]), most sublocales of $X$ are *not* topological.  Specifically, we have an [[inclusion function]] $Sub Top(X) \hookrightarrow Sub Loc(X)$ which, while [[injection|injective]], is usually far from [[surjection|surjective]].


## Definitions

Let $L$ be a [[locale]], which (as an [[object]]) is the same as a [[frame]].

A __sublocale__ of $L$ is a [[regular subobject]] of $L$ in [[Loc]], the [[category]] of locales.  Equivalently, it is a [[regular quotient]] of $L$ in [[Frm]], the category of [[frame]].

A sublocale is given precisely by a __[[nucleus]]__ on the underlying frame.  This is a [[function]] $j$ from the opens of $L$ to the opens of $L$ satisfying the following identities:

1.  $j(U \cap V) = j(U) \cap j(V)$,
2.  $U \subseteq j(U)$,
3.  $j(j(U)) = j(U)$.

In other words, a sublocale of $L$ is given by a [[meet]]-preserving [[monad]] on its frame of opens.

The interpretation of the operation $j$ is that $j(U)$ is the largest open which 'agrees with $U$ on the subspace'.


## Correspondence between these

Given a locale $L$ and a nucleus $j$ as above, let $L/j$ be the set of opens $U$ such that $j(U) = U$.  Then $L/j$ is a frame in its own right, and we can interpret $j$ as a function from $L$ to $L/j$, which is in fact a frame [[homomorphism]].  Therefore, we have a locale morphism (a [[continuous map]]) $j\colon L/j \to L$.  This is in fact a [[regular monomorphism]].

Conversely, every [[regular monomorphism]] of locales is of this form.  (Need more details here ....)


## Special cases

Suppose that $U$ is an open in the locale $L$.  Then $U$ defines an [[open subspace]] of $L$, also denoted $U$, given by
$$ j_U(V) \coloneqq U \Rightarrow V ,$$
and a [[closed subspace]] of $L$, denoted $U'$ (or any other notation for a [[complement]]), given by
$$ j_{U'}(V) \coloneqq U \cup V .$$
If $L$ is [[topological locale|topological]], then every open or closed sublocale of $L$ is also topological.

The [[double negation]] sublocale of $L$, denoted $L_{\neg\neg}$, is given by
$$ j_{\neg\neg}(U) \coloneqq \neg{\neg{U}} .$$
This is always a [[dense subspace]]; in fact, it is the *smallest* dense sublocale of $L$.  (As such, even when $L$ is topological, $L_{\neg\neg}$ is topological only if $L$ is [[discrete space|discrete]].)


## References

* _[[Stone Spaces]]_, II.2


[[!redirects sublocale]]
[[!redirects sublocales]]
[[!redirects localic subspace]]
[[!redirects localic subspaces]]
