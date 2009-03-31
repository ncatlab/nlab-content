#Idea#

A _null system_ in a [[triangulated category]] is a triangulated [[subcategory]] whose objects may consistently be regarded as being equivalent to the [[zero object]]. Null systems give a convenient means for encoding and computing [[localization]] of [[triangulated category|triangulated categories]].

#Definition#

A **null system** of a [[triangulated category]] $C$ is a full [[subcategory]] $N \subset C$ such that

* $N$ is _saturated_: every object $X$ in $C$ which is [[isomorphism|isomorphic]] in $C$ to an object in $N$ is in $N$;

* the [[zero object]] is in $N$;

* $X$ is in $N$ precisely if $T X$ is in $N$;

* if $X \to Y \to Z \to T X$ is a distinguished triangle in $C$ with $X, Z \in N$, then also $Y \in N$.

#Properties#

The point about null systems is the following:

for $N$ a null system, let $N Q$ be the collection of all morphisms in $C$ whose "[[mapping cone]]" is in $N$, precisely: set

$$
  N Q := \{ X \stackrel{f}{\to} Y | \exists dist. tri. X \to Y \to Z in C with Z \in N\}
  \,.
$$

Then
$N Q$ is a left and right [[multiplicative system]] in $C$.

#Examples#

* For $K(C)$ the [[category of chain complexes]] modulo [[chain homotopy]] of an [[abelian category]], the full [[subcategory]] of $K(C)$ of chain complexes $V$ whose [[homology]] vanishes, $H(V) \simeq 0$ is a null system.
Then$D(C) := K(C)/N$ is the [[derived category]] of $C$.

+-- {: .query}
[[David Roberts]]: Would [[Serre class]]es fit in here? Perhaps that's one step back.
=--

#References#

For instance section 10.2 of

* Kashiwara-Schapira, [[Categories and Sheaves]]