
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A [[connected topological space|connected]] [[topological space]] $X$ (or rather its [[homotopy type]]) is called _nilpotent_ if 

1. its [[fundamental group]] $\pi_1(X)$ is a [[nilpotent group]];

1. the [[action]] of $\pi_1(X)$ on the higher [[homotopy groups]] is a [[nilpotent module]] in that the [[sequence]] $N_{0,n} \coloneqq \pi_n(X)$, $N_{k+1,n} \coloneqq \{g n - n | n \in N_{k,n}, g \in \pi_1(X)\}$ terminates.

## Examples

Directly from the definition we have that:

* every [[simply connected topological space]] is nilpotent;

and more generally

* every [[simple space]] is nilpotent.

As a special case of this

* every [[connected topological space|connected]] [[H-space]] is nilpotent

and thus 

* every [[loop space]] is nilpotent 

  (since all its connected components are homotopy equivalent to the unit component, which is a connected H-space).


(See [May-Ponto 12, p. 49 (77 of 542)](#MayPonto12))

* For $G$ a [[nilpotent group|nilpotent]] [[Lie group]], the [[classifying space]] $B G$ is a nilpotent space.

(See [Hilton 82, Section 3](#Hilton82)).



## Properties
 {#Properties}


Nilpotency is involved in sufficient conditions for many important constructions in ([[stable homotopy theory|stable]]) [[homotopy theory]], see for instance at 

* [[localization of a space]];

* [[fracture theorem]].

* [[fundamental theorem of dg-algebraic rational homotopy theory]]


## Related concepts

* [[nilpotent element]]

* [[nilpotent Lie algebra]], [[nilpotent L-infinity algebra]]

* [[nilpotent group]], [[nilpotent module]]

\linebreak

* [[connected topological space]]

* [[simply-connected topological space]]

* [[simple topological space]]

\linebreak

* [[rational homotopy theory]]

  * [[Sullivan model]]

  * [[rational fiber lemma]]

\linebreak

* [[finite homotopy type]]

* [[p-local homotopy type]]

* [[p-complete homotopy type]]



## References

* {#Hilton82} [[Peter Hilton]], _Nilpotency in group theory and topology_, Publicacions de la Secció de Matemàtiques Vol. 26, No. 3 (1982), pp. 47-78 ([jstor:43741908](https://www.jstor.org/stable/43741908))

* {#MayPonto12} [[Peter May]], [[Kate Ponto]], _More Concise Algebraic Topology_, University of Chicago Press (2012) ([pdf](https://www.math.uchicago.edu/~may/TEAK/KateBookFinal.pdf))

* {#Riehl14} [[Emily Riehl]], def. 14.4.9 in: _[[Categorical Homotopy Theory]]_, New Mathematical Monographs 24, Cambridge University Press 2014 ([pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf), [doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457))


See also 

* Wikipedia, _[Nilpotent space](https://en.wikipedia.org/wiki/Nilpotent_space)_

See also

* Wikipedia, _[Nilpotent space](https://en.wikipedia.org/wiki/Nilpotent_space)_


The [[rational homotopy theory]] of nilpotent topological spaces is discussed in

* {#BousfieldGugenheim76} [[Aldridge Bousfield]], V. K. A. M. Gugenheim, section 9.1 of _On PL deRham theory and rational homotopy type_ , Memoirs of the AMS, vol. 179 (1976)

* {#Neisendorfer78} [[Joseph Neisendorfer]], _Lie algebras, coalgebras and rational homotopy theory for nilpotent spaces_, Pacific J. Math. Volume 74, Number 2 (1978), 429-460. ([euclid](http://projecteuclid.org/euclid.pjm/1102810284))

Discussion in [[homotopy type theory]]:

* {#Scoccola19} Luis Scoccola, _Nilpotent Types and Fracture Squares in Homotopy Type Theory_ ([arXiv:1903.03245](https://arxiv.org/abs/1903.03245))






[[!redirects nilpotent topological spaces]]

[[!redirects nilpotent homotopy type]]
[[!redirects nilpotent homotopy types]]

[[!redirects nilpotent space]]
[[!redirects nilpotent spaces]]

[[!redirects nilpotent spectrum]]
[[!redirects nilpotent spectra]]
 
