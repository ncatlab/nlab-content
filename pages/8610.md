
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

### Relation to &#233;tale cohomology

Galois cohomology of a [[field]] $k$ is essentially the
[[étale cohomology]] of the [[spectrum of a commutative ring|spectrum]]
$Spec(k)$.

See also at _[[comparison theorem (étale cohomology)]]_.


### In terms of cohesive homotopy type theory 
 {#InCohesiveHomotopyTypeTheory}

We make some comments on the formulation of Galois cohomology in [[cohesive homotopy type theory]].

As discussed at _[[Galois theory]]_, the [[absolute Galois group]] $G_{Galois}$ of a [[field]] $K$ is the [[fundamental group]] of the [[spectrum of a commutative ring|spectrum]] $X \coloneqq Spec(K)$. Hence its [[delooping]] $\mathbf{B}G_{Galois}$ is the [[fundamental groupoid]]

$$
  \Pi_1(X)  \simeq \mathbf{B}G_{Galois}
  \,.
$$ 

In [[cohesive homotopy type theory]] there exists the [[fundamental ∞-groupoid]]-construction  -- the [[shape modality]] $\Pi$ --

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

* [[Jean-Pierre Serre]], _Galois cohomology_, Springer Monographs in Mathematics (1997) doi:[10.1007/978-3-642-59141-9](https://doi.org/10.1007/978-3-642-59141-9)

  _Cohomologie galoisienne_, Lecture Notes in Mathematics, 5 (Fifth ed. 1994), Springer-Verlag, MR1324577 doi:[10.1007/BFb0108758)](https://doi.org/10.1007/BFb0108758)


* Gr&#233;gory Berhuy, _An introduction to Galois cohomology and its applications_ ([pdf](http://www-fourier.ujf-grenoble.fr/~berhuy/fichiers/NTUcourse.pdf))

* M. Kneser, _Lectures on Galois cohomology of classical groups_ ([pdf](http://www.math.tifr.res.in/~publ/ln/tifr47.pdf))

* Wikipedia, _[Galois cohomology](http://en.wikipedia.org/wiki/Galois_cohomology)_

A generalization in the setup of [[coring]]s:

* [[Tomasz Brzezi?ski]], _Descent cohomology and corings_, Comm Algebra 36:1894-1900, 2008, [math.RA/0601491](http://arxiv.org/abs/math/0601491)

In a [[model theory|model theoretic]] context:

* [[Anand Pillay]], _Remarks on Galois cohomology and definability_, The Journal of Symbolic Logic __62__:2 (1997) 487-492 [doi](https://doi.org/10.2307/2275542)
* B. Poizat,  _Une theorie de Galois imaginaire_, J. Symb. Logic __48__  (1983) 1151-1170. 


