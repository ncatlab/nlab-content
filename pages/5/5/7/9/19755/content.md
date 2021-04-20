

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

The [[permutations]] of a [[set]] $X$ form a [[group]], $S_X$, under [[composition]].  This is especially clear if one thinks of the permutation as a [[bijection]] on $X$, where the multiplication / composition is just composition of [[functions]]. This group is called the _symmetric group_ of $X$ and often denoted $S_X$, $\Sigma_X$, $Sym(X)$ or similar.

The [[subgroups]] of symmetric groups are the _[[permutation groups]]_.

When $X$ is [[the]] [[finite set]] $(n) = \{1,\dots,n\}$, then its symmetric group is a [[finite group]] of [[cardinality]] $n!$ = "$n$ [[factorial]]", and one typically writes $S_n$ or $\Sigma_n$. 

(We will make frequent use of the entry [[permutation]] for some key notation and concepts.)

In general, an element of $S_n$ can be represented by a two row array

$$\sigma= \left(\array{1&2&\ldots &n\\\sigma(1)&\sigma(2)&\ldots&\sigma(n)}\right).$$

It can also be given in cycle notation. We repeat the example from the entry on [[permutations]]. This is from $S_6$:

Let $\sigma$ be the permutation on $(6)$ defined by

$$\sigma = (\array{1 \mapsto 1 & 2\mapsto 4 & 3 \mapsto 5 & 4 \mapsto 6 & 5 \mapsto 3 & 6 \mapsto 2})= \left(\array{1&2&3&4&5&6\\1&4&5&6&3&2}\right)$$

The domain of the permutation is partitioned into three $\langle\sigma\rangle$-orbits 

$$(6) = \{1\} \cup \{2,4,6\} \cup \{3,5\}$$

corresponding to the three cycles

$$1 \underset{\sigma}{\to} 1 \qquad
2 \underset{\sigma}{\to} 4 \underset{\sigma}{\to} 6 \underset{\sigma}{\to} 2 \qquad
3 \underset{\sigma}{\to} 5 \underset{\sigma}{\to} 3$$

We express this more compactly by writing $\sigma$ as the composition $\sigma = (1)(2\,4\,6)(3\,5)$, or $\sigma = (2\,4\,6)(3\,5)$ leaving implicit the action of the identity (1).

We can also write $\sigma$ as a product of transpositions

$$(2\,4)(2\,6)(3\,5)$$



## Examples

### The symmetric group  $S_3$

$S_3$ is the group of permutations of $(3)=\{1,2,3\}$.

One simple way to represent an element of $S_3$ is by listing the $(3)$ on the top row of an array with a second row denoting the image of each element under the permutation.  For instance, the element $sigma= (1\mapsto 2, 2\mapsto 1, 3\mapsto 3)$ can be written more compactly as 

$$\sigma= \left(\array{1&2&3\\2&1&3}\right).$$

We can also use, even more compactly, 'cycle notation', as explained in more detail at [[permutation]], in which successive images under the permutation, $\sigma$, are listed until you get back to where you started. Elements of (3), or more generally of (n),  are usually not listed as cycles of length 1, exept that (1) may be used to indicate the identity element. For the above permutation, this gives

$$\sigma = (1\,2)$$

the _transposition_ exchanging the elements 1 and 2 and leaving 3 'unmoved'.  Whilst the 3-cycle, $(1\,2\,3)$, shifts every element to the right one position and then maps 3 to 1. 

\begin{example}\label{CayleyGraphOfSym3}
**([[Cayley graph of Sym(3)]])**
The following shows the [[Cayley graph]] of the [[symmetric groups]] on 3 elements, $Sym(3)$, with [[edges]] corresponding to any [[transposition]] (not necessarily adjacent), hence whose [[graph distance]] is the [[Cayley distance]]:

\begin{tikzcd}[row sep=-6pt, column sep=14pt]
  123
  \ar[rrrr,-]
  \ar[ddddd,-]
  \ar[ddrrr,-]
  &&
  &&
  132
  \ar[ddddd,-]
  \\
  {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A}}}}}}}}
  \\
  &&&
  \scalebox{.8}{$321$}
  \ar[dddr,-]
  \\
  &
  \scalebox{1.2}{231}
  \ar[ddl,-]
  \ar[uuurrr,-, crossing over]
  \ar[urr,-]
  \\
  {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A}}}}}}}}
  \\
  213
  \ar[rrrr,-]
  &&&&
  312
\end{tikzcd}

\end{example}


### The symmetric group $S_4$

The symmetric group on 4 elements is [[isomorphism|isomorphic]] to the full [[tetrahedral group]] as well as to the orientation-preserving [[octahedral group]].



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

 
Even in the simple example of $S_3$ one can see some patterns. 

