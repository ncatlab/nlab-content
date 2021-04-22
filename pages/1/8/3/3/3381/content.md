
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A __permutation__ on a [[set]] $X$ is equivalently

* a [[bijection]] from $X$ to itself, 

* a [[pair]] of [[linear orderings]] on $X$;

* an element in the [[symmetric group]] of $X$.


In the case of a set that is already equipped with a natural [[ordering]] (such as a finite [[ordinal]] $X = \{1,\dots,n\}$), these two ways of defining permutations are interchangeable, but they correspond to different abstract [[structures]] that are more salient in different contexts, and to different natural ways of comparing permutations.
Typically, the definition of permutations-as-[[automorphisms]] is important in [[group theory]], while the definition of permutations-as-linear-orders is more common in [[combinatorics]].
Both views of permutations are relevant to the theory of [[symmetric operads]].

## Definitions

### Permutations as automorphisms, and conjugacy

As automorphisms $\sigma : X \to X$ in [[Set]], the permutations of $X$ naturally form a [[group]] under [[composition]], called the __symmetric group__ (or __permutation group__) on $X$.
This group may be denoted $S_X$, $\Sigma_X$, or $X!$.
When $X$ is [[the]] [[finite set]] $(n) = \{1,\dots,n\}$, then its symmetric group is a [[finite group]] of [[cardinality]] $n!$ = "$n$ [[factorial]]", and one typically writes $S_n$ or $\Sigma_n$.

Two permutations $\sigma : X \to X$ and $\tau : Y \to Y$ are said to be **conjugate** (written $\sigma \cong \tau$) just in case there is a bijection $f : X \to Y$ such that $\sigma = f^{-1} \tau f$, or equivalently, when there is a commuting square of bijections:

$$\array{& X & \overset{f}\rightarrow & Y & \\
          \sigma & \downarrow &&\downarrow & \tau\\
          &X & \underset{f}\rightarrow& Y & \\
}$$

Observe that conjugacy is an [[equivalence relation]], and that conjugacy classes of permutations of $X$ are in one-to-one correspondence with [[partitions]] of $X$ (see below).

### Permutations as linear orders, and pattern containment

If $X$ is a set equipped with a [[linear ordering]] $\lt$, then a permutation of $X$ is the same thing as a second (unrelated) linear ordering $\lt_\sigma$ on $X$.
Indeed, suppose we label the elements of $X$ according to the $\lt$ order as $x_1 \lt x_2 \lt \dots$, and according to the $\lt_\sigma$ order as $\sigma_1 \lt_\sigma \sigma_2 \lt_\sigma \dots$.
Then we can define a bijection $\sigma : X \to X$ as the function sending $x_1 \mapsto \sigma_1$, $x_2 \mapsto \sigma_2$, and so on.
Conversely, any bijection $\sigma : X \to X$ induces a linear ordering $\lt_\sigma$ on $X$ by defining $x \lt_\sigma x'$ iff $\sigma(x) \lt \sigma(x')$.

This way of viewing permutations naturally gives rise to "array notation" (or "one-line notation"), where a permutation $\sigma : X \to X$ is represented as the list of elements $\sigma = (\sigma_1,\sigma_2,\dots)$, and it may be contrasted with "cycle notation" (see below).
Whereas cycle notation makes it easy to compare permutations for conjugacy, array notation leads to a different natural way of comparing permutations known as **pattern containment**.

Given two linearly ordered sets $(X,\lt_X)$ and $(Y,\lt_Y)$, a permutation (or "pattern") $\sigma : X \to X$ is said to be _contained_ in a permutation $\tau : Y \to Y$ (written $\sigma \preceq \tau$) just in case there exists a [[monotone function|monotone]] [[injective]] function $f : X \to Y$ such that
$$\sigma_i \lt_X \sigma_j \Rightarrow \tau_{f(i)} \lt_Y \tau_{f(j)}$$
for all $i,j \in X$, or in other words, if $\tau = (\tau_1,\tau_2,\dots)$ contains a subsequence of elements whose relative ordering (in $Y$) is the same as the relative ordering (in $X$) of the sequence $\sigma = (\sigma_1,\sigma_2,\dots)$.
Note that this definition of $\sigma \preceq \tau$ is equivalent to asking for the existence of a commuting square:

$$\array{& X & \overset{f}\rightarrow & Y & \\
          \sigma & \downarrow &&\downarrow & \tau\\
          &X & \underset{g}\rightarrow& Y & \\
}$$

