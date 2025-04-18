

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Sublocales
* table of contents
{: toc}

## Idea

A sublocale is a [[subspace]] of a [[locale]].

It is important to understand that, even for a [[topological locale]] $X$ (which can be identified with a [[sober space|sober]] [[topological space]]), most sublocales of $X$ are *not* topological.  Specifically, we have an [[inclusion function]] $Sub Top(X) \hookrightarrow Sub Loc(X)$ which, while [[injection|injective]], is usually far from [[surjection|surjective]].

Sublocales can also be defined for [[formal topologies]]. 

## Definitions

There are multiple equivalent ways to formally define this concept.


### In terms of regular monomorphisms of locales

Let $L$ be a [[locale]], which (as an [[object]]) is the same as a [[frame]].

A __sublocale__ of $L$ is a [[regular subobject]] of $L$ in [[Loc]], the [[category]] of locales.  Equivalently, it is a [[regular quotient]] of $L$ in [[Frm]], the category of [[frames]].

Equivalently, a sublocale of $L$ can be described as a [[morphism of frames]]
$L\to S$ whose underlying map of sets is surjective.


### In terms of subsets of opens

Given a [[regular monomorphism]] $i\colon S\to L$,
it induces an adjunction $f^*\dashv f_*$ between the underlying [[posets]].
The direct image map
$$f_*: S\to L$$
is an injection on underlying sets
such that if we equip its image $f_*(S)$ with the induced order,
it becomes a [[locale]] itself, and the inclusion $f_*(S)\to L$
is a localic map, i.e., it has a left adjoint that preserves finite meets.

Thus, sublocales of $L$ can be defined as subsets $S$ of $L$
such that $S$ is a [[locale]] once we equip it with the order induced from $L$,
and the left adjoint to the inclusion $S\to L$ exists and preserves finite meets.
(Proposition 2.2 in [Picado & Pultr 2012](#PicadoPultr12).)

(The inclusion $S\to L$ need not preserve joins, so in particular,
the lattice structure on $S$ may be different from that of $L$,
only the ordering is the same.)

Equivalently, sublocales of $L$ can also be described
([PP12 §2.1](#PicadoPultr12)) as subsets $S$ of $L$
that are closed under all meets and for any $s\in S$ and $x\in L$, we have $(x\to s)\in S$.


### Equivalence of these two definitions

Given a surjective [[morphism of frames]] $h\colon L\to S$,
the subset $h_*(S)$ is a sublocale of $L$.

Given a subset $S$ of a locale $L$ that is a sublocale,
the left adjoint $j^*\colon L\to S$ to the inclusion $j_*\colon S\to L$
is a surjective [[morphism of frames]].


### In terms of nuclei

A sublocale is given precisely by a __[[nucleus]]__ on the underlying frame.  This is a [[function]] $j$ from the opens of $L$ to the opens of $L$ satisfying the following identities:

1.  $j(U \cap V) = j(U) \cap j(V)$,
2.  $U \subseteq j(U)$,
3.  $j(j(U)) = j(U)$.

In other words, a sublocale of $L$ is given by a [[meet]]-preserving [[monad]] on its frame of opens.

The precise reasons why nuclei correspond to quotient frames (and hence to sublocales) is given at [[nucleus]].  But the interpretation of the operation $j$ is this: we identify two opens if they 'agree on the sublocale'.  Given an open $U$, there will always be a largest open that is identified with $U$, so we can also describe a subspace of a locale as an operation that maps each open to its largest representative open in the sublocale.  This map is the nucleus $j$.


### Equivalence of nuclei and other definitions

Given a nucleus $j$ on a [[frame]] $L$,
we construct a [[congruence]] on $L$
given by the equivalence relation $E$
consisting of all pairs $(x,y)$ ($x,y\in L$)
such that $j(x)=j(y)$.
The quotient map $L\to L/E$ is a surjective [[morphism of frames]].

Vice versa, given a congruence $E$ on $L$,
define $j(x)=\bigvee_{y\colon (x,y)\in E}y$.
Then $j$ is the nucleus corresponding to the sublocale $L\to L/E$.

Given a nucleus $j$, we can restrict its codomain to its set-theoretical image,
obtaining a surjective [[morphism of frames]] $L\to j(L)$.

Vice versa, given a surjective [[morphism of frames]] $h^*\colon L\to S$,
the composition $h_* h^*\colon L\to L$ is a nucleus on $L$.

Given a nucleus $j\colon L\to L$, the subset $j(L)$ is a sublocale.

Vice versa, given a subset $S\subset L$ that is a sublocale,
the corresponding nucleus $j\colon L\to L$
is given by the formula $j(a)=\bigwedge\{s\in S\mid a\le s\}$.


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


## Relation to topological subspaces

The underlying [[locale]] of a [[topological space]]
will typically have many sublocales that are not [[spatial locale|spatial]],
i.e., do not come from any [[topological space]].

However, any [[subset]] $S$ of a [[topological space]] $X$ can be equipped with the induced topology, which turns it into a subspace, whose underlying [[locale]] is a sublocale of $\Omega(X)$. This can be most easily seen in the language of surjective [[morphisms of frames]], since open sets in the induced topology are by definition intersections of $S$ and an open subset of $X$.

Thus, we have a canonical map from the set of (topological) subspaces of $X$ to the set of spatial sublocales of $\Omega X$.

This map is injective if $X$ satisfies the [[separation axiom]] $T_D$, e.g., is a [[Hausdorff space]] (VI.1.2 in [PP12](#PicadoPultr12)).

This map is a surjection if $X$ is a [[sober space]] (Proposition VI.2.2.1 in [PP12](#PicadoPultr12)).


## References

* [[Peter Johnstone]], II.2 in: *[[Stone Spaces]]*, Studies in Advanced Mathematics __3__, Cambridge University Press (1982, 1986) &lbrack;[ISBN:9780521337793](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/stone-spaces?format=PB&isbn=9780521337793)&rbrack;


* {#PicadoPultr12} [[Jorge Picado]], [[Aleš Pultr]]: _[[Frames and Locales]]_, Frontiers in Mathematics, Birkhäuser (2012) &lbrack;[doi:10.1007/978-3-0348-0154-6](https://doi.org/10.1007/978-3-0348-0154-6)&rbrack;

  

* [[Steven Vickers]]: *Sublocales in formal topology*, Journal of Symbolic Logic **72** 2 (2007) 463-482 &lbrack;[doi:10.2178/jsl/1185803619](https://doi.org/10.2178/jsl/1185803619)&rbrack;


[[!redirects sublocale]]
[[!redirects sublocales]]
[[!redirects localic subspace]]
[[!redirects localic subspaces]]
