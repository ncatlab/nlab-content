
# Sublocales
* table of contents
{: toc}

## Idea

A sublocale is a [[subspace]] of a [[locale]].

It is important to understand that, even for a [[topological locale]] $X$ (which can be identified with a [[sober space|sober]] [[topological space]]), most sublocales of $X$ are *not* topological.  Specifically, we have an [[inclusion function]] $Sub Top(X) \hookrightarrow Sub Loc(X)$ which, while [[injection|injective]], is usually far from [[surjection|surjective]].


## Definitions

Let $L$ be a [[locale]], which (as an [[object]]) is the same as a [[frame]].

A __sublocale__ of $L$ is a [[regular subobject]] of $L$ in [[Loc]], the [[category]] of locales.  Equivalently, it is a [[regular quotient]] of $L$ in [[Frm]], the category of [[frames]].

A sublocale is given precisely by a __[[nucleus]]__ on the underlying frame.  This is a [[function]] $j$ from the opens of $L$ to the opens of $L$ satisfying the following identities:

1.  $j(U \cap V) = j(U) \cap j(V)$,
2.  $U \subseteq j(U)$,
3.  $j(j(U)) = j(U)$.

In other words, a sublocale of $L$ is given by a [[meet]]-preserving [[monad]] on its frame of opens.

The precise reasons why nuclei correspond to quotient frames (and hence to sublocales) is given at [[nucleus]].  But the interpretation of the operation $j$ is this: we identify two opens if they 'agree on the sublocale'.  Given an open $U$, there will always be a largest open that is identified with $U$, so we can also describe a subspace of a locale as an operation that maps each open to its largest representative open in the sublocale.  This map is the nucleus $j$.


## Special cases

Of course, every locale $L$ is a sublocale of itself.  The corresponding nucleus is given by
$$ j_L(U) \coloneqq U ,$$
so every open is preserved in this sublocale.  Conversely, every locale has an [[empty subspace|empty]] sublocale, given by
$$j_\empty(U) \coloneqq L .$$

Suppose that $U$ is an open in the locale $L$.
Then $U$ defines an [[open subspace]] of $L$, also denoted $U$, given by
$$ j_U(V) \coloneqq U \Rightarrow V ,$$
so $j_U(V)$ is the largest open which agrees with $V$ on $U$.
$U$ also defines a [[closed subspace]] of $L$, denoted $U'$ (or any other notation for a [[complement]]), given by
$$ j_{U'}(V) \coloneqq U \cup V ,$$
so $j_{U'}(V)$ is the largest open which agrees with $V$ except on $U$.
If $L$ is [[topological locale|topological]], then every open sublocale of $L$ is also topological; the same goes for closed sublocales, assuming [[excluded middle]].  Even in [[constructive mathematics]], however, open and closed sublocales are [[complements]] in the lattice of sublocales.

The [[double negation sublocale]] of $L$, denoted $L_{\neg\neg}$, is given by
$$ j_{\neg\neg}(U) \coloneqq \neg{\neg{U}} .$$
This is always a [[dense subspace]]; in fact, it is the *smallest* dense sublocale of $L$.  (As such, even when $L$ is topological, $L_{\neg\neg}$ is rarely topological; in fact, its only points are the [[isolated point]]s of $L$.)


## References

* _[[Stone Spaces]]_, II.2


[[!redirects sublocale]]
[[!redirects sublocales]]
[[!redirects localic subspace]]
[[!redirects localic subspaces]]
