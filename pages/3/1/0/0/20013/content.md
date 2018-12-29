

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

The _table of Burnside marks_ (or _table of marks_, for short) of a [[finite group]] $G$ is the [[matrix]] indexed by [[conjugacy classes]] $[H]$ of [[subgroups]] $H \subset G$ whose $[H_i], [H_j]$-entry is the [[cardinality]] of the [[set]] of [[fixed points]] (hence the number of fixed points) of the [[action]] of $H_j$ on the [[coset space]] $G/H_i$:

$$
  M_{i j}
  \;\coloneqq\;
  \left\vert
    \left(G/H_j\right)^{H_i}
  \right\vert
  \,.
$$

More generally: 

+-- {: .num_defn #BurnsideCharacter}
###### Definition
**([[Burnside character]])**

For $X \in G Set^{fin}$ any [[finite set|finite]] [[G-set]], its _$[H_i]$-mark_ is its number $\left\vert X^{H_i} \right\vert$ of $H_i$-[[fixed points]]. This construction extends to a [[ring homomorphism]]

\[
  \label{BurnsideCharacter}
  \array{
    \phi
    &\colon&
    A(G) &\overset{\phi}{\longrightarrow}& \mathbb{Z}^{Conj(G)}
    \\
    && [X] &\mapsto& \big( [H_i] \mapsto \left\vert X^H\right\vert\big)
  } 
\] 

from the [[Burnside ring]] to the ring of [[tuples]] of [[integers]] of length the number $Conj(G)$ of [[conjugacy classes]] of [[subgroups]] of $G$.

This morphism is also called the _Burnside character_ or _mark homomorphism_.

=--

## Properties

The following says that the Burnside character plays the same role for finite [[G-sets]] as [[group characters]] play for finite-dimensional [[representations]]:

+-- {: .num_prop #BurnsideCharacterIsInjective}
###### Proposition
**([[Burnside character]] is [[injective function|injective]])**

The Burnside character (eq:BurnsideCharacter) is [[injective function|injective]]. Hence any two [[finite set|finite]] [[G-sets]] are [[isomorphism|isomorphic]] precisely if they have the same Burnside marks.

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

See also 

* Götz Pfeiffer, _The Subgroups of _$M_{24}$_, or How to Compute the Table of Marks of a Finite Group_ ([web](http://schmidt.ucg.ie/~goetz/pub/marks/marks.html))

* Brendan Masterson, Götz Pfeiffer, _On the Table of Marks of a Direct Product of Finite Groups_, Journal of Algebra Volume 499, 1 April 2018, Pages 610-644 ([arXiv:1704.03433](https://arxiv.org/abs/1704.03433))


[[!redirects tables of marks]]

[[!redirects Burnside mark]]
[[!redirects Burnside marks]]

[[!redirects Burnside character]]
[[!redirects Burnside characters]]

[[!redirects mark homomorphism]]
[[!redirects mark homomorphisms]]




