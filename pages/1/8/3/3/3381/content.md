
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

Classically, a __permutation__ on a [[set]] $X$ can be thought of in one of two different ways: either as a [[bijection]] from $X$ to itself, or as a pair of [[linear orderings]] on $X$.
In the case of a set that is already equipped with a natural ordering (such as a finite [[ordinal]] $X = \{1,\dots,n\}$), these two ways of defining permutations are interchangeable, but they correspond to different abstract [[structures]] that are more salient in different contexts, and to different natural ways of comparing permutations.
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

## Cycles and partitions

### Cycle decomposition

As an element of the symmetric group $S_X$, every permutation $\sigma : X \to X$ generates a [[cyclic group|cyclic]] [[subgroup]] $\langle \sigma \rangle$, and hence inherits a [[group action]] on $X$.  The [[orbits]] of this action partition the set $X$ into a disjoint union of cycles, called the **cyclic decomposition** of the permutation $\sigma$.

For example, let $\sigma$ be the permutation on $(6)$ defined by

$$\sigma = (\array{1 \mapsto 1 & 2 \mapsto 4 & 3 \mapsto 5 & 4 \mapsto 6 & 5 \mapsto 3 & 6 \mapsto 2})$$

The domain of the permutation is partitioned into three $\langle\sigma\rangle$-orbits 

$$(6) = \{1\} \cup \{2,4,6\} \cup \{3,5\}$$

corresponding to the three cycles

$$1 \underset{\sigma}{\to} 1 \qquad
2 \underset{\sigma}{\to} 4 \underset{\sigma}{\to} 6 \underset{\sigma}{\to} 2 \qquad
3 \underset{\sigma}{\to} 5 \underset{\sigma}{\to} 3$$

We can express this more compactly by writing $\sigma$ in "cycle notation", as the composition $\sigma = (1)(2\,4\,6)(3\,5)$, or $\sigma = (2\,4\,6)(3\,5)$ leaving implicit the action of the identity (1).

