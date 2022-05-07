
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What is called _KR-theory_ ([Atiyah 66](#Atiyah66)) is variant of [[topological K-theory]] on [[spaces]] equipped with a $\mathbb{Z}_2$-[[action]] (by [[homeomorphism]], hence equipped with one [[involution|involutive]] homeomorphism -- a "[[real space]]").

In terms of [[cocycle]] models, classes of KR-theory are represented by [[complex vector bundles]] over $X$ on which the involution on their base space lifts to an _anti-linear_ involution of the total space. Over manifolds with trivial involution these are precisely the [[complexification]] of [[real vector bundles]] and hence over such spaces $KR$-theory reduces to [[KO]]-[[cohomology theory|theory]]. Conversely, over two copies $X \cup X$ of $X$ equipped with the involution that interchanges the two, $KR$-theory reduces to [[KU]]-[[cohomology theory|theory]]. Finally over $X \times S^1$ with the involution the antipodal identification on the second ([[circle]]) factor , $KR$-theory reduces to the self-conjugate [[KSC-theory]] ([Anderson 64](#Anderson64)). So in general $KR$-theory interpolates between all these cases. For instance on $X \times S^1$ with the reflection-involution on the circle (the [[real space]] denoted $S^{1,1}$, the non-trivial $\mathbb{Z}_2$-[[representation sphere]]) it behaves like $KO$-theory at the two involution fixed points (the two [[O-planes]]) and like $KU$ in their complement (a model that makes this very explicit is given in [DMR 13, section 4](#DMR13)), schematically:

$$
  KR(S^{1,1}) = ( KO --- KU --- KO )
$$


More abstractly, complex conjugation of complex vector bundles induces on the [[complex K-theory]] [[spectrum]] [[KU]] an involutive [[automorphism]]. $KR$ is the corresponding $\mathbb{Z}_2$-[[equivariant spectrum]], and $KR$-theory the corresponding $\mathbb{Z}_2$-[[equivariant cohomology]] theory.  In particular, the [[homotopy fixed point]] of [[KU]] under this automorphism is [[KO]]

$$
  KO \simeq (KU)^{\mathbb{Z}/2}
$$

(e.g.[Karoubi 01](#Karoubi01), [Dugger 03, corollary 7.6](#Dugger03), [Hill-Hopkins-Ravenel, section 7.3](#HillHopkinsRavenel)) and this way where in complex K-theory one has [[KU]]-[[modules]] ([[∞-modules]]), so in KR-theory one has $KO$-modules.

KR is an example of a [[real-oriented cohomology theory]], together with for instance [[MR-theory]] and [[BPR-theory]].

+-- {: .num_remark}
###### Remark on terminology

An [[involution]] on a space by a [[homeomorphism]] (or [[diffeomorphism]]) as they appear in KR theory may be thought of as a "non-linear [[real structure]]", and therefore spaces equipped with such involutions are called "[[real spaces]]". Following this, $KR$-theory is usually pronounced "real K-theory". But **beware** that this terminology easily conflicts with or is confused with [[KO]]-theory. For disambiguation the latter might better be called "orthogonal K-theory". But on abstract grounds maybe $KR$-theory would best be just called $\mathbb{Z}_2$-equivariant complex K-theory.

=--

## Definition

### As the Grothendieck group of complex vector bundles with real structure

...([Atiyah 66](#Atiyah66))...

### As a genuine $\mathbb{Z}_2$-Spectrum

The following gives $KR$ as a [[genuine G-spectrum]] for $G = \mathbb{Z}_2$.

Using that every orthogonal representation of $\mathbb{Z}_2$ is contained in an $\mathbb{C}^n$ with its [[complex conjugation]] action, one can restrict attention to these. Write 

$$
  \mathbb{C}P^1 = S^{2,1} = S^{\mathbb{C}}
  \,.
$$

The reduced [[canonical line bundle]] over this (the [[Hopf fibration]]) is classified by a map

$$
  S^{2,1}= \mathbb{C}P^1 \to \mathbb{Z}\times BU
$$

to the [[classifying space]] for [[topological K-theory]]. The homotopy-associative  multiplication on this space then yields the structure map of a $\mathbb{Z}_2$-spectrum

$$
  S^{2,1} \wedge (\mathbb{Z} \times BU)\to \mathbb{Z}\times BU
  \,.
$$

This is in fact an [[Omega spectrum]], by equivariant complex [[Bott periodicity]] (for instance in [Dugger 03, p. 2-3](#Dugger03)).



## Properties

### Bigrading

As any genuine [[equivariant cohomology theory]] $KR$-theory is naturally graded over the [[representation ring]] $RO(\mathbb{Z}_2)$. Write $\mathbb{R}$ for the trivial 1-dimensional representation and $\mathbb{R}_-$ for that given by the sign involution. Then the general orthogonalrepresentation decomposes as a [[direct sum]]

$$
  V = \mathbb{R}^+\oplus \mathbb{R}_-^q
  \,.
$$

The corresponding [[representation sphere]] is

$$
  S^V = (some\; convention)
  \,.
$$

### As induced from the derived moduli stack of tori
 {#InducedFromModuliStackOfTori}

The relation between $KU$, $KO$ and $KR$ naturally arises in [[chromatic homotopy theory]] as follows.

Inside the [[moduli stack of formal group laws]] sits the _[[moduli stack of tori|moduli stack of one dimensional tori]]_ $\mathcal{M}_{\mathbb{G}_m}$ ([Lawson-Naumann 12, def. A.1, A.3](#LawsonNaumann12)). This is equivalent to the [[quotient stack]] of the point by the [[group of order 2]]

$$
  \mathcal{M}_{\mathbb{G}_m}\simeq \mathbf{B}\mathbb{Z}_2
$$

([Lawson-Naumann 12, prop. A.4](#LawsonNaumann12)). Here the $\mathbb{Z}_2$-action is the inversion involution on [[abelian groups]].

Using the [[Goerss-Hopkins-Miller theorem]] this stack carries an [[E-∞ ring]]-valued [[structure sheaf]] $\mathcal{O}^{top}$ ([Lawson-Naumann 12, theorem A.5](#LawsonNaumann12)); and by the above equivalence this is a single [[E-∞ ring]] equipped with a $\mathbb{Z}_2$-[[∞-action]]. This is [[KU]] with its involution induced by [[complex conjugation]], hence essentially is $KR$. 

Accordingly, the [[global sections]] of $\mathcal{O}^{top}$ over $\mathcal{M}_{\mathbb{G}_m}$ are the $\mathbb{Z}_2$-[[homotopy fixed points]] of this action, hence is $KO$. This is further amplified in ([Mathew 13, section 3](#Mathew13)) and ([Mathew, section 2](#Mathew)).

As suggested there and by the main ([Lawson-Naumann 12, theorem 1.2](#LawsonNaumann12)) this realizes (at least localized at $p = 2$) the inclusion $KO \to KU$ as the restriction of an analogous inclusion of [[tmf]] built as the global sections of the similarly derived [[moduli stack of elliptic curves]].



## Related concepts

* [[real-oriented cohomology theory]]

  * [[MR-theory]]

  * [[BPR-theory]]

* [[real algebraic K-theory]]

* [[orientifold]]

* [[KO-dimension]]

[[!include chromatic tower examples - table]]

[[!include string theory and cohomology theory -- table]]

[[!include moduli stack of curves -- table]]

## References

KR theory was introduced in

* {#Atiyah66} [[Michael Atiyah]], _K-theory and reality_, The Quarterly Journal of Mathematics. Oxford. Second Series 17 (1) (1966),: 367&#8211;386, ISSN 0033-5606, MR 0206940 ([doi:10.1093/qmath/17.1.367](https://doi.org/10.1093/qmath/17.1.367), [[AtiyahKReal.pdf:file]])

The version of $KSC$-theory was introduced in 

* {#Anderson64} D. W. Anderson, _The real K-theory of classifying spaces_ Proc. Nat. Acad. Sci. U. S. A., 51(4):634&#8211;636, 1964.

The dual concept of KR-homology was defined in

* [[Gennady Kasparov]], _The operator K-functor and extensions of $C^\ast$-algebras,_ Izv. Akad. Nauk. SSSR Ser. Mat. 44, 571-636 (1980).

Discussion in [[equivariant homotopy theory]]:

* Paolo Masulli, _Equivariant homotopy: $KR$-theory_, Master thesis (2011) ([pdf](http://www.math.ku.dk/~jg/students/masulli.msthesis.2011.pdf), [[MasulliKRTheory2011.pdf:file]])


Computations over [[compact Lie groups]] in the context of [[twisted ad-equivariant K-theory]]:

* [[Chi-Kwong Fok]], *The Real K-theory of compact Lie groups*, SIGMA 10 (2014), 022, ([arXiv:1308.3871](https://arxiv.org/abs/1308.3871), [doi:10.3842/SIGMA.2014.022](https://doi.org/10.3842/SIGMA.2014.022))

* [[Chi-Kwong Fok]], *Equivariant twisted Real K-theory of compact Lie groups*,   Journal of Geometry and Physics 124 (2018) 325-349 ([arXiv:1503.00957](https://arxiv.org/abs/1503.00957), [doi:10.1016/j.geomphys.2017.11.013](https://doi.org/10.1016/j.geomphys.2017.11.013))


Discussion in the general context of [[real oriented cohomology theory]] is in 

* {#Kriz01} Po Hu, [[Igor Kriz]], _Real-oriented homotopy theory and an analogue of the Adams-Novikov spectral sequence_, Topology 40 (2001) 317-399 ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/hukriz.pdf))


Further discussion includes

* [[Johan Dupont]], _Symplectic bundles and $KR$-theory_ (1967) ([pdf](http://www.mscand.dk/article.php?id=1908))

Reviews include

* Wikipedia, _[KR-theory](http://en.wikipedia.org/wiki/KR-theory)_



Remarks on homotopy-theoretic KR in the context of [[algebraic K-theory]] are in

* [[Vigleik Angeltveit]], [[Andrew Blumberg]], Teena Gerhardt, [[Michael Hill]], _Algebraic K-theory and equivariant homotopy theory_, 2012 ([pdf](http://www.birs.ca/workshops/2012/12w5116/report12w5116.pdf))

Discussion of [[equivariant K-theory|equivariant]] and [[twisted K-theory|twisted]] versions of KR-theory

* [[El-kaïoum M. Moutuou]], _Twistings of KR for Real groupoids_ ([arXiv:1110.6836](http://arxiv.org/abs/1110.6836))

* [[El-kaïoum M. Moutuou]], _Graded Brauer groups of a groupoid with involution_, J. Funct. Anal. 266 (2014), no.5 ([arXiv:1202.2057](https://arxiv.org/abs/1202.2057))

* {#Freed12} [[Daniel Freed]], _Lectures on twisted K-theory and orientifolds_, lectures at ESI Vienna, 2012 ([[FreedESI2012.pdf:file]])

* [[Daniel Freed]], [[Gregory Moore]], Section 7 of: _Twisted equivariant matter_,  Ann. Henri Poincaré (2013) 14: 1927 ([arXiv:1208.5055](https://arxiv.org/abs/1208.5055))

* {#Gomi17} [[Kiyonori Gomi]], _Freed-Moore K-theory_ ([arXiv:1705.09134](https://arxiv.org/abs/1705.09134), [spire:1601772](http://inspirehep.net/record/1601772))


This is with motivation from _[[orientifolds]]_, see the references given there for more. A long list of computations of twisted $KR$-classes on tori with applications to [[T-duality]] on [[orientifolds]]/[[O-planes]] is in

* {#Gukov00} [[Sergei Gukov]], _K-Theory, Reality, and Orientifolds_, Commun.Math.Phys. 210 (2000) 621-639 ([arXiv:hep-th/9901042](http://arxiv.org/abs/hep-th/9901042))

* {#DMR13} [[Charles Doran]], Stefan Mendez-Diez, [[Jonathan Rosenberg]], _T-duality For Orientifolds and Twisted KR-theory_ ([arXiv:1306.1779](http://arxiv.org/abs/1306.1779))

  (but see [HMSV 19, p.5 footnote 1](#HMSV19))

* {#DMR14} [[Charles Doran]], Stefan Mendez-Diez, [[Jonathan Rosenberg]], _String theory on elliptic curve orientifolds and KR-theory_ ([arXiv:1402.4885](http://arxiv.org/abs/1402.4885))

A general proposal for [[differential K-theory|differential]] [[equivariant K-theory|equivariant]] KR-theory of [[orientifolds]] and [[O-plane charge]]

* {#DistlerFreedMoore09} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))


Discussion of $KO$ as the $\mathbb{Z}_2$-[[homotopy fixed points]] of $KU$ (or $KR$) is in

* {#Karoubi01} [[Max Karoubi]], _A descent theorem in topological K-theory_, K-theory 24 (2001), no. 2, 109&#8211;114 ([arXiv:math/0509396](http://arxiv.org/abs/math/0509396))

* {#Dugger03} [[Daniel Dugger]], _An Atiyah-Hirzebruch spectral sequence for $KR$-theory_, Ktheory
35 (2005), 213&#8211;256. ([arXiv:0304099](http://arxiv.org/abs/math/0304099))

* {#HillHopkinsRavenel} [[Michael Hill]], [[Michael Hopkins]], [[Douglas Ravenel]], section 7.3 of _The Arf-Kervaire problem in algebraic topology: Sketch of the proof_ ([[HHRKervaire.pdf:file]])

Discussion of $KU$ with its $\mathbb{Z}_2$-action as the [[E-∞ ring]]-valued [[structure sheaf]] of the moduli stack of tori is due to 

* {#LawsonNaumann12} [[Tyler Lawson]], [[Niko Naumann]], appendix of _Strictly commutative realizations of diagrams over the Steenrod algebra and topological modular forms at the prime 2_ ([arXiv:1203.1696](http://arxiv.org/abs/1203.1696))

which is reviewed and amplified further in 

* {#Mathew13} [[Akhil Mathew]], section 3 of _The homology of $tmf$_ ([arXiv:1305.6100](http://arxiv.org/abs/1305.6100)) 

* {#Mathew} Akhil Mathew, section 2 of _The homotopy groups of $TMF$_, talk notes ([pdf](http://math.mit.edu/~sglasman/tmfhomotopy.pdf))

Discussion of [[twisted cohomology|twists]] of [[KR-theory]] by [[HZR-theory]] in degree 3 via [[bundle gerbes]] ([[Jandl gerbes]]) suitable for classifying [[D-brane charge]] on [[orientifolds]]:

* [[Pedram Hekmati]], [[Michael Murray]], [[Richard Szabo]], [[Raymond Vozzo]], _Real bundle gerbes, orientifolds and twisted KR-homology_ ([arXiv:1608.06466](http://arxiv.org/abs/1608.06466))

* {#HMSV19} [[Pedram Hekmati]], [[Michael Murray]], [[Richard Szabo]], [[Raymond Vozzo]], _Sign choices for orientifolds_, Commun. Math. Phys. 378, 1843–1873 (2020) ([arXiv:1905.06041](https://arxiv.org/abs/1905.06041))

[[!redirects KR-homology]]

[[!redirects KR-theory]]

[[!redirects KR]]

[[!redirects real K-theory]]
