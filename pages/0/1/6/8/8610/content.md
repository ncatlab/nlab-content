
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Galois cohomology_ is the [[group cohomology]] of [[Galois groups]] $G$. Specifically, for $G$ the Galois group of a [[field extension]] $L/K$, Galois cohomology refers to the group cohomology of $G$ with [[coefficients]] in a $G$-[[module]] naturally associated to $L$.

Galois cohomology is studied notably in the context of _[[algebraic number theory]]_.

## Properties

### In terms of cohesive homotopy type theory 
 {#InCohesiveHomotopyTypeTheory}

We make some comments on the formulation of Galois cohomology in [[cohesive homotopy type theory]].

As discussed at _[[Galois theory]]_, the [[absolute Galois group]] $G_{Galois}$ of a [[field]] $K$ is the [[fundamental group]] of the [[space]] $X \coloneqq Spec(K)$. Hence its [[delooping]] $\mathbf{B}G_{Galois}$ is the [[fundamental groupoid]]

$$
  \Pi_1(X)  \simeq \mathbf{B}G_{Galois}
  \,.
$$ 

In [[cohesive homotopy type theory]] there exists the [[fundamental ∞-groupoid]]-construction 

$$
  X \colon Type \;\vdash \; \Pi(X) \colon Type
  \,.
$$

Moreover, by the discussion at _[[group cohomology]]_ in the section _[group cohomology - In terms of homotopy type theory](http://ncatlab.org/nlab/show/group%20cohomology#InHomotopyTypeTheory)_

1. a $G_{Galois}$-[[module]] $A$ is a $\mathbf{B}G_{Galois}$-[[dependent type]];

1. the [[group cohomology]] is the [[dependent product]] over the [[function type]]

   $$
     \vdash \; \left( \prod_{x \colon \mathbf{B}G_{Galois}} \left( * \to A \right)\right) \colon Type
     \,.
   $$

Hence, generally in [[cohesive homotopy type theory]], for $X$ a [[type]] and 

$$
  x \colon \Pi(X) \;\vdash \; A(x) \colon Type
$$

a $\Pi(X)$-[[dependent type]], we can say that the corresponding _$\infty$-Galois cohomology_ is

$$
  \vdash \; \left( \prod_{x \colon \Pi(X)} \left( * \to A\right) \right)
  \colon Type
  \,.
$$

**Warning.** Currently there is not written down yet a [[model]] for [[cohesive homotopy type theory]] given by a [[cohesive (∞,1)-topos]] over a [[site]] like the [[étale site]].

## Examples

* [[Hilbert's theorem 90]]

## Related concepts

* [[algebraic number theory]]

## References

* [[John Tate]], _Galois cohomology_ ([pdf](http://modular.math.washington.edu/edu/2010/582e/refs/tate-galois_cohomology.pdf))

* [[Jean-Pierre Serre]], _Galois cohomology_, Springer Monographs in Mathematics (1997)

* Gr&#233;gory Berhuy, _An introduction to Galois cohomology and its applications_ ([pdf](http://www-fourier.ujf-grenoble.fr/~berhuy/fichiers/NTUcourse.pdf))

* M. Kneser, _Lectures on Galois cohomology of classical groups_ ([pdf](http://www.math.tifr.res.in/~publ/ln/tifr47.pdf))

* Wikipedia, _[Galois cohomology](http://en.wikipedia.org/wiki/Galois_cohomology)_


---
## Galois cohomology

[MathSciNet](http://www.ams.org/mathscinet/search/publications.html?pg4=AUCN&s4=&co4=AND&pg5=TI&s5=&co5=AND&pg6=PC&s6=&co6=AND&pg7=ALLF&s7=%22Galois+cohomology%22&co7=AND&Submit=Search&dr=all&yrop=eq&arg3=&yearRangeFirst=&yearRangeSecond=&pg8=ET&s8=All)

[Google Scholar](http://scholar.google.co.uk/scholar?q=%22Galois+cohomology%22&hl=en&lr=&btnG=Search)

[Google](http://www.google.com/search?hl=en&q=%22Galois+cohomology%22&btnG=Search)

[arXiv: Experimental full text search](http://search.arxiv.org:8081/?query=%22Galois+cohomology%22&in=)

[arXiv: Abstract search](http://front.math.ucdavis.edu/search?a=&t=&q=%22Galois+cohomology%22&c=&n=25&s=Abstracts)

category: Search results
---
## Galois cohomology

AAG (Arithmetic algebraic geometry), RT (Groups and representation theory)

category: World [private]
---
## Galois cohomology

Arithmetic

category: Labels [private]
---
## Galois cohomology

[arXiv:1009.2181](http://front.math.ucdavis.edu/1009.2181) Notes on Cohomology
from arXiv Front: math.NT by Luis Arenas-Carmona
This work is a collection of old and new aplications of Galois cohomology to
the clasification of algebraic and arithmetical objects.

category: Online References
---
## Galois cohomology

Serre: Galois cohomology.

See also a survey article by Serre in Asterisque (1995) on "Progres et Problemes" or something like that.

Kato: Galois cohomology of complete discrete valuation fields. LNM 967 (1982)

category: Paper References
---
## Galois cohomology

&lt;http://mathoverflow.net/questions/60310/galois-cohomology-groups-given-by-etale-cohomology>

&lt;http://mathoverflow.net/questions/28749/are-all-galois-cohomology-groups-also-etale-cohomology-groups>

category: Other Information
---
## Galois cohomology

Algebraic varieties, K-groups and the Hasse principle, by Cristian D. Gonzalez-Aviles: &lt;http://www.math.uiuc.edu/K-theory/0662>

Quotients of absolute Galois groups which determine the entire Galois cohomology by Chebolu  et al &lt;http://arxiv.org/abs/0905.1364>

[arXiv:1208.6359](http://front.math.ucdavis.edu/1208.6359) Local-global principles for Galois cohomology
from arXiv Front: math.NT by David Harbater, Julia Hartmann, Daniel Krashen
This paper proves local-global principles for Galois cohomology groups over
function fields $F$ of curves that are defined over a complete discretely
valued field. We show in particular that such principles hold for $H^n(F,
Z/mZ(n-1))$, for all $n>1$. This is motivated by work of Kato and others, where
such principles were shown in related cases for $n=3$. Using our results in
combination with cohomological invariants, we obtain local-global principles
for torsors and related algebraic structures over $F$. Our arguments rely on
ideas from patching as well as the Bloch-Kato conjecture.

category: Some Research Articles

nLab page on [[nlab:Galois cohomology]]
