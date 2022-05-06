

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[representation theory]], one defines the _character of a [[linear representation]] $\rho\colon G\to End(V)$ to be the [[group character]] on $G$ given by $g \mapsto Tr \rho(g)$, whenever the [[trace]] in $V$ makes sense (e.g. when $V$ is [[finite-dimensional vector space|finite-dimensional]]).  Since such a function is invariant under conjugation, we may equivalently consider it a function on the set of [[conjugacy classes]] of elements in $G$.

Sometimes we also extend a character linearly to the free vector space on the set of conjugacy classes.  This version of the character can be identified with the [[bicategorical trace]] of the identity map of the representation, considered as a $k[G]$-$k$-module.

There is a different notion of an _infinitesimal character_ in [[Harish–Chandra theory]] and also a notion of the _formal character_.

There are important formulas concerning characters in representation theory, like [[Weyl character formula]], Kirillov character formula, Demazure character formula and so on.  There is also a formula for the [[induced character]] of an [[induced representation]].

## Properties

+-- {: .num_prop #InCharZeroCharacterMorphismIsInjective}
###### Proposition
**(in [[characteristic zero]] the [[character homomorphism]] is [[injective function|injective]])**

For $G$ a [[finite group]] and $k$ a [[field]] of [[characteristic zero]], the [[character homomorphism]]

$$
  \array{
    Rep_k(G)_{/\sim}
    &\overset{\chi}{\longrightarrow}&
    k^{ConjCl(G)}
    \\
    V 
      &\mapsto&
    \big(
      [g] \mapsto \chi_V(g) 
    \mathrlap{
      \coloneqq \mathrm{tr}_V(g)
    \big)
    }
  }
$$

is [[injective function|injective]].

=--

(e.g. [tom Dieck 09, Theorem (2.1.3)](#tomDieck09))


+-- {: .num_prop #NormalizedSumOfCharacters}
###### Proposition
**(normalized [[sum]] of [[character of a linear representation|characters]] is [[fixed point space]]-[[dimension]])**

Let $G$ be a [[finite group]] of [[order of a group|order]] ${\vert G \vert} \in \mathbb{N}$, and let $V \in Rep_k(G)$ be a [[linear representation]] over a [[ground field]] $k$ of [[characteristic zero]]. Then the [[dimension]] of the [[fixed point space]] $V^G$ of $V$ under $G$ equals the normalized [[sum]] of the characters over all group elements:

$$
  dim\left( V^G \right)
  \;=\;
  \frac{1}{{\vert G\vert}}
  \underset{g \in G}{\sum}
  \chi_V(g)
  \,.
$$
 
=--

(e.g. [tom Dieck 09 (2.1)](#tomDieck09))

## Related concepts

* [[equivariant K-theory]]

* [[fractional D-brane]]

## References

* {#tomDieck09} [[Tammo tom Dieck]], chapter 2 of _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

For more see the references at _[[representation theory]]_.

Character rings of [[compact Lie groups]] are discussed in 

* [[Graeme Segal]], _The representation ring of a compact Lie group_, Publications Math&#233;matiques de l'Institut des Hautes &#201;tudes Scientifiques
January 1968, Volume 34, Issue 1, pp 113-128 ([NUMDAM](http://archive.numdam.org/numdam-bin/fitem?id=PMIHES_1968__34__113_0))

* Masaru Tackeuchi, _A remark on the character ring of a compact Lie group_, J. Math. Soc. Japan Volume 23, Number 4 (1971), 555-705 ([Euclid](http://projecteuclid.org/euclid.jmsj/1259849785))

* Troels Roussauc Johansen, _Character Theory for Finite Groups and Compact Lie Groups_ [pdf](http://www.math.upb.de/~johansen/character-theory.pdf)

Discussion in the more general context of [[equivariant cohomology|equivariant]] [[complex oriented cohomology theory]] ([[transchromatic character]]) is in 

* [[Michael Hopkins]], [[Nicholas Kuhn]], [[Douglas Ravenel]], _Generalized group characters and complex oriented cohomology theories_, J. Amer. Math. Soc. 13 (2000), 553-594 ([publisher](http://www.ams.org/journals/jams/2000-13-03/S0894-0347-00-00332-5/), [pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/hkr.pdf))

for review see

* {#Raksit15} Arpon Raksit, _Characters in global equivariant homotopy theory_, 2015 [pdf](http://web.stanford.edu/~arpon/math/files/senior-thesis.pdf)


Examples of [[characters of linear representations]] of [[finite groups]] are discussed and listed at 

* {#Montaldi08} James Montaldi, _[representations](http://www.maths.manchester.ac.uk/~jm/wiki/Representations/Representations)_, 2008


[[!redirects characters of linear representations]]

[[!redirects character of a representation]]
[[!redirects characters of representations]]

[[!redirects character homomorphism]]
[[!redirects character homomorphisms]]

[[!redirects character morphism]]
[[!redirects character morphisms]]


[[!redirects character table]]
[[!redirects character tables]]


