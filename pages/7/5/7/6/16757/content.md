
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

An _ADE singularity_ is an [[orbifold]] [[fixed point]] locally of the form $\mathbb{C}^2\sslash\Gamma$ with $\Gamma \hookrightarrow SU(2)$ a [[finite subgroup of SU(2)]] given by the [[ADE classification]] (and $SU(2)$ is understood with its defining linear [[action]] on the [[complex numbers|complex]] [[vector space]] $\mathbb{C}^2$).

## Properties

### Resolution by spheres touching along a Dynkin diagram
 {#ResolutionBySpheresTouchingAlongADynkinDiagram}

The [[blow-up]] of an ADE-singularity is given by a [[union]] of [[Riemann spheres]] that touch each other such as to form the shape of the [[Dynkin diagram]] whose A-D-E label corresponds to that of the given [[finite subgroup of SU(2)]].

This statement is originally due to ([duVal 1934 I, p. 1-3 (453-455)](#duVal1934I)). A description in terms of [[hyper-Kähler geometry]] is due to [Kronheimer 89a](#Kronheimer89a).

Quick survey of this fact is in [Reid 87](#Reid87), a textbook account is [Slodowy 80](#Slodowy80).

{#InStringTheory} In [[string theory]] this fact is interpreted in terms of [[gauge enhancement]] of the [[M-theory]]-lift of coincident [[black brane|black]] [[D6-branes]] to an  [[MK6]] at an ADE-singularity ([Sen 97](enhanced+gauge+symmetry#Sen97)):

\begin{center}
\begin{imagefromfile}
  "file_name": "ADESingularity.jpg",
  "width": 760
\end{imagefromfile}
\end{center}

> graphics grabbed from [HSS18](#HSS18)
 
See at _[[M-theory lift of gauge enhancement on D6-branes]]_ for more.

$\,$

[[!include ADE -- table]]


### From coincident KK-monopoles

[[!include KK-monopole geometries -- table]]


### Bridgeland stability conditions

For $G_{ADE} \subset SU(2)$ a [[finite subgroup of SU(2)]], 
let $\tilde X$ be the [[resolution of singularities|resolution]] of the corresponding ADE-singularity as [above](#ResolutionBySpheresTouchingAlongADynkinDiagram).

Then the [[connected component]] of the space of [[Bridgeland stability conditions]] on the bounded [[derived category]] of [[coherent sheaves]] over $\tilde X$ can be described explicitly ([Bridgeland 05](#Bridgeland05)). 

Specifically for type-A singularities the space of stability conditions is in fact [[connected topological space|connected]] and [[simply-connected topological space]] ([Ishii-Ueda-Uehara 10](#IshiiUedaUehara10)). 

Brief review is in [Bridgeland 09, section 6.3](#Bridgeland09).



## Related concepts

* [[singularity]]

* [[conical singularity]]

* [[quiver gauge theory]]

* [[M-theory on G2-manifolds]]

* [[D7-brane]]

## References

### General

Original articles include

* {#duVal1934I} [[Patrick du Val]], _On isolated singularities of surfaces which do not affect the conditions of adjunction. I_, Proceedings of the Cambridge Philosophical Society, 30 (4): 453–459  (1934a) ([doi:10.1017/S030500410001269X](https://doi.org/10.1017/S030500410001269X))

* {#duVal1934II} [[Patrick du Val]], _On isolated singularities of surfaces which do not affect the conditions of adjunction. II_, Proceedings of the Cambridge Philosophical Society, 30 (4): 460–465 (1934) ([doi:10.1017/S0305004100012706](https://doi.org/10.1017/S0305004100012706))

* {#duVal1934III} [[Patrick du Val]], _On isolated singularities of surfaces which do not affect the conditions of adjunction. III_, Proceedings of the Cambridge Philosophical Society, 30 (4): 483–491 (1934) ([doi:10.1017/S030500410001272X](https://doi.org/10.1017/S030500410001272X))

Textbook accounts include

* {#Durfee79} Alan H. Durfee, _Fifteen characterizations of rational double points and simple critical points_, L'Enseignement Mathématique Volume: 25 (1979) ([doi:10.5169/seals-50375](http://dx.doi.org/10.5169/seals-50375), [pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/durfee15.pdf))

* {#Slodowy80} [[Peter Slodowy]], _Simple singularities and simple algebraic groups_, in Lecture Notes in Mathematics 815, Springer, Berlin, 1980.

* {#Lamotke86} [[Klaus Lamotke]], chapter IV of _Regular Solids and Isolated Singularities_, Vieweg, Braunschweig, Wiesbaden 1986.


* {#Reid87} [[Miles Reid]], _Young persons guide to canonical singularities, in [[Spencer Bloch]] (ed.), _[Algebraic geometry -- Bowdoin 1985, Part 1](https://www.ams.org/books/pspum/046.1/)_, Proc. Sympos. Pure Math. 46 Part 1, Amer. Math. Soc., Providence, RI, 1987, pp. 345-414 ([pdf](http://www.maths.ed.ac.uk/cheltsov/quotient/pdf/reid3.pdf))

  (The last formula on page 409 has a typo: there should be no $r$ in the [[denominator]].)

Discussion of [[resolution of singularities|resolution]] of ADE-singularities in terms of [[hyper-Kähler geometry]]:

* {#Kronheimer89a} [[Peter Kronheimer]], _The construction of ALE spaces as hyper-K&#228;hler quotients_, J. Differential Geom. Volume 29, Number 3 (1989), 665-683. ([euclid:1214443066](https://projecteuclid.org/euclid.jdg/1214443066))

* {#Kronheimer89b} [[Peter Kronheimer]], _A Torelli-type theorem for gravitational instantons_, J. Differential Geom. Volume 29, Number 3 (1989), 685-697 ([euclid:1214443067](https://projecteuclid.org/euclid.jdg/1214443067))

and in terms of preprojective algebras:

* {#CBH98} William Crawley-Boevey, Martin P. Holland, _Noncommutative deformations of Kleinian singularities_, Duke Math. J. Volume 92, Number 3 (1998), 605-635 ([euclid:1077231679](https://projecteuclid.org/euclid.dmj/1077231679))

Reviews and lecture notes:

* _[Classification of singularities](http://www.mathematik.uni-kl.de/~zca/Reports_on_ca/29/paper_html/node10.html)_

* {#Burban} Igor Burban, _Du Val Singularities_ ([pdf](http://www.mi.uni-koeln.de/~burban/singul.pdf))

* [[Miles Reid]], _The Du Val Singularities $A_n$, $D_n$, $E_6$, $E_7$, $E_8$_ ([pdf](http://homepages.warwick.ac.uk/~masda/surf/more/DuVal.pdf))

* Anda Degeratu, _Crepant Resolutions of Calabi-Yau Orbifolds_, 2004 ([pdf](https://home.mathematik.uni-freiburg.de/degeratu/crepant.pdf))

* {#Siegel14} Kyler Siegel, section 6 of _The Ubiquity of the ADE classification in Nature_ , 2014 ([pdf](http://math.stanford.edu/~ksiegel/ADEClassifications.pdf))

* MathOverflow, _[Resolving ADE singularities by blowing up](http://mathoverflow.net/q/186368/381)_

On the [[Chen-Ruan cohomology|Chen-Ruan]] [[orbifold cohomology]] of ADE-singularities:

* [[Fabio Perroni]], *Orbifold Cohomology of ADE-singularities* ([arXiv:0510528](https://arxiv.org/abs/math/0510528))

* [[Fabio Perroni]], *Chen-Ruan cohomology of ADE-singularities*, International Journal of Mathematics, Vol. 18, No. 9 (2007) 1009-1059 ([arXiv:math/0605207](https://arxiv.org/abs/math/0605207), [doi:10.1142/S0129167X07004436](https://doi.org/10.1142/S0129167X07004436)) 



Families of examples of [[G2 manifolds|G2 orbifolds]] with ADE singularities are constructed in 

* {#Reidegeld15} [[Frank Reidegeld]], _$G_2$-orbifolds from K3 surfaces with ADE-singularities_ ([arXiv:1512.05114](http://arxiv.org/abs/1512.05114))

* [[Frank Reidegeld]], _$G_2$-orbifolds with ADE-singularities_ ([pdf](https://core.ac.uk/download/pdf/159317626.pdf))

[[Riemannian geometry]] of manifolds with ADE singularities is discussed in 

* Boris Botvinnik, [[Jonathan Rosenberg]], _Positive scalar curvature on manifolds with fibered singularities_ ([arXiv:1808.06007](https://arxiv.org/abs/1808.06007))

See also 

* Wikipedia, _[du Val singularity](https://en.wikipedia.org/wiki/Du_Val_singularity)_

### Via Bridgeland stability

Discussion of [[Bridgeland stability conditions]] for ([[resolution of singularities|resolutions of]]) ADE singularities includes:

* {#Bridgeland05} [[Tom Bridgeland]], _Stability conditions and Kleinian singularities_, International Mathematics Research Notices 2009.21 (2009): 4142-4157 ([arXiv:0508257](https://arxiv.org/abs/math/0508257))

* {#IshiiUedaUehara10} Akira Ishii, Kazushi Ueda, Hokuto Uehara, _Stability conditions on $A_n$-singularities_, Journal of Differential Geometry 84 (2010) 87-126 ([arXiv:math/0609551](https://arxiv.org/abs/math/0609551))

and specifically over [[Dynkin quivers]]

* {#Qiu15} [[Yu Qiu]], Def. 2.1 _Stability conditions and quantum dilogarithm identities for Dynkin quivers_, Adv. Math., 269 (2015), pp 220-264 ([arXiv:1111.1010](https://arxiv.org/abs/1111.1010))

* [[Tom Bridgeland]], [[Yu Qiu]], Tom Sutherland, _Stability conditions and the $A_2$ quiver_ ([arXiv:1406.2566](https://arxiv.org/abs/1406.2566))



### In string theory
  {#ReferencesInStringTheory}

Discussion of [[ADE-singularities]] in [[string theory]] on [[orbifolds]]:

#### M-theory on ADE-orbifolds reducing to D6-branes in type II

[[M-theory lift of gauge enhancement on D6-branes]]:

* {#Sen97} [[Ashoke Sen]], _A Note on Enhanced Gauge Symmetries in M- and String Theory_, JHEP 9709:001,1997 ([arXiv:hep-th/9707123](http://arxiv.org/abs/hep-th/9707123))

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], Section 6.3.3 of: _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012


#### Heterotic M-theory on ADE-orbifolds

[[heterotic M-theory on ADE-orbifolds]]: 

* {#Sen97} [[Ashoke Sen]], _A Note on Enhanced Gauge Symmetries in M- and String Theory_, JHEP 9709:001,1997 ([arXiv:hep-th/9707123](http://arxiv.org/abs/hep-th/9707123))

* {#FLO99} Michael Faux, [[Dieter Lüst]], [[Burt Ovrut]], _Intersecting Orbifold Planes and Local Anomaly Cancellation in M-Theory_, Nucl. Phys. B554: 437-483, 1999 ([arXiv:hep-th/9903028](https://arxiv.org/abs/hep-th/9903028))

* {#FLO00a} Michael Faux, [[Dieter Lüst]], [[Burt Ovrut]], _Local Anomaly Cancellation, M-Theory Orbifolds and Phase-Transitions_, Nucl. Phys. B589: 269-291, 2000 ([arXiv:hep-th/0005251](https://arxiv.org/abs/hep-th/0005251))

* {#FLO00b} Michael Faux, [[Dieter Lüst]], [[Burt Ovrut]], _An M-Theory Perspective on Heterotic K3 Orbifold Compactifications_, Int. J. Mod. Phys. A18:3273-3314, 2003 ([arXiv:hep-th/0010087](https://arxiv.org/abs/hep-th/0010087))

* {#FLO00c} Michael Faux, [[Dieter Lüst]], [[Burt Ovrut]], _Twisted Sectors and Chern-Simons Terms in M-Theory Orbifolds_, Int. J. Mod. Phys. A18: 2995-3014, 2003 ([arXiv:hep-th/0011031](https://arxiv.org/abs/hep-th/0011031))

* {#KSTY99} [[Vadim Kaplunovsky]], J. Sonnenschein, [[Stefan Theisen]], S. Yankielowicz, _On the Duality between Perturbative Heterotic Orbifolds and M-Theory on $T^4/Z_N$_, Nuclear Physics B Volume 590, Issues 1–2, 4 December 2000, Pages 123-160 Nuclear Physics B ([arXiv:hep-th/9912144](https://arxiv.org/abs/hep-th/9912144), <a href="https://doi.org/10.1016/S0550-3213(00)00460-0">doi:10.1016/S0550-3213(00)00460-0</a>)

* {#GKSTY02} E. Gorbatov, [[Vadim Kaplunovsky]], J. Sonnenschein, [[Stefan Theisen]], S. Yankielowicz, _On Heterotic Orbifolds, M Theory and Type I' Brane Engineering_, JHEP 0205:015, 2002 ([arXiv:hep-th/0108135](https://arxiv.org/abs/hep-th/0108135))

* {#HSS18} [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_, CMP (2019) ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987), [doi:10.1007/s00220-019-03442-3](http://link.springer.com/article/10.1007/s00220-019-03442-3))

#### Heterotic string theory on ADE-orbifolds

[[heterotic string theory]] on ADE-orbifolds:

* [[Paul Aspinwall]], [[David Morrison]], _Point-like Instantons on K3 Orbifolds_,  Nucl. Phys. B503 (1997) 533-564 ([arXiv:hep-th/9705104](https://arxiv.org/abs/hep-th/9705104))

* {#Witten99} [[Edward Witten]], _Heterotic String Conformal Field Theory And A-D-E Singularities_, JHEP 0002:025, 2000 ([arXiv:hep-th/9909229](https://arxiv.org/abs/hep-th/9909229))

#### Type $I'$-string theory on ADE-orbifolds

[[type I' string theory]] on ADE-orbifolds

* {#BergmanRodriguezGomez12} [[Oren Bergman]], Diego Rodriguez-Gomez, Section 3 of: _5d quivers and their $AdS_6$ duals_, JHEP07 (2012) 171 ([arxiv:1206.3503](https://arxiv.org/abs/1206.3503))

#### Type $I$-string theory on ADE-orbifolds

[[type I string theory]] on ADE-orbifolds

* [[Kenneth Intriligator]], _New String Theories in Six Dimensions via Branes at Orbifold Singularities_, Adv. Theor. Math. Phys.1:271-282, 1998 ([arXiv:hep-th/9708117](https://arxiv.org/abs/hep-th/9708117))


#### M-theory on $G_2$-orbifolds with ADE-singularities

[[M-theory on G2-manifolds]] $\,$ [with ADE-singularities](M-theory+on%20G2-manifolds#EnhancedGaugeGroups):

* {#Acharya98} [[Bobby Acharya]], _M theory, Joyce Orbifolds and Super Yang-Mills_, Adv. Theor. Math. Phys. 3 (1999) 227-248 ([arXiv:hep-th/9812205](http://arxiv.org/abs/hep-th/9812205))

* {#Acharya00} [[Bobby Acharya]], _On Realising $N=1$ Super Yang-Mills in M theory_ ([arXiv:hep-th/0011089](http://arxiv.org/abs/hep-th/0011089))

* {#AcharyaSpence00} [[Bobby Acharya]], B. Spence, _Flux, Supersymmetry and M theory on 7-manifolds_ ([arXiv:hep-th/0007213](http://arxiv.org/abs/hep-th/0007213))

* {#Acharya02} [[Bobby Acharya]], _M Theory, $G_2$-manifolds and Four Dimensional Physics_,  Classical and Quantum Gravity Volume 19 Number 22, 2002  ([pdf](http://users.ictp.it/~pub_off/lectures/lns013/Acharya/Acharya_Final.pdf))

* {#AtijayMaldacenaVafa00} [[Michael Atiyah]], [[Juan Maldacena]], [[Cumrun Vafa]], _An M-theory Flop as a Large N Duality_, J. Math. Phys.42:3209-3220, 2001 ([arXiv:hep-th/0011256](https://arxiv.org/abs/hep-th/0011256))

* {#BeasleyWitten02} [[Chris Beasley]], [[Edward Witten]], _A Note on Fluxes and Superpotentials in M-theory Compactifications on Manifolds of $G_2$ Holonomy_, JHEP 0207:046,2002 ([arXiv:hep-th/0203061](http://arxiv.org/abs/hep-th/0203061))

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]] _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

* {#Witten01} [[Edward Witten]], _Anomaly Cancellation On Manifolds Of $G_2$ Holonomy_ ([arXiv:hep-th/0108165](http://arxiv.org/abs/hep-th/0108165))

* {#AcharyaWitten01} [[Bobby Acharya]], [[Edward Witten]], _Chiral Fermions from Manifolds of $G_2$ Holonomy_ ([arXiv:hep-th/0109152](http://arxiv.org/abs/hep-th/0109152))

#### F-theory with ADE-singularities

[[F-theory]] with ADE-singularities

* [[Paul Aspinwall]], [[David Morrison]], _Point-like Instantons on K3 Orbifolds_,  Nucl. Phys. B503 (1997) 533-564 ([arXiv:hep-th/9705104](https://arxiv.org/abs/hep-th/9705104))





See also at _[[F-branes -- table]]_





[[!redirects ADE singularities]]

[[!redirects ADE-singularity]]
[[!redirects ADE-singularities]]

[[!redirects ADE orbifold]]
[[!redirects ADE orbifolds]]

[[!redirects ADE-orbifold]]
[[!redirects ADE-orbifolds]]

[[!redirects du Val singularity]]
[[!redirects du Val singularities]]