### Conjugacy classes
 {#ConjugacyClasses}


+-- {: .num_prop #ConjugacycClassesOfSymmetricGroupCorrespondToCycleSet}
###### Proposition

Let $n \in \mathbb{N}$ and $\Sigma(n)$ the [[symmetric group]]
on $n$ elements. Then the [[conjugacy classes]] of elements of $\Sigma(n)$, hence of permutations of $n$ elements, correspond to the [[cycle]] structures: two elements are conjugate to each other precisely if they have the same number of distinct cycles of the same length, or in other words if they define the same underlying [[partition]] of $n$.

=--

+-- {: .num_example }
###### Example


For the symmetric group on three elements there are three such classes:

<div>
<div style="float:left;width:30%;margin:10%">
 <div style="padding-bottom:20px">(1 2 3) ~ (1 3 2)</div>
 <div style="padding-bottom:20px">(1 2)(3) ~ (1 3)(2) ~ (1)(2 3)</div>
 <div>(1)(2)(3)</div>
</div>
<div style="float:left;width:20%">
<div>
 <svg width="80" height="40" xmlns="http://www.w3.org/2000/svg" se:nonce="39384" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <desc>Young diagram (3)</desc>
 <g>
  <title>Layer 1</title>
  <rect x="10" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_1"/>
  <rect x="30" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_2"/>
  <rect x="50" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_3"/>
 </g>
 </svg>
</div>
<div>
 <svg width="60" height="60" xmlns="http://www.w3.org/2000/svg" se:nonce="39384" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <desc>Young diagram (2,1)</desc>
 <g>
  <title>Layer 1</title>
  <rect x="10" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_1"/>
  <rect x="30" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_2"/>
  <rect x="10" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_3"/>
 </g>
 </svg>
</div>
<div>
 <svg width="40" height="90" xmlns="http://www.w3.org/2000/svg" se:nonce="39384" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <desc>Young diagram (1,1,1)</desc>
 <g>
  <title>Layer 1</title>
  <rect x="10" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_1"/>
  <rect x="10" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_2"/>
  <rect x="10" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_3"/>
 </g>
 </svg>
</div>
</div>
<div style="float:left;width:20%">
<img src="https://ncatlab.org/nlab/files/The3SheetedCoveringsOfTheCircle.png" width="100">
</div>
</div>

=--

<div style="width:200px;height:30px"></div>

$\,$

$\,$

$\,$

$\,$

$\,$

$\,$

$\,$

## Properties


### Relation to the field with one element

One may regard the symmetric group $S_n$ as the [[general linear group]] in dimension $n$ on the [[field with one element]]  $GL(n,\mathbb{F}_1)$.

### Classifying space and universal Thom space
 {#ClassifyingSpaceAndThomSpace}

The [[classifying space]] $B \Sigma(n)$ of the symmetric group on $n$ elements may be presented by $Emb(\{1,\cdots, n\}, \mathbb{R}^\infty)/\Sigma(n)$, the [[Fadell's configuration space]] on $n$ unordered points in $\mathbb{R}^\infty$.


Write $\tau_n$ for the [[rank]] $n$ [[vector bundle]] over this which exhibits the canonical [[action]] of $\Sigma(n)$ on $\mathbb{R}^n$, by permutation of [[coordinates]].

The [[Thom space]] $B \Sigma(n)^{\tau_n}$ of this bundle appears as the cofficients of the [[spectral symmetric algebra]] of the "absolute [[spectral superpoint]]" $Sym_{\mathbb{S}} \Sigma \mathbb{S}$ (see [Rezk 10, slide 4](spectral%20symmetric%20algebra#Rezk10)).


See also ([Hopkins-Mahowald-Sadofsky 94, around def. 2.8](#HopkinsMahowaldSadofsky94))





### Whitehead tower and relation to supersymmetry
 {#WhiteheadTowerAndSupersymmetry}

The [[symmetric groups]] and [[alternating groups]] are the first stages in a restriction of the [[Whitehead tower]] of the [[orthogonal group]] to "finite [[discrete ∞-groups]]" in the sense of [[homotopy type with finite homotopy groups]]. The [[homotopy fibers]] of the stages of the "finite Whitehead tower" are the [[stable homotopy groups of spheres]] ([Epa-Ganter 16](#EpaGanter16)). (See also at _[super algebra -- Abstract idea](super+algebra#AbstractIdea)_ and at _[[Platonic 2-group]]_.)

$$
  \array{   
    && && \vdots
    \\
    && && \downarrow
    \\
    && && \mathbf{B}Fivebrane(n)
    \\
    && \downarrow && \downarrow
    \\
    \mathbf{B}^2 \pi_3 \mathbb{S} 
      &\stackrel{}{\longrightarrow} & 
     \mathbf{B}\mathcal{A}_n &\hookrightarrow& \mathbf{B} String(n)
    \\
    && \downarrow && \downarrow
    \\
    \mathbf{B} \pi_2 \mathbb{S} &\longrightarrow & \mathbf{B} \tilde A_n &\hookrightarrow& \mathbf{B} Spin(n)
    \\
    && \downarrow && \downarrow
    \\
    \pi_1 \mathbb{S} &\longrightarrow& \mathbf{B} A_n &\hookrightarrow& \mathbf{B} SO(n)
    \\
    && \downarrow && \downarrow
    \\
    && \mathbf{B} S_n &\hookrightarrow& \mathbf{B} O(n)
  }
$$

* on the right: the [[delooping|delooped]] [[smooth ∞-group]] [[Whitehead tower]] of the [[orthogonal group]] ([[fivebrane 6-group]] $\to$ [[string 2-group]] $\to$ [[spin group]] $\to$ [[special orthogonal group]] $\to$ [[orthogonal group]]);

* in the middle, its restriction to [[deloopings]] of [[finite groups]] and their universal [[∞-group extensions]] ($\cdots \to $ [[covering of alternating group]] $\to$ [[alternating group]] $\to$ [[symmetric group]])

* on the left the [[homotopy fibers]] of each stage.


Notice that the squares on the right are _not_ [[homotopy pullback]] squares. (The homotopy pullback of the [[string 2-group]] along $\tilde A \hookrightarrow Spin(n)$ is a $\mathbf{B}U(1)$-extension of $\tilde  A$, but here we get the universal _finite_ 2-group extension, by $\mathbb{Z}/24$ instead.

## Examples

* The symmetric group on 4 elements is [[isomorphism|isomorphic]] to the full [[tetrahedral group]] as well as to the orientation-preserving [[octahedral group]].

## Related entries

* [[permutation representation]], [[permutation matrix]]

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

