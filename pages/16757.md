
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

<img src="http://ncatlab.org/nlab/files/ADESingularity.jpg" width="760" alt="ADE 2Cycle" />

> graphics grabbed from [HSS18](http://ncatlab.org/schreiber/show/Equivariant+homotopy+and+super+M-branes)
 
See at _[[M-theory lift of gauge enhancement on D6-branes]]_ for more.

$\,$

[[!include ADE -- table]]

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

* {#duVal1934I} [[Patrick du Val]],  (1934a), "On isolated singularities of surfaces which do not affect the conditions of adjunction. I", Proceedings of the Cambridge Philosophical Society, 30 (4): 453–459, [doi:10.1017/S030500410001269X](https://doi.org/10.1017/S030500410001269X) 

* {#duVal1934II} [[Patrick du Val]],  (1934b), "On isolated singularities of surfaces which do not affect the conditions of adjunction. II", Proceedings of the Cambridge Philosophical Society, 30 (4): 460–465, [doi:10.1017/S0305004100012706](https://doi.org/10.1017/S0305004100012706)

* {#duVal1934III} [[Patrick du Val]],  (1934c), "On isolated singularities of surfaces which do not affect the conditions of adjunction. III", Proceedings of the Cambridge Philosophical Society, 30 (4): 483–491, [doi:10.1017/S030500410001272X](https://doi.org/10.1017/S030500410001272X)

Textbook accounts include

* {#Durfee79} Alan H. Durfee, _Fifteen characterizations of rational double points and simple critical points_, L'Enseignement Mathématique Volume: 25 (1979) ([doi:10.5169/seals-50375](http://dx.doi.org/10.5169/seals-50375), [pdf](http://www.maths.ed.ac.uk/~v1ranick/papers/durfee15.pdf))

* {#Slodowy80} [[Peter Slodowy]], _Simple singularities and simple algebraic groups_, in Lecture Notes in Mathematics 815, Springer, Berlin, 1980.

* {#Lamotke86} [[Klaus Lamotke]], chapter IV of _Regular Solids and Isolated Singularities_, Vieweg, Braunschweig, Wiesbaden 1986.


* {#Reid87} [[Miles Reid]], _Young persons guide to canonical singularities, in [[Spencer Bloch]] (ed.), _[Algebraic geometry -- Bowdoin 1985, Part 1](https://www.ams.org/books/pspum/046.1/)_, Proc. Sympos. Pure Math. 46 Part 1, Amer. Math. Soc., Providence, RI, 1987, pp. 345-414 ([pdf](http://www.maths.ed.ac.uk/cheltsov/quotient/pdf/reid3.pdf))

  (The last formula on page 409 has a typo: there should be no $r$ in the [[denominator]].)

Discussion in terms of [[hyper-Kähler geometry]]:

* {#Kronheimer89a} [[Peter Kronheimer]], _The construction of ALE spaces as hyper-K&#228;hler quotients_, J. Differential Geom. Volume 29, Number 3 (1989), 665-683. ([euclid:1214443066](https://projecteuclid.org/euclid.jdg/1214443066))

* {#Kronheimer89b} [[Peter Kronheimer]], _A Torelli-type theorem for gravitational instantons_, J. Differential Geom. Volume 29, Number 3 (1989), 685-697 ([euclid:1214443067](https://projecteuclid.org/euclid.jdg/1214443067))

Reviews and lecture notes include

* _[Classification of singularities](http://www.mathematik.uni-kl.de/~zca/Reports_on_ca/29/paper_html/node10.html)_

* {#Burban} Igor Burban, _Du Val Singularities_ ([pdf](http://www.mi.uni-koeln.de/~burban/singul.pdf))

* [[Miles Reid]], _The Du Val Singularities $A_n$, $D_n$, $E_6$, $E_7$, $E_8$_ ([pdf](http://homepages.warwick.ac.uk/~masda/surf/more/DuVal.pdf))

* Anda Degeratu, _Crepant Resolutions of Calabi-Yau Orbifolds_, 2004 ([pdf](https://home.mathematik.uni-freiburg.de/degeratu/crepant.pdf))

* Fabio Perroni, _Orbifold Cohomology of ADE-singularities_ ([pdf](http://mathweb.uzh.ch/fileadmin/math/preprints/10-06.pdf))

* {#Siegel14} Kyler Siegel, section 6 of _The Ubiquity of the ADE classification in Nature_ , 2014 ([pdf](http://math.stanford.edu/~ksiegel/ADEClassifications.pdf))

* MathOverflow, _[Resolving ADE singularities by blowing up](http://mathoverflow.net/q/186368/381)_

Families of examples of [[G2 manifolds|G2 orbifolds]] with ADE singularities are constructed in 

* {#Reidegeld15} [[Frank Reidegeld]], _$G_2$-orbifolds from K3 surfaces with ADE-singularities_ ([arXiv:1512.05114](http://arxiv.org/abs/1512.05114))

[[Riemannian geometry]] of manifolds with ADE singularities is discussed in 

* Boris Botvinnik, [[Jonathan Rosenberg]], _Positive scalar curvature on manifolds with fibered singularities_ ([arXiv:1808.06007](https://arxiv.org/abs/1808.06007))

See also 

* Wikipedia, _[du Val singularity](https://en.wikipedia.org/wiki/Du_Val_singularity)_


### In the context of string theory and stability conditions

Discussion in [[string theory]]:

* {#Sen97} [[Ashoke Sen]], _A Note on Enhanced Gauge Symmetries in M- and String Theory_, JHEP 9709:001,1997 ([arXiv:hep-th/9707123](http://arxiv.org/abs/hep-th/9707123))

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 6.3.3 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

For more seet at _[[M-theory on G2-manifolds]]_ the section [Orbifold singularities](M-theory+on%20G2-manifolds#EnhancedGaugeGroups)

See also at _[[F-branes -- table]]_

Discussion of [[Bridgeland stability conditions]] for ([[resolution of singularities|resolutions of]]) ADE singularities includes:

* {#Bridgeland05} [[Tom Bridgeland]], _Stability conditions and Kleinian singularities_, International Mathematics Research Notices 2009.21 (2009): 4142-4157 ([arXiv:0508257](https://arxiv.org/abs/math/0508257))

* {#IshiiUedaUehara10} Akira Ishii, Kazushi Ueda, Hokuto Uehara, _Stability conditions on $A_n$-singularities_, Journal of Differential Geometry 84 (2010) 87-126 ([arXiv:math/0609551](https://arxiv.org/abs/math/0609551))

and specifically over [[Dynkin quivers]]

* {#Qiu15} [[Yu Qiu]], Def. 2.1 _Stability conditions and quantum dilogarithm identities for Dynkin quivers_, Adv. Math., 269 (2015), pp 220-264 ([arXiv:1111.1010](https://arxiv.org/abs/1111.1010))

* [[Tom Bridgeland]], [[Yu Qiu]], Tom Sutherland, _Stability conditions and the $A_2$ quiver_ ([arXiv:1406.2566](https://arxiv.org/abs/1406.2566))





[[!redirects ADE singularities]]

[[!redirects ADE-singularity]]
[[!redirects ADE-singularities]]

[[!redirects ADE orbifold]]
[[!redirects ADE orbifolds]]

[[!redirects ADE-orbifold]]
[[!redirects ADE-orbifolds]]

[[!redirects du Val singularity]]
[[!redirects du Val singularities]]

