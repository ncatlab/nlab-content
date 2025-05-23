
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

After localization at primes dividing $n \in \mathbb{N}$, the [[covering]] of the [[moduli stack of elliptic curves]] $\mathcal{M}_{{ell}}$ by that of [[elliptic curves with level-n structure]], $\mathcal{M}_{{ell}}[n] \to \mathcal{M}_{{ell}}$, is sufficiently good that the [[Goerss-Hopkins-Miller-Lurie theorem]] may be applied to produce a [[homomorphism]] of [[E-∞ rings]]

$$
  (TMF \to TMF(n)) 
   = 
  \Gamma\left(
    \left(
      \mathcal{M}_{\overline{ell}}[n] \to \mathcal{M}_{\overline{ell}} 
    \right), 
    \mathcal{O}^{top}
  \right)
$$

exhibiting [[TMF]] (after localization at $n$) as the [[homotopy fixed points]] of a [[modular group]] action by $SL_2(\mathbb{Z}/n\mathbb{Z})$ ([Hill & Lawson 2013 p.3](#HillLawson13)).

With a bit more work one obtains analogous statements for the [[Deligne-Mumford compactification|compactified]] [[moduli stack of elliptic curves]] and $Tmf$ instead of $TMF$ ([Hill & Lawson 2013 Theorem 9.1](#HillLawson13))

This is directly analogous ([Lawson & Naumann 2012](#LawsonNaumann12), [Hill-Lawson 13](#HillLawson13)) to how [[KO]] $\to$ [[KU]] exhibits the inclusion of the homotopy fixed points of the $\mathbb{Z}_2$-action on [[complex K-theory]] (which defines [[KR-theory]], see there for more).

See also at _[[modular equivariant elliptic cohomology]]_.


## References

* {#MahowaldRezk09} [[Mark Mahowald]] [[Charles Rezk]], _Topological modular forms of level 3_, Pure Appl. Math. Quar. 5 (2009) 853-872 ([pdf](http://www.math.uiuc.edu/~rezk/tmf3-paper-final.pdf))

* {#DavisMahowald10} [[Donald Davis]], [[Mark Mahowald]], _Connective versions of $TMF(3)$_ ([arXiv:1005.3752](http://arxiv.org/abs/1005.3752))


* {#Stojanoska11} [[Vesna Stojanoska]], Duality for Topological Modular Forms ([arXiv:1105.3968](http://arxiv.org/abs/1105.3968))

* {#LawsonNaumann12} [[Tyler Lawson]], [[Niko Naumann]], _Strictly commutative realizations of diagrams over the Steenrod algebra and topological modular forms at the prime 2_, Int. Math.
Res. Not. (2013) ([arXiv:1203.1696](http://arxiv.org/abs/1203.1696))

* {#HillLawson13} [[Michael Hill]], [[Tyler Lawson]], _Topological modular forms with level structure_ ([arXiv:1312.7394](http://arxiv.org/abs/1312.7394))

[[!redirects tmf(n)]]