where $f$ and $g$ are monotone injections (each uniquely determined by the other).

Whereas conjugacy defines an equivalence relation on the permutations of a particular set $X$, pattern containment defines a [[partial order]] on the permutations of arbitrary linearly ordered sets (which restricts to the [[equality|discrete order]] on the permutations of $X$).

### r-permutations

In combinatorics, one sometimes also wants a slight generalisation of the notion of permutation-as-linear-order: for any [[natural number]] $r$, an _$r$-permutation_ of $X$ is an [[injective function]] $\sigma : (r) \to X$.
An $r$-permutation corresponds to a list of $r$ distinct elements of $X$, so that for a finite set $X$ of cardinality $n = |X|$, an $n$-permutation is the same thing as an ordinary permutation of $X$ (it is [[surjective]] and therefore [[bijective]], since [[Set]] is a [[balanced category]]).
More generally, the number of $r$-permutations of a set of cardinality $n$ is counted by the [[falling factorial]] $n^{\underline{r}} = n(n-1)\dots(n-r+1)$.

## Properties

### Cycle decomposition

As an element of the [[symmetric group]] $S_X$, every permutation $\sigma : X \to X$ generates a [[cyclic group|cyclic]] [[subgroup]] $\langle \sigma \rangle$, and hence inherits a [[group action]] on $X$.  The [[orbits]] of this action partition the set $X$ into a disjoint union of cycles, called the **cyclic decomposition** of the permutation $\sigma$.

For example, let $\sigma$ be the permutation on $(6)$ defined by

$$\sigma = (\array{1 \mapsto 1 & 2 \mapsto 4 & 3 \mapsto 5 & 4 \mapsto 6 & 5 \mapsto 3 & 6 \mapsto 2})$$

The domain of the permutation is partitioned into three $\langle\sigma\rangle$-orbits 

$$(6) = \{1\} \cup \{2,4,6\} \cup \{3,5\}$$

corresponding to the three cycles

$$1 \underset{\sigma}{\to} 1 \qquad
2 \underset{\sigma}{\to} 4 \underset{\sigma}{\to} 6 \underset{\sigma}{\to} 2 \qquad
3 \underset{\sigma}{\to} 5 \underset{\sigma}{\to} 3$$

We can express this more compactly by writing $\sigma$ in "cycle notation", as the composition $\sigma = (1)(2\,4\,6)(3\,5)$, or $\sigma = (2\,4\,6)(3\,5)$ leaving implicit the action of the identity (1).



## Related entries

* [[permutation representation]], [[permutation matrix]]

* [[cyclic permutation]], [[rotation permutation]]

* [[transposition permutation]]

* [[alternating group]]

* [[signature of a permutation]]

* [[permutation category]]

* [[permutation D-brane]]

## References

* {#EpaGanter16} [[Narthana Epa]], [[Nora Ganter]], _Platonic and alternating 2-groups_, Higher Structures 1(1):122-146, 2017 ([arXiv:1605.09192](http://arxiv.org/abs/1605.09192))

* {#HopkinsMahowaldSadofsky94} [[Michael Hopkins]], [[Mark Mahowald]], [[Hal Sadofsky]], _Constructions of elements in Picard groups_, Contemporary mathematics, Volume 158, 1994 in [[Eric Friedlander]], [[Mark Mahowald]] (eds.), _Topology and Representation theory_ ([doi:10.1090/conm/158/01454](http://dx.doi.org/10.1090/conm/158/01454))

For the operadic structure of permutations, see Volume 1, Chapter 1 of:

* {#FresseHOGTG} [[Benoit Fresse]], _Homotopy of Operads and Grothendieck-Teichm&#252;ller Groups (Volumes 1 & 2)_, [website](http://math.univ-lille1.fr/~fresse/OperadHomotopyBook/) 

For more on permutation patterns, see:

* Wikipedia, [Permutation pattern](https://en.wikipedia.org/wiki/Permutation_pattern).

* Étienne Ghys, _A Singular Mathematical Promenade_, August 2017. [arXiv:1612.06373](https://arxiv.org/abs/1612.06373) [author pdf](http://perso.ens-lyon.fr/ghys/promenade/)

[[!redirects permutation]]
[[!redirects permutations]]

[[!redirects cycle notation]]
[[!redirects cycle notations]]

