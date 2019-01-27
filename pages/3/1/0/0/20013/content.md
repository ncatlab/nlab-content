

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

### General

The following says that the [[Burnside character]] plays the same role for finite [[G-sets]] as [[characters of representations]] play for finite-dimensional [[linear representations]]:

+-- {: .num_prop #BurnsideCharacterIsInjective}
###### Proposition
**([[Burnside character]] is [[injective function|injective]])**

The Burnside character (eq:BurnsideCharacter) is [[injective function|injective]]. Hence any two [[finite set|finite]] [[G-sets]] are [[isomorphism|isomorphic]] precisely if they have the same Burnside marks (Def. \ref{BurnsideCharacter}).

=--

(e.g. [tomDieck 79, Prop. 1.2.2](#tomDieck79), [tomDieck 09, Prop. 5.1.1](#tomDieck09))

Notice that

+-- {: .num_prop #LinearOrderOnConjugacyClassesOfSubgroups}
###### Lemma
**([[linear order]] on set of [[conjugacy classes]] of [[subgroups]])**

There exists a [[linear order]] $\leq_{lin}$ on the [[set]] of [[conjugacy classes]] $[H]$ of [[subgroups]] of $G$ such that a subgroup inclusion $H \subset H'$ implies that $[H] \leq_{lin} [H']$.

=--

+-- {: .proof}
###### Proof

This follows by the general existence of [[linear extensions of partial orders]] applied to the [[subgroup lattice]] of $G$.

=--

+-- {: .num_prop #TableOfMarksIsInvertibleUpperTriangular}
###### Proposition
**([[table of marks]] is [[upper-triangular matrix|upper-triangular]] [[invertible matrix]])**


With respect to any [[linear order]] on the [[conjugacy classes]] of subgroups as in Lemma \ref{LinearOrderOnConjugacyClassesOfSubgroups},  the [[table of marks]] (Def. \ref{TableOfMarks}) becomes a [[lower triangular matrix]] over the [[integers]] with non-[[zero]] entries on the diagonal. Therefore it is in particular an [[invertible matrix]]

=--

+-- {: .proof}
###### Proof

That the [[subgroup]] $H_j \subset G$ has any [[fixed points]] in $G/H_i$ means equivalently that $H_j$ is [[conjugation action|conjugate]] to a [[subgroup]] of the [[stabilizer group]] of $[e] = \in G/H_i$. But the latter group is manifestly $H_i$. This says that

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

hence that the matrix $M$ is [[lower triangular matrix|lower triangular]].

Finally, it is clear that at least $[e] \in G/H$ is fixed by $H$, which shows that he diaginal entries are positive.


=--

### Relation to Burnside product

We discuss how the [[table of marks]] is related to the [[Burnside ring]] of the given [[finite group]] $G$.

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

The Burnside ring structure constants  $\left( n_{i j}^\ell\right)$ (Def. \ref{BurnsideMultiplicities}) are equal to the following algebraic expression in the [[table of marks]] $\left( M_{i j}\right)$ and its [[inverse matrix]] $\left( \left(M^{-1}\right)^{m \ell} \right)$ (which exists by Prop. \ref{TableOfMarksIsInvertibleUpperTriangular}):

$$
  n_{i j}^\ell
  \;=\;
  \underset{m}{\sum}
  M_{i m} \cdot M_{j m}
  \cdot
  (M^{-1})^{m \ell}
$$

=--

+-- {: .proof}
###### Proof

We compute as follows:

$$
  \begin{aligned}
    \underset{\ell}{\sum}
    n_{i j}^\ell \cdot M_{\ell m}
    & =
    \underset{\ell}{\sum}
    n_{i j}^\ell 
    \cdot
    \left\vert
      Hom_G
      \big(
        G/H_m
        ,
        G/H_\ell
      \big)
    \right\vert
    \\
    & =
    \left\vert
      Hom_G
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
      Hom_G\big(
       G/H_m, 
       \;
       G/H_i \times G/H_j
      \big)
    \right\vert
    \\
    & =
    \left\vert
      Hom_G\big(
       G/H_m, 
       \;
       G/H_i 
      \big)
    \right\vert
    \cdot
    \left\vert
      Hom_G\big(
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

The claim now follows by [[matrix multiplication]] of both sides of this equation my $M^{-1}$.

=--




## Related concepts

* [[character table]]

## References

The concept was introduced in 

* {#Burnside1897} [[William Burnside]], chapter XII of _Theory of Groups of Finite Order_, 1897 ([pdf](http://www.gutenberg.org/files/40395/40395-pdf.pdf))

Textbook accounts and lecture notes include

* {#tomDieck79} [[Tammo tom Dieck]], _[[Transformation Groups and Representation Theory]]_ Lecture Notes in Mathematics 766 Springer 1979

* {#tomDieck09} [[Tammo tom Dieck]], section 5.1 of _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

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




