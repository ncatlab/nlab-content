
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Tychonoff spaces
* table of contents
{: toc}

## Idea

A _Tychonoff space_ is a [[subspace]] of a [[compactum]].  By default, one usually means a Tychonoff [[topological space]], although there exist (even [[classical mathematics|classically]]) additional Tychonoff [[locales]].


## Definitions

The classical definition is:
+-- {: .num_defn #classical}
###### Definition
A [[topological space]] $X$ is __completely regular__ if, given a [[point]] $a$ of $X$ and a [[closed subset]] $F$ of $X$, if $a \notin F$, then there is a [[continuous map]] $f$ from $X$ to the [[real line]] $\mathbb{R}$ such that $f$ is [[constant function|constant]] when [[restriction|restricted]] to $F$ but takes a different value at $a$.
=--
(Traditionally, one requires $f(a) = 0$ and $f(F) = \{1\}$, but this can always be forced by postcomposition with an [[affine linear map]].  One sometimes sees, even more specifically, the requirement that $f$ land in the [[unit interval]] $[0,1]$, but this too can be forced since $[0,1]$ is a [[retract]] of $\mathbb{R}$.)

An equivalent definition focussing on open sets is this:
+-- {: .num_defn #constructive}
###### Definition
A [[topological space]] $X$ is __completely regular__ if, given a point $a$ of $X$ and an [[open neighbourhood]] $U$ of $a$ in $X$, there is a continuous $f\colon X \to \mathbb{R}$ and a [[real number]] $c$ such that $a \in f^*(\{c\}') \subseteq U$.
=--
(Here $f^*(\{c\}')$ is the [[preimage]] under $f$ of the [[complement]] of the [[singleton]] of $c$.  Again, one can force $c = 1$, $f(a) = 0$, and even $f\colon X \to [0,1]$ if desired.)  This definition is suitable for [[constructive mathematics]] based on [[weak countable choice]], [[Markov's principle]], and the [[fan theorem]] (all of which follow from [[excluded middle]]), or in any case if the following interpretations are made:

*  $f$ lands in the [[locale of real numbers]],
*  the complement $\{c\}'$ is the [[open subspace]] [[apartness|apart]] from $c$.


There is also a definition entirely in terms of the lattice of open sets, suitable for [[locales]], which I need to look up again.  (It\'s similar to the localic definition of [[regular space]], but using a stronger notion than well-inside.)

When a space is completely regular, we also often ask it to be $T_0$:

+-- {: .un_defn}
###### Definition 
**(of $T_0$)** 
Given any two points, if each neighbourhood of either is a neighbourhood of the other, then they are equal.
=--

A completely regular $T_0$-space is variously called a __$T_{3\frac{1}{2}}$-space__ (or __$T_{\pi}$-space__), a __completely regular Hausdorff space__ (since it is a theorem that such a space is [[Hausdorff space|Hausdorff]]), or a __Tychonoff space__ (or using other spellings of [[Tychonoff]]\'s name).

As is usual with the [[separation axioms]], some authors while conflate the meanings of 'completely regular' and '$T_{3\frac{1}{2}}$' either way, or even reverse them.  In contrast, the terms 'completely regular Hausdorff' and 'Tychonoff' are unambiguous.  The only unambiguous term for a completely regular space in general seems to be '$R_{2\frac{1}{2}}$', but this is not widely recognised.


## Properties

*  Every completely regular space is [[preregular space|preregular]], so every completely regular Hausdorff space (as defined above) really is Hausdorff.

*  Every completely regular space is [[regular space|regular]].

*  The [[natural transformation|natural map]] from a Tychonoff space to its [[Stone-Cech compactification]] (the [[unit of an adjunction|unit of the adjunction]]) really is a [[compactification]]  in that it is the inclusion of a [[dense subspace]] into a [[compact space]].  Conversely, any [[subspace]] of a [[compact Hausdorff space]] must be Tychonoff.

* Without $T_0$, we can say that a completely regular space embeds as a dense subspace of a [[compact regular space]], and any subspace of a compact regular space is complete regular.


## Examples

* Every [[metric space]] is Tychonoff (and every pseudometric space is completely regular).

* Every [[topological group]] is Tychonoff, if one requires groups to be Hausdorff; if not, then they are still completely regular.

* Every [[topological manifold]] is Tychonoff, if one requires manifolds to be Hausdorff.  (But if not, then the non-Hausdorff manifolds are *not* completely regular, indeed not even preregular, and in fact they are still $T_0$, indeed $T_1$.)

* Every [[CW-complex]] is Tychonoff.


## References

Named after [[A. N. Tychonoff]].

For a version appropriate to [[constructive mathematics|constructive]] (but impredicative) mathematics, see

* Bernhard Banaschewski, Ale&#353; Pultr; 2002; A Constructive View of Complete Regularity; [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.9.4811).


[[!redirects completely regular space]]
[[!redirects completely regular spaces]]
[[!redirects R-2-1/2 space]]
[[!redirects R-2-1/2 spaces]]

[[!redirects completely regular Hausdorff space]]
[[!redirects completely regular Hausdorff spaces]]
[[!redirects Tychonoff space]]
[[!redirects Tychonoff spaces]]
[[!redirects Tychonov space]]
[[!redirects Tychonov spaces]]
[[!redirects Tykhonov space]]
[[!redirects Tykhonov spaces]]
[[!redirects Tikhonov space]]
[[!redirects Tikhonov spaces]]
[[!redirects Tihonov space]]
[[!redirects Tihonov spaces]]
[[!redirects T-3-1/2 space]]
[[!redirects T-3-1/2 spaces]]
[[!redirects T-pi space]]
[[!redirects T-pi spaces]]

[[!redirects completely regular locale]]
[[!redirects completely regular locales]]

[[!redirects completely regular topological space]]
[[!redirects completely regular topological spaces]]
