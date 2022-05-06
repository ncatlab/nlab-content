

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

The _table of Burnside marks_ (or _table of marks_, for short) of a [[finite group]] $G$ is the [[matrix]] indexed by [[conjugacy classes]] $[H]$ of [[subgroups]] $H \subset G$ whose $([H_i], [H_j])$-entry is the $[H_i]$-marks of $G/H_j$ (Def. \ref{BurnsideCharacter}), hence the number of [[fixed points]] of the [[action]] of $H_i$ on the [[coset space]] $G/H_j$:

$$
  M_{i j}
  \;\coloneqq\;
  \left\vert
    \left(G/H_j\right)^{H_i}
  \right\vert
  \,.
$$

=--

(e.g. [Pfeiffer 97](#Pfeiffer97), chapter _[The Burnside Ring and the Table of Marks](http://schmidt.ucg.ie/~goetz/pub/marks/node1.html#SECTION00010000000000000000)_)

+-- {: .num_example #TableOfMarksInTermsOfHoms}
###### Remark
**(table of marks in terms of homs)**

The expression of marks in terms of homs (Remark \ref{MarksInTermsOfHoms}) means here that the table of marks (Def. \ref{TableOfMarks}) is equivalently given by


$$
  M_{i j}
  \;\coloneqq\;
  \left\vert
    \left(G/H_j\right)^{H_i}
  \right\vert
  \;=\;
  \left\vert Hom_{G Set}(G/H_i, G/H_j)\right\vert
  \,.
$$


=--

## Properties

The following says that the Burnside character plays the same role for finite [[G-sets]] as [[characters of representations]] play for finite-dimensional [[linear representations]]:

+-- {: .num_prop #BurnsideCharacterIsInjective}
###### Proposition
**([[Burnside character]] is [[injective function|injective]])**

The Burnside character (eq:BurnsideCharacter) is [[injective function|injective]]. Hence any two [[finite set|finite]] [[G-sets]] are [[isomorphism|isomorphic]] precisely if they have the same Burnside marks (Def. \ref{BurnsideCharacter}).

=--

(e.g. [tomDieck 79, Prop. 1.2.2](#tomDieck79), [tomDieck 09, Prop. 5.1.1](#tomDieck09))



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




