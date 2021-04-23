
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Rigid analytic geometry_ (often just "rigid geometry" for short) is a form of [[analytic geometry]] over a [[nonarchimedean field]] $K$ which considers [[spaces]] glued from [[polydiscs]], hence from [[maximal spectra]] of [[Tate algebras]] (quotients of a $K$-algebra of [[convergence|converging]] [[power series]]). This is in contrast to some modern approaches to [[non-Archimedean analytic geometry]] such as [[Berkovich spaces]] which are glued from Berkovich's [[analytic spectra]] and more recent Huber's [[adic spaces]].

The issue is that while the [[p-adic numbers]] are [[complete topological space|complete]] in the [[p-adic norm]], that [[topology]] is exotic: $\mathbb{Q}_p$ is a [[Stone space]], hence in particular a [[totally disconnected topological space]].

For that reason the naive idea of formulating [[p-adic geometry|p-adic]] analytic geometry in analogy to [[complex analytic geometry]] as modeled on domains in $\mathbb{Q}_p^n$, regarded with their [[subspace topology]], fails, as also all these domains are totally disconnected.

Instead there is ([Tate 71](#Tate71)) a suitable [[Grothendieck topology]] on such [[affinoid domains]] -- the _[[G-topology]]_ -- with respect to which there is a good theory of [[non-archimedean analytic geometry]] ("[[rigid analytic geometry]]") and hence in particular of [[p-adic geometry]]. Moreover, one may sensibly assign to a $p$-adic domain a [[topological space]] which _is_ well behaved (in particular locally connected and even locally contractible), this is the _[[analytic spectrum]]_ construction. The resulting topological spaces equipped with covers by [[affinoid domain]] under the [[analytic spectrum]] are called [[Berkovich spaces]].


According to [Kedlaya, p. 18](#Kedlaya), the terminology "rigid" is because...

> ... one develops everything "rigidly" by imitating the theory of [[schemes]] in [[algebraic geometry]], but using rings of [[convergence|convergent]] [[power series]] instead of [[polynomials]].

See also _[[global analytic geometry]]_. 

## Cohomology

The related type of cohomology is called [[rigid cohomology]].

## Applications

* The solution by Raynaud and Harbater of Abyhankar's conjecture concerning fundamental groups of curves in positive characteristic uses the rigid analytic
GAGA theorems (whose proofs are very similar to Serre's proofs in the
complex-analytic case). 


* Work of Kisin on modularity of Galois representations makes creative use of rigid-analytic spaces associated to [[Galois deformation rings]].

## Related concepts

* [[complex analytic space]]

* [[analytification]]

* [[global analytic geometry]]

* [[overconvergent global analytic geometry]]

## References

An original article is

* {#Tate71} [[John Tate]], _Rigid analytic spaces_, Invent. Math. __12__:257&#8211;289, 1971.

and for the construction of the generic fiber of formal schemes over the ring of integers of $K$

* Michel Raynaud, _G&#233;om&#233;trie analytique rigide d'apr&#232;s Tate, Kiehl,&#8943;_, Table Ronde d'Analyse non archim&#233;dienne (Paris, 1972), pp. 319&#8211;327. Bull. Soc. Math. France, Mem. No. 39&#8211;40, Soc. Math. France, Paris, 1974, [MR470254](http://www.ams.org/mathscinet-getitem?mr=470254)

Introductions are in 

* Johannes Nicaise, _Formal and rigid geometry: an intuitive introduction, and some applications_ ([pdf](http://gc83.perso.sfr.fr/GTIM/PDF%20GROUPE%20DE%20TRAVAIL/Nicaise/formal%20rigid%20Nicaise.pdf))

* [[Brian Conrad]], _Several approaches to non-Archimedean geometry_, [pdf](http://math.stanford.edu/~conrad/papers/aws.pdf)
* Peter Schneider, _Basic notions of rigid analytic geometry_, in: Galois representations in arithmetic algebraic geometry (Durham, 1996), 369&#8211;378, London Math. Soc. Lecture Note Ser. __254__, Cambridge Univ. Press 1998, [doi](http://dx.doi.org/10.1017/CBO9780511662010.010)

A comprehensive textbook account is in 

* {#BoschGuntzerRemmert84} S. Bosch, U. G&#252;ntzer, [[Reinhold Remmert]], _[[Non-Archimedean Analysis]] -- A systematic approach to rigid analytic geometry_, Grundlehren der Mathem. Wissen. __261__, Springer 1984 ([MR0746961](http://www.ams.org/mathscinet-getitem?mr=0746961), [pdf](http://math.arizona.edu/~cais/scans/BGR-Non_Archimedean_Analysis.pdf))



Comparison of various spectra and topologies is in

* M. van der Put, P. Schneider, _Points and topologies in rigid geometry_, Math. Ann. 302 (1995), no. 1, 81&#8211;103, [MR96k:32070](http://www.ams.org/mathscinet-getitem?mr=1329448), [doi](http://dx.doi.org/10.1007/BF01444488)

Other accounts include

* Ahmed Abbes, _&#201;l&#233;ments de G&#233;om&#233;trie Rigide_, vol. I. _Construction et &#233;tude g&#233;om&#233;trique des espaces rigides_, Progress in Mathematics __286__, Birkh&#228;user 2011, 496 p.[book page](http://perso.univ-rennes1.fr/ahmed.abbes/egr.html)

* Siegfried Bosch, _Lectures on formal and rigid geometry_, Preprints of SFB Geom. Struk. Math. Heft 378, [pdf](http://wwwmath.uni-muenster.de/sfb/about/publ/heft378.pdf) (revised 2008)
* J. Fresnel, M. van der Put, _Rigid geometry and applications_, Birkh&#228;user (2004) [MR2014891](http://www.ams.org/mathscinet-getitem?mr=2014891)
* F. Denef, L. van den Dries, _$p$-adic and real subanalytic sets_, Ann. of Math. __128__ (1988) no. 1, 79&#8211;138 [MR951508](http://www.ams.org/mathscinet-getitem?mr=951508), [doi](http://dx.doi.org/10.2307/1971463)
* [[Yan Soibelman]], _On non-commutative analytic spaces over non-archimedean fields_, preprint IHES, [pdf](http://www.math.ksu.edu/~soibel/lapkin-spaces-2.ps)
* Hans Grauert, Reinhold Remmert, _Coherent analytic sheaves_, Springer 1984
* [[R. Cluckers]], L. Lipshitz, _Fields with analytic structure_, J. Eur. Math. Soc. __13__, 1147&#8211;1223, [pdf](http://wis.kuleuven.be/algebra/Raf/prints/JEMS.pdf)
and several articles (in various formalisms) in collection
* R. Cluckers, J. Nicaise, J. Sebag (Editors), _Motivic integration and its interactions with [[model theory]] and non-archimedean Geometry_, 2 vols.
London Mathematical Society Lecture Note Series __383__, __384__ 
* Peter Schneider, _Points of rigid analytic varieties_, J. Reine Angew. Math. 434 (1993), 127&#8211;157, [MR94b:14017](http://www.ams.org/mathscinet-getitem?mr=1195693), [doi](http://dx.doi.org/10.1515/crll.1993.434.127)

See also 

* [[Kiran Kedlaya]], _$p$-Adic differential equations_ ([pdf](http://www-math.mit.edu/~kedlaya/18.787/compiled.pdf))
  {#Kedlaya}

category: geometry

[[!redirects rigid analytic geometries]]

[[!redirects rigid analytic space]]
[[!redirects rigid analytic spaces]]


[[!redirects rigid geometry]]
[[!redirects rigid geometries]]
