
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents## 
* table of contents
{:toc}

## Idea

$MU$ is the universal [[Thom spectrum]] for [[complex vector bundles]]. It is the spectrum [[Brown representability theorem|representing]] _complex [[cobordism cohomology theory]]_. It is the complex analog of [[MO]]. 


[[MR cohomology theory]], or _real cobordism_, ([Landweber 68](#Landweber68), [Landweber 69](#Landweber69)) is the $\mathbb{Z}_2$-[[equivariant cohomology theory]] version of $MU$ [[complex cobordism cohomology theory]]. 

## The $M U$ spectrum 

The spectrum denoted $M U$
is, as a [[sequential spectrum]], in degree $2 n$ given by the [[Thom space]] of the underlying real vector bundle of the complex [[universal vector bundle]]:  the [[vector bundle]] that is  [[associated bundle|associated]] by the defining [[representation]] of the [[unitary group]] $U(n)$ on $\mathbb{C}^n$ to the $U(n)$-[[universal principal bundle]]:

$$
  M U(2n) = Thom
  \left(
    standard\;associated\;bundle\;to\;universal\;bundle
    \array{
      E U(n) \\ \downarrow \\ B U(n)
    }
  \right)
$$

A priori this yields a  [sequential S2-spectrum](Introduction+to+Stable+homotopy+theory+--+1#SequentialTSpectra), which is then turned into a sequential $S^1$-spectrum by taking the component spaces in odd degree to be the [[smash product]] of the [[circle]] $S^1$ with those in even degree.


This represents a [[complex oriented cohomology theory]] and indeed the universal one among these, see at _[[universal complex orientation on MU]]_.

The _periodic_ complex cobordism theory is given by adding up all the even degree powers of this theory:

$$
  M P = \vee_{n \in \mathbb{Z}} \Sigma^{2 n} M U
$$


The [[cohomology ring]] $M P({*})$ is the [[Lazard ring]] which is the universal coefficient ring for [[formal group laws]], see at _[[Milnor-Quillen theorem on MU]]_ .

The [[periodic cohomology theory|periodic]] version is sometimes written $PMU$.



## Properties

### Homotopy groups: Cobordism and Lazard ring
  {#HomotopyGroups}

The [[graded ring]] given by evaluating complex cobordism theory on the point is both the complex [[cobordism ring]] as well as the [[Lazard ring]] classifying [[formal group laws]].

+-- {: .num_theorem #RelationToCobordismRing}
###### Theorem

Evaluation of $MU$ on the point yields the complex [[cobordism ring]], whose underlying group is

$$
  \pi_\ast MU \simeq MU_\ast(pt) \simeq \mathbb{Z}[x_1, x_2, \cdots]
  \,,
$$

where the generator $x_i$ is in degree $2 i$.

=--

This is due to ([Milnor 60](#Milnor60), [Novikov 60](#Novikov60), [Novikov 62](#Novikov62)). A review is in ([Ravenel theorem 1.2.18](#Ravenel), [Ravenel, ch. 3, theorem 3.1.5](#Ravenel)).


The [[formal group law]] associated with $MU$ as with any [[complex oriented cohomology theory]] is classified by a [[ring]] [[homomorphism]] $L \longrightarrow \pi_\bullet(MU)$ out of the [[Lazard ring]].

+-- {: .num_theorem}
###### Theorem

This canonical [[homomorphism]] is an [[isomorphism]]

$$
  L \stackrel{\simeq}{\longrightarrow} \pi_\bullet(MU)
$$

between the [[Lazard ring]] and the $MU$-[[cohomology ring]], hence by theorem \ref{RelationToCobordismRing} with the complex [[cobordism ring]].

=--

This is [[Quillen's theorem on MU]].
(e.g [Lurie 10, lect. 7, theorem 1](#LurieLect7))


### Universal complex orientation on $M U$
 {#UniversalComplexOrientation}

There is a canonical [[complex oriented cohomology theory|complex orientation]] on $MU$ obtained from the map

$$
  \omega : \mathbb{C}P^\infty \stackrel{\simeq}{\to}
  M U(1)
  \;\;\;\;
  M U(\mathbb{C}P^\infty)
$$


For $E$ an [[E-infinity ring]] there is a [[bijection]] between [[complex oriented cohomology theory|complex orientation]] of $E$ and [[E-infinity ring]] maps of the form

$$
  MU \longrightarrow E
  \,.
$$

(e.g [Lurie 10, lect. 6, theorem 8](#LurieLect6), [Ravenel, chapter 4, lemma 4.1.13](#Ravenel))

See also at _[[complex orientation and MU]]_.


### $MU$-homology of a manifold: bordisms in $X$

For $X$ a [[manifold]] or a [[topological space]], the $MU$-homology [[group]] $MU_\ast(X)$ of its underlying [[homotopy type]] is the group of equivalence classes of maps $\Sigma \to X$ from manifolds $\Sigma$ with [[complex structure]] on the stable [[normal bundle]], modulo suitable complex [[cobordisms]].

See [Ravenel chapter 1, section 2](#Ravenel).

For more information, see the article [[bordism homology theory]],
which treats the oriented case; the case of (stable almost) complex structure is similar.

### $MU$-cohomology of a manifold: cobordisms in $X$

$MU$-cohomology groups of a manifold $M$ can be expressed
in terms of bordisms given by proper [complex-oriented maps](cobordism+cohomology+theory#ComplexOrientedMaps) into $M$.

For more information, see the article _[[cobordism cohomology theory]]_.

### $MU$-homology of $MU$: Hopf algebroid structure on dual Steenrod algebra

Moreover, the dual $MU$-[[Steenrod algebra]] $MU_\bullet(MU)$
forms a [[commutative Hopf algebroid]] over the [[Lazard ring]]. 
This is the content of the _[[Landweber-Novikov theorem]]_.



### Nilpotence theorem

* [[nilpotence theorem]]

### Snaith's theorem

[[Snaith's theorem]] asserts that the [[periodic complex cobordism spectrum]] is the [[∞-group ∞-ring]] of the [[classifying space]] for stable [[complex vector bundles]] (the classifying space for [[topological K-theory]]) localized at the [[Bott element]] $\beta$:

$$
  PMU \simeq \mathbb{S}[B U][\beta^{-1}]
  \,.
$$

### $p$-Localization and Brown-Peterson spectrum

The [[p-localization]] of $MU$ decomposes into the 
[[Brown-Peterson spectra]].

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]



## References

### General

* {#Novikov62} [[Sergei Novikov]], _Homotopy properties of Thom complexes_, Mat. Sbornik 57 (1962), no. 4, 407–442, 407&#8211;442 ([pdf](http://www.mi-ras.ru/~snovikov/6.pdf), [[NovikovThomComplexes.pdf:file]])

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Section 12 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

* {#Stong68} [[Robert Stong]], Chapter VII of: _Notes on Cobordism theory_, Princeton University Press, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [ISBN:9780691649016](http://press.princeton.edu/titles/6465.html), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/stongcob.pdf))

* {#ConnerSmith69} [[Pierre Conner]], [[Larry Smith]], _On the complex bordism of finite complexes_, Publications Mathématiques de l'IHÉS, Tome 37 (1969) , pp. 117-221 ([numdam:PMIHES_1969__37__117_0](http://www.numdam.org/item/?id=PMIHES_1969__37__117_0))

* [[Larry Smith]], _On Realizing Complex Bordism Modules: Applications to the Stable Homotopy of Spheres_, American Journal of Mathematics Vol. 92, No. 4 (Oct., 1970), pp. 793-856 ([doi:10.2307/2373397](https://doi.org/10.2307/2373397))


* {#Landweber70} [[Peter Landweber]], _On the complex bordism and cobordism of infinite complexes_, Bull. Amer. Math. Soc. Volume 76, Number 3 (1970) ([Euclid](http://projecteuclid.org/euclid.bams/1183531832)) 

* {#Adams74} [[Frank Adams]], _Stable homotopy theory and generalized homology_, Chicago lectures in mathematics, 1974

* {#Ravenel} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986

* [[Stanley Kochman]], Section 4.4 of: _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, Fields Institute Monographs, American Mathematical Society, 1996 ([cds:2264210](https://cdsweb.cern.ch/record/2264210))

* {#EKMM97} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May]], section VIII of _[[Rings, modules and algebras in stable homotopy theory]]_ 1997 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/EKMM.pdf))

* {#Hopkins99} [[Mike Hopkins]], section 4 of _Complex oriented cohomology theories and the language of stacks_, course notes 1999 ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/coctalos.pdf))

* [[Dai Tamaki]], [[Akira Kono]], Section 3.7 and Chapter 6 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ Lecture series ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html)), Lecture 5 _Complex bordism_ 
([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture5.pdf))

* {#LurieLect6} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ Lecture series ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html)) Lecture 6 _MU and complex orientations_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture6.pdf)) 
  

* {#LurieLect7} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_ Lecture series ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html)),  Lecture 7 _The homology of MU_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture7.pdf))
 

* [[Manifold Atlas]], _[Complex bordism](http://www.map.mpim-bonn.mpg.de/Complex_bordism)_


* [[Neil Strickland]], _Products on $MU$-modules_ ([pdf](http://hopf.math.purdue.edu/Strickland/mult.pdf))

* [[Jesse McKeown]], _Complex Cobordism vs. Representing Formal Group Laws_ ([arXiv:1605.09252](http://arxiv.org/abs/1605.09252))


For general discussion of equivariant complex oriented cohomology see at _[equivariant cohomology -- References -- Complex oriented cohomology](equivariant+cohomology#InComplexOrientedGeneralizedCohomologyTheory)_

On the [[Chern-Dold character]] on complex cobordism:

* {#Buchstaber70} [[Victor Buchstaber]], _The Chern–Dold character in cobordisms. I_, 

  Russian original: Mat. Sb. (N.S.), 1970 Volume 83(125), Number 4(12), Pages 575–595 ([mathnet:3530](http://m.mathnet.ru/php/archive.phtml?wshow=paper&jrnid=sm&paperid=3530&option_lang=eng))

  English translation: Mathematics of the USSR-Sbornik, Volume 12, Number 4, AMS 1970 ([doi:10.1070/SM1970v012n04ABEH000939](https://iopscience.iop.org/article/10.1070/SM1970v012n04ABEH000939))

* [[Victor Buchstaber]], A. P. Veselov, _Chern-Dold character in complex cobordisms and abelian varieties_ ([arXiv:2007.05782](https://arxiv.org/abs/2007.05782))



### Relation to CFT

A relation to [[2d CFT]] over [[Spec(Z)]] was suggested in

* Toshiyuki Katsura, Yuji Shimizu, [[Kenji Ueno]], _Complex cobordism ring and conformal field theory over $\mathbb{Z}$_, Mathematische Annalen
March 1991, Volume 291, Issue 1, pp 551-571 ([journal](http://link.springer.com/article/10.1007%2FBF01445226))

### Relation to divisors

Relation of [[complex cobordism cohomology]] with [[divisors]], [[algebraic cycles]] and [[Chow groups]]:

* [[Burt Totaro]], _Torsion algebraic cycles and complex cobordism_, J. Amer. Math. Soc. 10 (1997), 467-493 ([doi:10.1090/S0894-0347-97-00232-4](https://doi.org/10.1090/S0894-0347-97-00232-4))

* [MO discussion](https://mathoverflow.net/a/272131/381)


[[!redirects MU-theory]]


[[!redirects complex cobordism spectrum]]

[[!redirects complex bordism ring]]
[[!redirects complex bordism rings]]

[[!redirects complex cobordism ring]]
[[!redirects complex cobordism rings]]

[[!redirects complex cobordism cohomology theory]]
[[!redirects complex cobordism]]

[[!redirects complex bordism]]

[[!redirects complex bordism ring]]
[[!redirects complex bordism rings]]

[[!redirects complex cobordism ring]]
[[!redirects complex cobordism rings]]


[[!redirects complex cobordism cohomology]]
[[!redirects complex cobordism cohomology theory]]

[[!redirects complex cobordism theory]]

[[!redirects U-bordism]]
[[!redirects U-bordisms]]

[[!redirects U-bordism ring]]
[[!redirects U-bordism rings]]

[[!redirects U-bordism theory]]
[[!redirects U-bordism theories]]



