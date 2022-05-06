

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

## Definition

+-- {: .num_defn #BurnsideCharacter}
###### Definition
**([[Burnside marks]] and [[Burnside character]])**

Let $G$ be a [[finite group]] and let $X \in G Set^{fin}$ any [[finite set|finite]] [[G-set]]. For
$[H]$ the [[conjugacy class]] of a [[subgroup]] $H \subset G$, the _$[H]$-mark on $X$_ is the [[cardinality]] of the [[set]] of $H$-[[fixed points]], hence the [[natural number]]

$$
  \phi_{[H]}(X)
  \;\coloneqq\;
  \left\vert X^{H} \right\vert
$$ 

of [[elements]] $x \in X$ such that for each $h \in H \subset G$ we have $h(x) = x$. 

This construction extends to a [[ring homomorphism]]

\[
  \label{BurnsideCharacter}
  \array{
    \phi
    &\colon&
    A(G) &\overset{\phi}{\longrightarrow}& \mathbb{Z}^{Conj(G)}
    \\
    && [X] &\mapsto& \big( [H] \mapsto \left\vert X^H\right\vert\big)
  } 
\] 

from the [[Burnside ring]] to the ring of [[tuples]] of [[integers]] of length the number $Conj(G)$ of [[conjugacy classes]] of [[subgroups]] of $G$.

This morphism is also called the _Burnside character_ or _mark homomorphism_.

=--

+-- {: .num_remark #MarksInTermsOfHoms}
###### Remark
**(marks in terms of homs)**

Equivalent the set of $[H]$-marks of a [[G-set]] $X$ (Def. \ref{BurnsideCharacter}) is the [[hom-set]] in [[GSet]] from $G/H$ to $X$.

=--

+-- {: .proof}
###### Proof


This follows from a basic standard argument. For completeness, we make it explicit:

By [[transitive action|transitivity]] of the [[action]] on $G/H$ a $G$-equivariant function $f \colon G/H \to X$ is fully specified by its [[image]] $f([e]) \in X$ of the [[equivalence class]] $[e] \in G/H$ of the [[neutral element]]. Since this $[e] \in G/H$ is [[fixed point|fixed]] precisely by the elements in $H \subset G$ it may, again by $G$-equivariance, be mapped to any $H$-[[fixed point]] $f([e]) \in X^H \subset X$. 

=--

Of particular interest are the marks of the [[transitive action|transitive]] [[G-sets]], i.e. those [[isomorphism|isomorphic]] to sets $G/H$ of [[coset]], for $H\subset G$ a [[subgroup]].  These arrange into a _table of marks_:


+-- {: .num_defn #TableOfMarks}
###### Definition
**([[table of marks]])**

The _table of Burnside marks_ (or _table of marks_, for short) of a [[finite group]] $G$ is the [[matrix]] indexed by [[conjugacy classes]] $[H]$ of [[subgroups]] $H \subset G$ whose $([H_i], [H_j])$-entry is the $[H_j]$-marks of $G/H_i$ (Def. \ref{BurnsideCharacter}), hence the number of [[fixed points]] of the [[action]] of $H_j$ on the [[coset space]] $G/H_i$:

$$
  M_{i j}
  \;\coloneqq\;
  \left\vert
    \left(G/H_i\right)^{H_j}
  \right\vert
  \,.
$$

=--

(e.g. [Pfeiffer 97](#Pfeiffer97), chapter _[The Burnside Ring and the Table of Marks](http://schmidt.ucg.ie/~goetz/pub/marks/node1.html#SECTION00010000000000000000)_)

+-- {: .num_remark #TableOfMarksInTermsOfHoms}
###### Remark
**(table of marks in terms of homs)**

The expression of marks in terms of homs (Remark \ref{MarksInTermsOfHoms}) means here that the table of marks (Def. \ref{TableOfMarks}) is equivalently given by


$$
  M_{i j}
  \;\coloneqq\;
  \left\vert
    \left(G/H_i\right)^{H_j}
  \right\vert
  \;=\;
  \left\vert Hom_{G Set}(G/H_j, G/H_i)\right\vert
  \,.
$$

=--

<br/>

## Properties
 {#Properties}

### Relation to characters
 {#RelationToCharacters}

The following Prop. \ref{BurnsideCharacterIsInjective} that the [[Burnside character]] plays the same role for finite [[G-sets]] as [[characters of representations]] play for finite-dimensional [[linear representations]], in that it faithfully reflects $G$-sets. In fact the marks of a $G$-set over [[cyclic group|cyclic]] [[subgroups]] coincides with the [[character of a linear representation|character]] of its [[permutation representation]] over any [[ground field]] (Prop. \ref{MarkHomomorphismIsCharactersOfPermutationRepresentation}) below.

+-- {: .num_prop #BurnsideCharacterIsInjective}
###### Proposition
**([[Burnside character]] is [[injective function|injective]])**

The Burnside character (eq:BurnsideCharacter) is [[injective function|injective]]. Hence any two [[finite set|finite]] [[G-sets]] are [[isomorphism|isomorphic]] precisely if they have the same Burnside marks (Def. \ref{BurnsideCharacter}).

=--

(e.g. [tomDieck 79, Prop. 1.2.2](#tomDieck79), [tomDieck 09, Prop. 5.1.1](#tomDieck09))

+-- {: .num_prop #MarkHomomorphismIsCharactersOfPermutationRepresentation}
###### Proposition
**([[mark homomorphism]] on [[cyclic groups]] agrees with [[character of a linear representation|characters]] of corresponding [[permutation representations]])**

For $S \in G Set_{fin}$ a [[finite set|finite]] [[G-set]], for $k$ any [[field]] and $k[S] \in Rep_k(G)$ the corresponding [[permutation representation]], the [[character of a representation|character]] $\chi_{k[S]}$ of the [[permutation representation]] at any $g \in G$ equals the [[Burnside marks]] (Def. \ref{BurnsideCharacter}) of $S$ under the [[cyclic group]] $\langle g\rangle \subset G$ [[generators and relations|generated]] by $g$:

$$
  \chi_{k[S]}\big( g \big)
  \;=\;
  \left\vert X^{\langle g \rangle} \right\vert
  \;\in\;
  \mathbb{Z} \longrightarrow k
  \,.
$$

Hence the [[mark homomorphism]] (Def. \ref{BurnsideCharacter}) of $G$-sets restricted to [[cyclic group|cyclic]] [[subgroups]] coincides with the [[character of a representation|characters]] of their [[permutation representations]].

This statement immediately generalizes from plain representations to [[virtual representations]], hence to the [[Burnside ring]].

=--

(e.g. [tom Dieck 09, (2.15)](#tomDieck09))

+-- {: .proof}
###### Proof

By definition of _[[character of a linear representation]]_, we have that 

$$
  \chi_{k[S]}(g)
  = 
  tr_{k[S]}(g)
$$

is the [[trace]] of the [[linear map|linear]] [[endomorphism]] $k[S] \overset{g}{\to} k[S]$ of the given [[permutation representation]].

Now the canonical $k$-[[linear basis]] for $k[S]$ is of course the [[set]] $S$ itself, and so 

$$
  \begin{aligned}
    \chi_{k[S]}(g)
    & =
    \underset{
      s \in S
    }{\sum}
    \left\{
      \array{
         1 &\vert& g(s) = s
         \\
         0 &\vert& \text{otherwise}
      }
    \right.
    \\
    & = 
    \left\vert S^g \right\vert
    \\
    &
    =
    \left\vert S^{\langle g \rangle} \right\vert
  \end{aligned}
$$

Here in the first step we spelled out the definition of [[trace]] in the canonical basis, and in the second step we observed that the [[fixed point set]] of a [[cyclic group]] equals that of any one of its generating elements.

=--


### Relation to Burnside product
 {#RelationToBurnsideProduct}

We discuss, in Prop. \ref{BurnsideProductInTermsOfTableOfMarks} below, how the [[table of marks]] encodes the product in the [[Burnside ring]] of the given [[finite group]] $G$. For this purpose we first consider two Lemma: Lemma \ref{LinearOrderOnConjugacyClassesOfSubgroups} and Lemma \ref{TableOfMarksIsInvertibleUpperTriangular}.


+-- {: .num_prop #LinearOrderOnConjugacyClassesOfSubgroups}
###### Lemma
**([[linear order]] on set of [[conjugacy classes]] of [[subgroups]])**

There exists a [[linear order]] $\leq_{lin}$ on the [[set]] of [[conjugacy classes]] $[H]$ of [[subgroups]] of $G$ such that a subgroup inclusion $H \subset H'$ implies that $[H] \leq_{lin} [H']$.

=--

+-- {: .proof}
###### Proof

This follows by the general existence of [[linear extensions of partial orders]] applied to the [[subgroup lattice]] of $G$.

=--

+-- {: .num_lemma #TableOfMarksIsInvertibleUpperTriangular}
###### Lemma
**([[table of marks]] is [[lower triangular matrix|lower triangular]] [[invertible matrix]])**


With respect to any [[linear order]] on the [[conjugacy classes]] of subgroups as in Lemma \ref{LinearOrderOnConjugacyClassesOfSubgroups},  the [[table of marks]] (Def. \ref{TableOfMarks}) becomes a [[lower triangular matrix]] over the [[integers]] with non-[[zero]] entries on the diagonal. In  particular, it is an [[invertible matrix]].

=--

+-- {: .proof}
###### Proof

That the [[subgroup]] $H_j \subset G$ has any [[fixed points]] in $G/H_i$ means that there is a $g \in G$ such that $h g H_i = g H_i$ for all $h \in H_j$, and thus that $g^{-1}H_{j}g$ is a subgroup of $H_{i}$, or in other words, that $H_{j}$ is conjugate to a subgroup of $H_{i}$. Hence

$$
  \big(
    M_{i j} \gt 0
  \big)
  \;\Rightarrow\;
  \big(
    [H_j] \leq_{lin} [H_i]
  \big)
  \,,
$$ 

and thus the matrix $M$ is [[lower triangular matrix|lower triangular]].

Since at least $H = 1_{G/H}$ is fixed by $H$, we moreover have that the diagonal entries are non-zero.


=--


In the following, given a [[G-set]] $G/H_i$ we write $[G/H_i] \in A(G)$ for its [[isomorphism class]], regarded as an element in the [[Burnside ring]].

+-- {: .num_defn #BurnsideMultiplicities}
###### Definition
**(Burnside multiplicities)**

Given a choice of [[linear order]] on the [[conjugacy classes]] of [[subgroups]] of $G$ (for instance as in Lemma \ref{LinearOrderOnConjugacyClassesOfSubgroups}), we say that the corresponding _structure constants_ of the [[Burnside ring]] (or _Burnside multiplicities_) are the [[natural numbers]] 

\[
  n_{i j}^\ell \;\in\; \mathbb{N}
\] 

uniquely defined by the [[equation]]

\[
  \label{BurnsideStructureConstants}
  [G/H_i] \times [G/H_j]
  \;=\;
  \underset{ \ell }{\sum}
  n_{i j}^\ell [G/H_\ell]
  \,.
\]

=--

+-- {: .num_prop #BurnsideProductInTermsOfTableOfMarks}
###### Proposition
**([[Burnside ring]] product in terms of [[table of marks]])**

The Burnside ring structure constants  $\left( n_{i j}^\ell\right)$ (Def. \ref{BurnsideMultiplicities}) are equal to the following algebraic expression in the [[table of marks]] $\left( M_{i j}\right)$ and its [[inverse matrix]] $\left( \left(M^{-1}\right)_{r s} \right)$ (which exists by Lemma \ref{TableOfMarksIsInvertibleUpperTriangular}):

$$
  n_{i j}^\ell
  \;=\;
  \underset{m}{\sum}
  M_{i m} \cdot M_{j m}
  \cdot
  (M^{-1})_{m \ell}
$$

=--

+-- {: .proof}
###### Proof

Let $t$ be the dimension of $M$, i.e. $M$ is a $t \times t$ matrix. For any $1 \leq m \leq t$, we compute as follows:

$$
  \begin{aligned}
    \underset{1 \leq \ell \leq t}{\sum}
    n_{i j}^\ell \cdot M_{\ell m}
    & =
    \underset{1 \leq \ell \leq t}{\sum}
    n_{i j}^\ell 
    \cdot
    \left\vert
      Hom_{GSet}
      \big(
        G/H_m
        ,
        G/H_\ell
      \big)
    \right\vert
    \\
    & =
    \left\vert
      Hom_{GSet}
      \big(
        G/H_m
        ,
        \underset{\ell}{\sum}
        n_{i j}^\ell 
        \cdot
        G/H_\ell
      \big)
    \right\vert
    \\
    & =
    \left\vert
      Hom_{GSet}\big(
       G/H_m, 
       \;
       G/H_i \times G/H_j
      \big)
    \right\vert
    \\
    & =
    \left\vert
      Hom_{GSet}\big(
       G/H_m, 
       \;
       G/H_i 
      \big)
    \right\vert
    \cdot
    \left\vert
      Hom_{GSet}\big(
       G/H_m, 
       \;
       G/H_j
      \big)
    \right\vert
    \\
    & =
    M_{i m} \cdot M_{j m}
  \end{aligned}
$$

Here the third step uses the defining equation (eq:BurnsideStructureConstants) of the structure constants $n_{i j}^\ell$, while all other steps use that the mark homomorphism is a [[ring homomorphism]], which we made manifest by expressing the marks via [[hom-sets]] (Remark \ref{TableOfMarksInTermsOfHoms}).

Thus we have that $\left( n_{i j}^{1}, n_{i j}^{2}, \ldots, n_{i j}^{t} \right)$ is a solution to the following system of equations.

$$
\begin{aligned}
    M_{i 1} \cdot M_{j 1} &= M_{1 1}x_{1} + \cdots + M_{t 1}x_{t} \\
    M_{i 2} \cdot M_{j 2} &= M_{1 2}x_{1} + \cdots + M_{t 2} x_{t} \\
                          &\vdots \\
   M_{i t} \cdot M_{j t} &= M_{1 t}x_{1} + \cdots + M_{t t} x_{t}  
\end{aligned}
$$

But, since $M$ is invertible, the unique solution to this system of equations is given by the product of $M^{-1}$ and the transposition of $\left( M_{i 1} \cdot M_{j 1}, \ldots, M_{i t} \cdot M_{j t} \right)$. The claim follows immediately.

=--

\begin{corollary} The [[table of marks]] of a finite group determines its [[Burnside ring]]. That is to say, if the tables of marks of a pair of groups $G_{1}$ and $G_{2}$ are [[equality|equal]], then the Burnside ring of $G_{1}$ is [[isomorphism|isomorphic]] to the Burnside ring of $G_{2}$.
\end{corollary}

\begin{proof} The Burnside ring of a finite group is a free abelian group on the set $G / H_1, \ldots, G / H_t$, where $H_1, \ldots, H_t$ are representatives of the conjugacy classes of that group, equipped with a certain multiplication. Thus it suffices to check that the structure constants of the Burnside rings coincide, which is established by the previous proposition. \end{proof}

## Applications

* [[Burnside ring is equivariant stable cohomotopy of the point]]

## Related concepts

* [[character table]]

## References

The concept was introduced in 

* {#Burnside1897} [[William Burnside]], chapter XII of _Theory of Groups of Finite Order_, 1897 ([pdf](http://www.gutenberg.org/files/40395/40395-pdf.pdf))

* {#Burnside01} [[William Burnside]], _On the Representation of a Group of Finite Order as a Permutation Group, and on the Composition of Permutation Groups_, Proceedings of the American Mathematical Society 1901 ([doi:10.1112/plms/s1-34.1.159](https://doi.org/10.1112/plms/s1-34.1.159))



Modern textbook accounts and lecture notes:

* {#tomDieck79} [[Tammo tom Dieck]], _[[Transformation Groups and Representation Theory]]_ Lecture Notes in Mathematics 766 Springer 1979

* {#tomDieck09} [[Tammo tom Dieck]], sections 5.1 and 5.4 of _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

* {#LuxPahlings10} Klaus Lux, Herbert Pahlings, section 3.5 of _Representations of groups -- A computational approach_, Cambridge University Press 2010 ([author page](http://www.math.rwth-aachen.de/~RepresentationsOfGroups/), [publisher page](http://www.cambridge.org/catalogue/catalogue.asp?isbn=9780521768078))

Computer implementation is discussed in

* {#GAP} [GAP](https://www.gap-system.org/) [Reference Manual](https://www.gap-system.org/Manuals/doc/ref/chap0.html), _[70 Tables of Marks](https://www.gap-system.org/Manuals/doc/ref/chap70.html)_

See also 

* {#Pfeiffer97} [[Götz Pfeiffer]], _The Subgroups of $M_{24}$, or How to Compute the Table of Marks of a Finite Group_, Experiment. Math. 6 (1997), no. 3, 247–270 ([doi:10.1080/10586458.1997.10504613](https://doi.org/10.1080/10586458.1997.10504613), [web](http://schmidt.ucg.ie/~goetz/pub/marks/marks.html))

* Liam Naughton, [[Götz Pfeiffer]], _Computing the table of marks of a cyclic extension_, Math. Comp. 81 (2012), no. 280, 2419–2438. 

* Brendan Masterson, [[Götz Pfeiffer]], _On the Table of Marks of a Direct Product of Finite Groups_, Journal of Algebra Volume 499, 1 April 2018, Pages 610-644 ([arXiv:1704.03433](https://arxiv.org/abs/1704.03433))


[[!redirects tables of marks]]

[[!redirects Burnside mark]]
[[!redirects Burnside marks]]

[[!redirects Burnside character]]
[[!redirects Burnside characters]]

[[!redirects mark homomorphism]]
[[!redirects mark homomorphisms]]