* $(12)$ clearly has order 2, whilst $(123)$ has square $(132)$, which is also the inverse of $(123)$, and has order 3.

* $(123) = (12)(13)$, so transpositions generate the whole group.

This gives a listing of the elements of $S_3$ as 

$$\{ 1, (12),(13),(23),(123),(132)\}.$$

* $S_3$ has a [[group presentation|presentation]]

$$\langle a,b | a^3, b^2,(a b)^2 \rangle.$$

where $a$ corresponds to the 3-cycle, $(123)$, whilst $b$ corresponds to any transposition.  It also has a presentation in which the generators correspond to the transpositions:

$$\langle \sigma_1,\sigma_2 | \sigma_1^2,\sigma_2^2, (\sigma_1\sigma_2)^3\rangle$$

It is easy to see that these relations imply that 

$$\sigma_1\sigma_2\sigma_1= \sigma_2\sigma_1\sigma_2$$

which relates this symmetric group to the [[braid group]], **Br 3**, and to the [[trefoil knot|trefoil group]].  It is clear that there is an epimorphism $S_3\to Br_3$ obtained by making the two braid generators become the transpositions. 


### Relation to the field with one element

One may regard the symmetric group $S_n$ as the [[general linear group]] in dimension $n$ on the [[field with one element]]  $GL(n,\mathbb{F}_1)$.

See [there](field+with+one+element#AlgebraOverF1).


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


### Classifying space and universal Thom space
 {#ClassifyingSpaceAndThomSpace}

The [[classifying space]] $B \Sigma(n)$ of the symmetric group on $n$ elements may be presented by $Emb(\{1,\cdots, n\}, \mathbb{R}^\infty)/\Sigma(n)$, the [[Fadell's configuration space]] on $n$ unordered points in $\mathbb{R}^\infty$.


(e.g. [Bödigheimer 87, Example 10](#Boedigheimer87))

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



## Related entries

* [[permutation]], [[permutation representation]], [[permutation matrix]]

* [[braid group]]

* [[alternating group]]

* [[signature of a permutation]]

* [[permutation category]]

* [[permutation D-brane]]



## References

### General

Textbook accounts include

* {#Sagan01} [[Bruce Sagan]], _The symmetric group_, Springer 2001 ([pdf](http://math.sfsu.edu/federico/Clase/RepTh/sagan.pdf))

Discussion of the [[classifying spaces]] of symetric groups includes

* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf))


See also 

* Wikipedia, _[Symmetric group](https://en.wikipedia.org/wiki/Symmetric_group)_

* {#EpaGanter16} [[Narthana Epa]], [[Nora Ganter]], _Platonic and alternating 2-groups_, Higher Structures 1(1):122-146, 2017 ([arXiv:1605.09192](http://arxiv.org/abs/1605.09192))

* {#HopkinsMahowaldSadofsky94} [[Michael Hopkins]], [[Mark Mahowald]], [[Hal Sadofsky]], _Constructions of elements in Picard groups_, Contemporary mathematics, Volume 158, 1994 in [[Eric Friedlander]], [[Mark Mahowald]] (eds.), _Topology and Representation theory_ ([doi:10.1090/conm/158/01454](http://dx.doi.org/10.1090/conm/158/01454))

For the operadic structure of permutations:

* {#FresseHOGTG} [[Benoit Fresse]], Volume 1, Chapter 1 of: _Homotopy of Operads and Grothendieck-Teichm&#252;ller Groups (Volumes 1 & 2)_, [website](http://math.univ-lille1.fr/~fresse/OperadHomotopyBook/) 

For more on permutation patterns, see:

* Wikipedia, [Permutation pattern](https://en.wikipedia.org/wiki/Permutation_pattern).

* Étienne Ghys, _A Singular Mathematical Promenade_, August 2017. [arXiv:1612.06373](https://arxiv.org/abs/1612.06373) [author pdf](http://perso.ens-lyon.fr/ghys/promenade/)

### Kernels

On the [[Cayley graph]] of the [[symmetric group]] and the corresponding distance kernel:

* Mohammad Hossein Ghaffri, Zohreh Mostaghim, _Distance in Cayley graphs on permutations generated by $k m$ cycles_, Transactions on Combinatorics, Vol 6 No. 3 (2017) ([[GhaffriMostaghim17.pdf:file]])

Other kernels on the symmetric groups:

* Yunlong Jiao, Jean-Philippe Vert, _The Kendall and Mallows Kernels for Permutations_, Proceedings of Machine Learning Research, Volume 37: International Conference on Machine Learning, 7-9 July 2015, Lille ([publisher](http://proceedings.mlr.press/v37/jiao15.html), [pdf](http://proceedings.mlr.press/v37/jiao15.pdf))


[[!redirects symmetric groups]]