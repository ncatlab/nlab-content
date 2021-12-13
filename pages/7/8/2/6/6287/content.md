
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A [[Lie algebra]] $\mathfrak{g}$ is called _reductive_ if the following equivalence conditions hold:

1. it is the [[direct sum]] $\mathfrak{g} \simeq \mathfrak{h} \oplus \mathfrak{a}$ of a [[semisimple Lie algebra]] $\mathfrak{h}$ and an abelian Lie algebra $\mathfrak{a}$;

1. its [[adjoint representation]] is completely [[reducible representation|reducible]]: every invariant subspace has an invariant complement.

{#OverAFieldOfCharacteristicZero} Over a [[field]] of [[characteristic zero]], the following conditions on $\mathfrak{g}$ are also equivalent to $\mathfrak{g}$ being reductive:

1. the radical of $\mathfrak{g}$ is equal to the centre of $\mathfrak{g}$ (in general, the radical is only contained inside the centre);

1. $\mathfrak{g}$ is a direct sum of its centre with a semisimple ideal;

1. $\mathfrak{g}$ is a direct sum of prime ideals.


More generally:

+-- {: .num_defn #LieAlgebraReductiveInAmbientLieAlgebra}
###### Definition
**([[reductive Lie algebra|Lie algebra reductive]] in ambient Lie algebra)**

A sub-[[Lie algebra]] 

$$
  \mathfrak{h} \hookrightarrow \mathfrak{g}
$$

is called _reductive_ if the [[adjoint representation|adjoint]] [[Lie algebra representation]] of $\mathfrak{h}$ on $\mathfrak{g}$ is [[reducible representation|reducible]].

=--

([Koszul 50](#Koszul50), recalled in e.g. [Solleveld 02, def. 2.27](#Solleveld02))



## Properties

* The [[Lie algebra]] of a [[compact space|compact]] and [[connected]] [[Lie group]] is reductive. ([GHV, vol III, section 4.4.](#GHV)).

* The graded algebra of [[invariant polynomial]]s on a reductive Lie algebra is the [[free construction|free]] graded algebra on the [[graded vector space]] of indecomposable invariant polynomials, and via [[transgression]] there generators are in bijection with the odd generators of the [[Lie algebra cohomology]].

[[!redirects reductive Lie algebras]]

## References
 
* {#Koszul50} [[Jean-Louis Koszul]], _Homologie et cohomologie des alg&egrave;bres de Lie_, Bull. Soc. Math. France 78 (1950), 65-127

* {#GHV} [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], volume III _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)
 

* {#Solleveld02} [[Maarten Solleveld]], _Lie algebra cohomology and Macdonald’s conjectures_, 2002 ([pdf](https://www.math.ru.nl/~solleveld/scrip.pdf))
