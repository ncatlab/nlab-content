
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

[[Hochschild homology]] may be understood as the [[cohomology]] of [[free loop space object]]s (as described there). These free loop space objects are canonically equipped with a [[circle group]]-[[action]] that rotates the loops. _Cyclic homology_ is the corresponding $S^1$-[[equivariant cohomology]] of free loop space objects.

Like [[Hochschild homology]], [[cyclic homology]] is an _additive invariant_ of [[dg-categories]] or [[stable infinity-categories]], in the sense of [[noncommutative motives]].  It also admits a [[Dennis trace map]] from [[algebraic K-theory]], and has been successful in allowing computations of the latter.

There are several definitions for the cyclic homology of an [[associative algebra]] $A$ (over a [[commutative ring]] $k$).  [[Alain Connes]] originally defined cyclic homology over [[fields]] of [[characteristic zero]], as the [[homology]] groups of a cyclic variant of the [[chain complex]] computing [[Hochschild homology]].  [[Jean-Louis Loday]] and [[Daniel Quillen]] gave a definition via a certain [[double complex]] (for arbitrary commutative rings).  [[Alain Connes|Connes]] gave another definition by associating to $A$ a [[cyclic object|cyclic]] [[vector space]] $A^\sharp$, and showing that the cyclic homology of $A$ may be computed as via [[Ext]]-groups $Ext^*(A^\sharp, k^\sharp)$.  A fourth definition was given by [[Christian Kassel]], who showed that the cyclic homology groups may be computed as the homology groups of a certain [[mixed complex]] associated to $A$.

Following [[Alexandre Grothendieck]], [[Charles Weibel]] gave a definition of [[cyclic homology]] (and [[Hochschild homology]]) for [[schemes]], using [[hypercohomology]].  On the other hand, the definition of [[Christian Kassel]] via [[mixed complexes]] was extended by [[Bernhard Keller]] to [[linear categories]] and [[dg-categories]], and he showed that the cyclic homology of the [[dg-category]] of [[perfect complexes]] on a (nice) [[scheme]] $X$ coincides with the cyclic homology of $X$ in the sense of [[Charles Weibel|Weibel]].

There are closely related variants called [[periodic cyclic homology]] and [[negative cyclic homology]].  There is a version for [[ring spectra]] called [[topological cyclic homology]].

## Definition

### The chain complex for cyclic homology

Let $A$ be an [[associative algebra]] over a [[field]] $k$ of characteristic $0$. Write $C_\bullet(A,A)$ for the [[Hochschild homology]] [[chain complex]] of $A$ with coefficients in $A$.

For each $n \in \mathbb{N}$ let $\lambda : C_n(A,A) \to C_n(A,A)$ be the $k$-linear map that cyclically permutes the elements and introduces a sign:

$$
  \lambda : (a_0, a_1, \cdots, a_{n-1}, a_n)
  \mapsto 
   (-1)^n
   (a_n, a_0  , \cdots, a_{n-1})
  \,.
$$


+-- {: .un_defn}
###### Definition

The **cyclic homology complex** $C^\lambda_\bullet(A)$ of $A$ is the quotient of the Hochschild homology complex of $A$ by cyclic permutations:

$$
  C_\bullet^\lambda(A) := C_\bullet(A,A)/im(Id-\lambda)
  \,.
$$

The [[homology]] of the cyclic complex, denoted

$$
  HC_n(A) := H_n( C_\bullet^\lambda(A) )
$$

is called the **cyclic homology** of $A$.
=--

+-- {: .un_defn}
###### Definition

The **cyclic cohomology** groups of $A$ Are the [[cohomology]] groups of the dual [[cochain complex]], denoted $HC^n(A)$.
=--

+-- {: .un_defn}
###### Definition

If $I\subset A$ is an ideal, then the **relative cyclic homology** groups $HC_n(A,I)$ are the homology groups of the complex $C_\bullet(A,I) = ker(C_\bullet(A)\to C_\bullet(A/I))$.
=--

### Ordinary cohomology of $\mathcal{L}X/S^1$ and cyclic homology of $X$

Let $X$ be a [[simply connected topological space|simply connected]] [[topological space]]. 

The [[ordinary cohomology]] $H^\bullet$ of its free loop space is the [[Hochschild homology]] $HH_\bullet$ of its [[singular cohomology|singular chains]] $C^\bullet(X)$:

$$
  H^\bullet(\mathcal{L}X)
    \simeq
  HH_\bullet( C^\bullet(X) )
  \,.
$$

Moreover the $S^1$-equivariant cohomology of the loop space, hence the ordinary cohomology of the [[cyclic loop space]] $\mathcal{L}X/^h S^1$ is the [[cyclic homology]] $HC_\bullet$ of the singular chains:

$$
  H^\bullet(\mathcal{L}X/^h S^1)
    \simeq
  HC_\bullet( C^\bullet(X) )
$$

([Jones 87, Thm. A](#Jones87), review in [Loday 92, Cor. 7.3.14](#Loday92), [Loday 11, Sec 4](#Loday11))

If the [[coefficients]] are [[rational numbers|rational]], and $X$ is of [[finite type]] then this may be computed by the _[[Sullivan model for free loop spaces]]_, see there the section on _[Relation to Hochschild homology](Sullivan+model+of+free+loop+space#RelationToHochschildHomology)_.


In the special case that the [[topological space]] $X$ carries the structure of a [[smooth manifold]], then the singular cochains on $X$ are equivalent to the [[dgc-algebra]] of [[differential forms]] (the [[de Rham algebra]]) and hence in this case the statement becomes that 


$$
  H^\bullet(\mathcal{L}X)
    \simeq
  HH_\bullet( \Omega^\bullet(X) )
  \,.
$$

$$
  H^\bullet(\mathcal{L}X/^h S^1)
    \simeq
  HC_\bullet( \Omega^\bullet(X) )
  \,.
$$

This is known as _[[Jones' theorem]]_ ([Jones 87](#Jones87))

An [[(infinity,1)-category theory|infinity-category theoretic]] proof of this fact is indicated at _[Hochschild cohomology -- Jones' theorem](Hochschild+cohomology#JonesTheorem)_.


## Properties

### Loday-Quillen-Tsygan theorem

The _[[Loday-Quillen-Tsygan theorem]]_ ([Loday-Quillen 84](#LodayQuillen84), [Tsygan 83](#Tsygan83)) states that for any [[associative algebra]], $A$ in [[characteristic zero]], the [[Lie algebra homology]] $H_\bullet(\mathfrak{gl}(A))$  of the infinite [[general linear Lie algebra]] $\mathfrak{gl}(A)$ with [[coefficients]] in $A$ is, up to a degree shift, the [[exterior algebra]] $\wedge(HC_{\bullet - 1}(A))$ on the [[cyclic homology]] $HC_{\bullet - 1}(A)$ of $A$:

$$
  H_\bullet(\mathfrak{gl}(A))
  \;\simeq\;
  \wedge( HC_{\bullet - 1}(A) )
$$

(see e.g [Loday 07, theorem 1.1](#Loday07)).




## Related entries 

* [[cyclic category]]

* [[cyclic object]]

  [[cyclic set]] [[cyclic space]]

* [[cyclic loop space]]

* [[topological cyclic homology]]

* [[Hochschild homology]], [[topological Hochschild homology]]

* [[Sullivan model of free loop space]]

* [[dihedral homology]]


* [[Loday-Quillen-Tsygan theorem]]

* [[additive K-theory]]

## References

Foundational articles:

* [[A. Connes]], _Noncommutative differential geometry, Part I, the Chern character in $K$-homology_, Preprint, Inst. Hautes &#201;tudes Sci., Bures-sur-Yvette, 1982; _Part II, de Rham homology and noncommutative algebra_, Preprint, IH&#201;S 1983; _Cohomologie cyclique et foncteurs $Ext^n$_, C. R. Acad. Sci. Paris __296__, (1983), pp. 953&#8211;958, [MR86d:18007](http://www.ams.org/mathscinet-getitem?mr=777584)

* {#Connes83} [[Alain Connes]], _Cohomologie cyclique et foncteurs $Ext^n$_, C.R.A.S. **296** (1983), S&#233;rie I, 953-958 ([pdf](https://alainconnes.org/wp-content/uploads/n83.pdf), [[Connes_CohomologieCyclique.pdf:file]]).


* [[B. L. Tsygan]], _The homology of matrix Lie algebras over rings and the Hochschild homology_, Uspekhi Mat. Nauk, 38:2(230) (1983), 217&#8211;218.

* [[Jean-Louis Loday]], [[Daniel Quillen]], _Cyclic homology and the Lie algebra homology of matrices_, Comment. Math. Helvetici 59 (1984) 565-591 ([doi:10.1007/978-3-662-21739-9](https://link.springer.com/book/10.1007/978-3-662-21739-9))

* [[Christian Kassel]], _Cyclic homology, comodules and mixed complexes_, J. Alg. 107 (1987), 195&#8211;216 (<a href="https://doi.org/10.1016/0021-8693(87)90086-X">doi:10.1016/0021-8693(87)90086-X</a>)


Monographs:

* {#Loday98} [[Jean-Louis Loday]], _Cyclic homology_, Grundlehren Math.Wiss. __301__, Springer (1998)

* [[Alain Connes]], _Noncommutative geometry_, Acad. Press 1994, 661 p. [PDF](http://www.alainconnes.org/docs/book94bigpdf.pdf) 
* [[Max Karoubi]], _Homologie cyclique et K-th&#233;orie_, Ast&#233;rique __149__, Soci&#233;t&#233; Math&#233;matique de France (1987). 
* [[Ib Madsen]], _Algebraic K-theory and traces_, Current Developments in Mathematics, 1995.

Lecture notes: 

* {#Loday07} [[Jean-Louis Loday]], _Cyclic Homology Theory, Part II_, notes taken by Pawel Witkowsk (2007) ([pdf](https://www.impan.pl/swiat-matematyki/notatki-z-wyklado~/loday_cht_2.pdf))

* [[D. Kaledin]], _Tokyo lectures "Homological methods in non-commutative geometry"_, ([pdf](http://imperium.lenin.ru/~kaledin/tokyo/final.pdf), [TeX](http://imperium.lenin.ru/~kaledin/tokyo/final.tex)); and related but different [Seoul lectures](http://imperium.lenin.ru/~kaledin/seoul)

* [[Masoud Khalkhali]]: _A short survey of cyclic cohomology_, in *Quanta of Maths*, Clay Mathematics Proceedings, CMI/AMS (2010) 283-311 &lbrack;[arxiv/1008.1212](http://arxiv.org/abs/1008.1212), [pdf](https://www.claymath.org/library/proceedings/cmip011c.pdf)&rbrack;

Some modern treatments:

* [[Bernhard Keller]], _On the cyclic homology of ringed spaces and schemes_, Doc. Math. J. DMV 3 (1998), 231-259, [pdf](http://www.math.jussieu.fr/~keller/publ/KellerHCSchemes.pdf).

* [[Bernhard Keller]], _On the cyclic homology of exact categories_, Journal of Pure and Applied Algebra 136 (1999), 1-56, [pdf](http://www.math.jussieu.fr/~keller/publ/cyex.pdf).

* [[Bernhard Keller]], _Invariance and Localization for Cyclic Homology of DG algebras_, Journal of Pure and Applied Algebra, 123 (1998), 223-273, [pdf](http://www.math.jussieu.fr/~keller/publ/ilc.pdf).

* [[Charles Weibel]], _Cyclic homology for schemes_, Proceedings of the AMS, 124 (1996), 1655-1662, [web](http://www.math.uiuc.edu/K-theory/0043/).

* [[D. Kaledin]], _Cyclic homology with coefficients_, [math.KT/0702068](http://arxiv.org/abs/math.KT/0702068), to appear in Yu. Manin's 70th anniversary volume.

* [[E. Getzler]], [[M. Kapranov]], _Cyclic operads and cyclic homology_, in: "Geometry, Topology and Physics for R. Bott", 
ed. S.-T. Yau, p. 167-201, International Press, Cambridge MA, 1995, [pdf](http://www.math.northwestern.edu/~getzler/Papers/cyclic.pdf)

* [[Teimuraz Pirashvili]], [[Birgit Richter]], _Hochschild and cyclic homology via functor homology_, K-Theory __25__ (2002), no. 1, 39&#8211;49, [MR2003c:16011](http://www.ams.org/mathscinet-getitem?mr=1899698), [doi](http://dx.doi.org/10.1023/A:1015064621329)

* [[Jolanta Słomińska]], _Decompositions of the category of noncommutative sets and Hochschild and cyclic homology_, Cent. Eur. J. Math. __1__ (2003), no. 3, 327&#8211;331 ([doi:10.2478/BF02475213](http://dx.doi.org/10.2478/BF02475213), [MR2004f:16011](http://www.ams.org/mathscinet-getitem?mr=1992895))

Some influential original references from 1980s: 

* [[Boris Tsygan]], [[Boris Feigin]],  _[[Additive K-theory]]_, in LNM 1289 (1987), edited by Yu. I. Manin, pp. 67--209, seminar 1984-1986 in Moscow), [MR89a:18017](http://www.ams.org/mathscinet-getitem?mr=923136); 
_&#1040;&#1076;&#1076;&#1080;&#1090;&#1080;&#1074;&#1085;&#1072;&#1103; K-&#1090;&#1077;&#1086;&#1088;&#1080;&#1103; &#1080; &#1082;&#1088;&#1080;&#1089;&#1090;&#1072;&#1083;&#1100;&#1085;&#1099;&#1077; &#1082;&#1086;&#1075;&#1086;&#1084;&#1086;&#1083;&#1086;&#1075;&#1080;&#1080;_, &#1060;&#1091;&#1085;&#1082;&#1094;. &#1072;&#1085;&#1072;&#1083;&#1080;&#1079; &#1080; &#1077;&#1075;&#1086; &#1087;&#1088;&#1080;&#1083;., 19:2 (1985), 52&#8211;-62, [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=1358&what=fullt&option_lang=rus), [MR88e:18008](http://www.ams.org/mathscinet-getitem?mr=800920); Engl. transl. in B. L. Fe&#301;gin, B. L. Tsygan, _Additive $K$-theory and crystalline cohomology_, Functional Analysis and Its Applications, 1985, 19:2, 124&#8211;132.
* [[T. Goodwillie]], _Cyclic homology, derivations, and the free loopspace_, Topology __24__ (1985),
no. 2, 187&#8211;215, [MR87c:18009](http://www.ams.org/mathscinet-getitem?mr=793184), <a href="http://dx.doi.org/10.1016/0040-9383(85)90055-2">doi</a>

The relation to [[cyclic loop spaces]]:

* {#Jones87} [[John D.S. Jones]], _Cyclic homology and equivariant homology_, Invent. Math. __87__, 403-423 (1987) ([pdf](https://math.berkeley.edu/~nadler/jones.pdf), [doi:10.1007/BF01389424](https://doi.org/10.1007/BF01389424))

reviewed in:

* {#Loday92} [[Jean-Louis Loday]], *Cyclic Spaces and $S^1$-Equivariant Homology* ([doi:10.1007/978-3-662-21739-9_7](https://link.springer.com/chapter/10.1007/978-3-662-21739-9_7))

  Chapter 7 in: *Cyclic Homology*, Grundlehren **301**, Springer 1992 ([doi:10.1007/978-3-662-21739-9](https://link.springer.com/book/10.1007/978-3-662-21739-9))

* {#Loday11} [[Jean-Louis Loday]], Section 4 of: _Free loop space and homology_, Chapter 4 in: Janko Latchev, Alexandru Oancea (eds.): *Free Loop Spaces in Geometry and Topology*, IRMA Lectures in Mathematics and Theoretical Physics **24**, EMS 2015 ([arXiv:1110.0405](https://arxiv.org/abs/1110.0405), [ISBN:978-3-03719-153-8](https://bookstore.ams.org/emsilmtp-24/))


On the [[ordinary cohomology]] of [[cyclic loop spaces]] ("string cohomology") computed directly (instead of via the isomorphism to cyclic homology):

* {#BokstedtOttosen05} [[Marcel Bökstedt]], [[Iver Ottosen]], *A spectral sequence for string cohomology*, Topology Volume 44, Issue 6, November 2005, Pages 1181-1212 ([arXiv:math/0411571](https://arxiv.org/abs/math/0411571), [doi:10.1016/j.top.2005.04.006](https://doi.org/10.1016/j.top.2005.04.006))

and specifically for [[complex projective spaces]]:

* [[Marcel Bökstedt]], [[Iver Ottosen]], *String cohomology groups of complex projective spaces*, Algebr. Geom. Topol. 7(4): 2165-2238 (2007). ([arXiv:math/0605754](https://arxiv.org/abs/math/0605754), [doi:10.2140/agt.2007.7.2165](https://projecteuclid.org/journals/algebraic-and-geometric-topology/volume-7/issue-4/String-cohomology-groups-of-complex-projective-spaces/10.2140/agt.2007.7.2165.full))

On the cyclic homology of the [[groupoid convolution algebra]] of [[étale groupoid|étale]] [[Lie groupoids]], hence of [[orbifolds]]:

* [[Jean-Luc Brylinski]], [[Victor Nistor]], *Cyclic cohomology of étale groupoids*,  K-theory 8.4 (1994): 341-365 ([pdf](https://www.researchgate.net/profile/Victor-Nistor/publication/226520448_Cyclic_cohomology_of_etale_groupoids/links/5509d9d30cf20ed529e227b0/Cyclic-cohomology-of-etale-groupoids.pdf), [[BrylinskiNistor_CyclicCohomology.pdf:file]])


* [[Marius Crainic]], *Cyclic Cohomology of Étale Groupoids; The General Case*, K-Theory 17: 319–362, 1999 ([arXiv:funct-an/9712001](https://arxiv.org/abs/funct-an/9712001), [published pdf](https://access.portico.org/Portico/rest/au/getAUContent?auId=ark:/27927/pgg1zfpvw2x&fileName=pgg1zfprgx2.pdf&viewType=PDF))


The [[Loday-Quillen-Tsygan theorem]] is originally due, independently, to

* {#LodayQuillen84} [[Jean-Louis Loday]], [[Daniel Quillen]], _Cyclic homology and the Lie algebra homology of matrices_ Comment. Math. Helv., 59(4):569–591, 1984 ([doi:10.1007/BF02566367](https://doi.org/10.1007/BF02566367))

and

* {#Tsygan83} [[Boris Tsygan]], _Homology of matrix algebras over rings and the Hochschild homology_, Uspeki Math. Nauk., 38:217–218, 1983.




[[!redirects cyclic (co)homology]]
[[!redirects cyclic cohomology]]


[[!redirects string cohomology]]



