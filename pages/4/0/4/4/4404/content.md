
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _exotic smooth structure_ is, roughly speaking, a [[smooth structure]] on a [[topological manifold]] $X$ which makes the resulting [[smooth manifold]] be [[diffeomorphism|non-diffeomorphic]] to the smooth manifold given by some evident 'standard' smooth structure on $X$. 

Mostly the term is used for smooth structures on [[Euclidean space]] $\mathbb{R}^n$ and on the [[n-spheres]] $S^n$, for $n \in \mathbb{N}$. The standard smooth structure on $\mathbb{R}^n$ is exhibited by the identity [[atlas]], and the standard smooth structure on $S^n$ is that given by the atlas by the two [[hemisphere]] as given by [[stereographic projection]].

For special values of $n$ there may exist smooth structure not equivalent to these. They are the _exotic smooth structures_.

A classification of [[smooth manifold|smooth]], [[piecewise-linear manifold|PL]] and [[topological manifold|topological]] structures on manifolds in dimension 5  and higher, in terms of various groups from [[algebraic topology]] (many not known) was established by [Kirby and Siebenmann (1977)](#KirbSieb) using [[obstruction theory]].



## Existence and Examples

### No exotic smooth structure in dimensions $\leq 3$

[Rado (1925)](#Rad) proved that in dimension 2 there are no exotic differentiable structures (or the uniqueness of the standard structure). The classification of 1-dimensional manifolds and the uniqueness of the smooth structure can be found in the Appendix of [Milnor (1965b)](#Milnor1965b).

[Moise (1952)](#Moise) proved that in dimension 3 there are no exotic differentiable structures, or to put in another way, 3-dimensional differentiable manifolds which are [[homeomorphism|homeomorphic]] are [[diffeomorphism|diffeomorphic]]. In this way the 3-sphere $S^3$ inherits a unique differentiable structure, no matter which $\mathbb{R}^4$ it is considered to be embedded in.



### No exotic Euclidean space away from dimension 4

There exists a unique smooth structure on the [[Euclidean space]] $\mathbb{R}^n$ for $n\neq 4$ ([Stallings 1962](#Stallings62)). 


### Exotic Euclidean 4-space
 {#ExoticEuclideal4Space}

There exists uncountably many exotic smooth structures on the [[Euclidean space]] $\mathbb{R}^4$ of dimension 4 ([Gompf 1985](#Gompf), [Freedman/Taylor 1986](#FreedTay), [Taubes 1987](#Taubes)). See also at _[[exotic R^4]]_.

There is a unique maximal exotic $\mathbb{R}^4$ into which all other 'versions' of $\mathbb{R}^4$ smoothly embed as open subsets (Freedman/Taylor 1986, [DeMichelis/Freedman 1992](#DeMFreed)).

There are two classes of exotic $\mathbb{R}^4$'s: large and small. A large exotic $\mathbb{R}^4$ cannot be embedded in the 4-sphere $S^4$ (Gompf 1985, Taubes 1987) whereas a small exotic $\mathbb{R}^4$ admits such an embedding (DeMichelis/Freedman 1992):

* A _large exotic $\mathbb{R}^4$_ is constructed by using the failure to smoothly split a smooth 4-manifold (the [[K3 surface]] for instance) as a [[connected sum]] of some factors (where a topological splitting exits). 

* The _small exotic $\mathbb{R}^4$_ (or _ribbon $\mathbb{R}^4$_) is constructed by using the failure of the smooth [[h-cobordism theorem]] in dimension 4 ([Donaldson 1987](#Donaldson1), [1990](#Donaldson2)). [Bizaca and Gompf (1996)](#BizGompf) are able to present an infinite handle body of a small exotic $\mathbb{R}^4$ which serve as a coordinate representation.

### Exotic 4-spheres?
 {#Exotic4Spheres}

It is open whether the [[4-sphere]] admits an exotic smooth structure. See ([Freedman-Gompf-Morrison-Walker 09](#FreedmanGompfMorrisonWalker09) for review).


### Exotic 7-sphere
 {#Exotic7Sphere}

[Milnor (1956)](#Milnor1956) gave the first examples of exotic smooth structures on the [[7-sphere]], finding at least seven. 

The [[exotic 7-spheres]] constructed in [Milnor 1956](#Milnor1956) are all examples of [[fibre bundles]] over the [[4-sphere]] $S^4$ with [[fibre]] the [[3-sphere]] $S^3$, with [[structure group]] the [[special orthogonal group]] [[SO(4)]] (see also at _[[8-manifold]]_ the section _[With exotic boundary 7-spheres](8-manifold#ExoticBoundary7Spheres)_):

By the classification of bundles on spheres via the [[clutching construction]], these correspond to [[homotopy classes]] of maps $S^3 \to SO(4)$, i.e. elements of $\pi_3(SO(4))$. From the table at [orthogonal group -- Homotopy groups](orthogonal+group#HomotopyGroups), this latter group is $\mathbb{Z}\oplus\mathbb{Z}$. Thus any such bundle can be described, up to [[isomorphism]], by a [[pair]] of [[integers]] $(n,m)$. When $n+m=1$, then one can show there is a [[Morse function]] with exactly two [[critical points]] on the total space of the bundle, and hence this 7-manifold is [[homeomorphic]] to a sphere.

The  [[fractional first Pontryagin class]] $\frac{p_1}{2} \in H^4(S^4) \simeq \mathbb{Z}$ of the bundle is given by $n-m$. Milnor constructs, using [[cobordism]] theory and [[Hirzebruch's signature theorem]] for 8-manifolds, a mod-7 diffeomorphism invariant of the manifold, so that it is standard 7-sphere precisely when $\frac{p_1}{2}^2 -1 = 0 (mod 7)$.

By using the [[connected sum]] operation, the set of smooth, non-diffeomorphic structures on the $n$-sphere has the structure of an [[abelian group]]. 
For the [[7-sphere]], it is the [[cyclic group]] $Z/{28}$ and Brieskorn (1966) found the generator $\Sigma$ so that $\underbrace{\Sigma\#\cdots\#\Sigma}_28$ is the standard sphere.

For review see for instance ([Kreck 10, chapter 19](#Kreck10), [McEnroe 15](#McEnroe15)). For more see at _[[exotic 7-sphere]]_.

From the point of view of [[M-theory on 8-manifolds]], these [[8-manifolds]] $X$ with (exotic) [[7-sphere]] [[boundaries]] correspond to [[near horizon limits]] of [[black brane|black]] [[M2 brane]] spacetimes $\mathbb{R}^{2,1} \times X$, where the [[M2-branes]] themselves would be sitting at the center of the [[7-spheres]] (if that were included in the spacetime, see also [[Dirac charge quantization]]).

([Morrison-Plesser 99, section 3.2](M-theory+on+8-manifolds#MorrisonPlesser99))

\linebreak

### Exotic $n$-spheres for $n \geq 5$
 {#ExoticNSpheresForNGreaterThanFour}

Via the celebrated [[h cobordism theorem]] of Smale ([Smale 1962](#Smale), [Milnor 1965](#Milnor1965a)) one gets a relation between the number of smooth structures on the $n$-sphere $S^n$ (for $n \geq 5$) and the number of [[isotopy]] classes $\pi_0 (Diff(S^{n-1}))$ of the [[equator]] $S^{n-1}$. 

Then [Kervaire and Milnor (1963)](#KervMil) proved that for each $n \geq 5$ there are only finitely many exotic smooth structures on the [[n-sphere]] $S^n$ (possibly none).

By using the [[connected sum]] operation, the set of smooth, non-diffeomorphic structures on the $n$-sphere has the structure of an [[abelian group]]. 

The only odd-dimensional spheres with _no_ exotic smooth structure are the [[circle]] $S^1$, the [[3-sphere]] $S^3$, as well as $S^5$ and $S^{61}$ ([Wang-Xu 16, corollary 1.13](#WangXu16))

In the range $5 \leq n  \leq 61$ the only $n$-spheres with _no_ exotic smooth structures are $S^5$, $S^6$, $S^{12}$, $S^{56}$ and $S^{61}$ ([Wang-Xu 16, corollary 1.15](#WangXu16)).

It is conjectured that this exhausts in fact all examples of $n$-spheres without exotic smooth structure for $n \geq 5$ ([Wang-Xu 16, conjecture 1.17](#WangXu16)).



## Related concepts

* [[differential topology]]


## References

See also

* Wikipedia, _[Exotic sphere](http://en.wikipedia.org/wiki/Exotic_sphere)_

### For the mathematical theory

The first construction of exotic smooth structures was on the 7-[[sphere]] in 

* {#Milnor1956} [[John Milnor]], _On manifolds homeomorphic to the 7-sphere_, Annals of Mathematics 64 (2): 399&#8211;405 (1956) ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/exotic.pdf), [doi:10.1142/9789812836878_0001](https://doi.org/10.1142/9789812836878_0001))


(...)

* {#Smale} [[Stephen Smale]],  _On the structure of manifolds_, Amer. J. of Math. 84 : 387-399 (1962)

* {#Milnor1965a} [[John Milnor]] (1965), _Lectures on the h-cobordism theorem_ (Princeton Univ. Press, Princeton)


* {#KervMil} [[Michel Kervaire]], ; [[John Milnor]],  (1963) "Groups of homotopy spheres: I", Ann. Math. 77, pp. 504 - 537.


* {#KirbSieb} Kirby, R.; Siebenmann, L. (1977) _Foundational essays on topological manifolds, smoothings, and triangulations_, Ann. Math. Studies (Princeton University Press, Princeton).


* {#Stallings62} John R. Stallings, _The piecewise-linear structure of Euclidean space_, Proceedings of the Cambridge Philosophical Society 58: 481&#8211;488 (1962) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/stallings2.pdf))


* {#FreedTay} Freedman, Michael H.; Taylor, Laurence (1986) "A universal smoothing of four-space", J. Diff. Geom. 24, pp. 69-78


* {#DeMFreed} De Michelis, Stefano; Freedman, Michael H. (1992) "Uncountably many exotic $\mathbb{R}^4$'s in standard 4-space", J. Diff. Geom. 35, pp. 219-254.
 

* {#Donaldson1} [[Simon Donaldson]] (1987) "Irrationality and the h-cobordism conjecture", J. Diff. Geom. 26, pp. 141-168.


* {#Donaldson2} [[Simon Donaldson]],  (1990) "Polynomial invariants for smooth four manifolds", Topology 29, pp. 257-315.
 

* {#Gompf} Gompf, Robert (1985) "An infinite set of exotic $\mathbb{R}^4$'s", J. Diff. Geom. 21, pp. 283-300.


* {#Taubes} Taubes, Clifford H. (1987) "Gauge theory on asymptotically periodic 4-manifolds", J. Diff. Geom. 25, pp. 363-430
 

* {#BizGompf} Bizaca, Z.; Gompf, Robert (1996) "Elliptic surfaces and some simple exotic $\mathbb{R}^4$'s", J. Diff. Geom. 43, pp. 458-504.


* {#Rad} Rado, T. (1925) "&#220;ber den Begriff der Riemannschen Fl&#228;che" , Acta Litt. Scient. Univ. Szegd 2, pp. 101-121


* {#Milnor1965b} [[John Milnor]], (1965b) _Topology from the Differentiable Viewpoint_ (University Press of Virginia)

* {#WangXu16} Guozhen Wang, Zhouli Xu, _The triviality of the 61-stem in the stable homotopy groups of spheres_ ([arXiv:1601.02184](https://arxiv.org
/abs/1601.02184))

* Llohann D. Sperança, _Pulling back the Gromoll-Meyer construction and models of exotic spheres_, Proceedings of the American Mathematical Society 144.7 (2016): 3181-3196 ([arXiv:1010.6039](https://arxiv.org/abs/1010.6039))

* Llohann D. Sperança, _Explicit Constructions over the Exotic 8-sphere_ ([pdf](https://www.ime.unicamp.br/~rigas/sigma8EncontroTopol.pdf), [[SperancaExoticSpheres.pdf:file]])

* {#DRL10} C. Duran, A. Rigas, Llohann D. Sperança, _Bootstrapping Ad-equivariant maps, diffeomorphisms and involutions_, Matematica Contemporanea, 35:27–39, 2010 ([pdf](http://www.ime.unicamp.br/~rigas/bootstrapping))


On the open issue of exotic [[4-spheres]]:

* {#FreedmanGompfMorrisonWalker09} [[Michael Freedman]], [[Robert Gompf]], [[Scott Morrison]], [[Kevin Walker]], _Man and machine thinking about the smooth 4-dimensional Poincar&#233; conjecture_, Quantum Topology, Volume 1, Issue 2 (2010), pp. 171-208 ([arXiv:0906.5177](http://arxiv.org/abs/0906.5177))


Review:

* {#Kreck10} [[Matthias Kreck]], chapter 19 "Exotic 7-spheres" of  _Differential Algebraic Topology -- From Stratifolds to Exotic Spheres_, AMS 2010

* [[Rustam Sadykov]], Sections 7,8 of: _Elements of Surgery Theory_, 2013 ([pdf](https://www.math.ksu.edu/~sadykov/Lecture%20Notes/Surgery%20Theory.pdf))


* {#McEnroe15} Rachel McEnroe, _Milnor' construction of exotic 7-spheres_, 2015 ([pdf](http://math.uchicago.edu/~may/REU2015/REUPapers/McEnroe.pdf))

See also

* Wikipedia ([spheres](http://en.wikipedia.org/wiki/Exotic_sphere#References), [$R^4$](http://en.wikipedia.org/wiki/Exotic_R4#References)) 


### For applications to physics
 {#ReferencesForApplicationsToPhysics}

The relevance of exotic smooth structure to [[physics]] is tantalizing but remains by and large unclear. Some of the following references probably ought to be handled with care.

#### General relativity

The argument that [[exotic spheres]] are to be regarded as [[gravitational instantons]]:

* {#Witten85} [[Edward Witten]], p. 12 of: _Global gravitational anomalies_, Comm. Math. Phys. Volume 100, Number 2 (1985), 197--229.  ([EUCLID](http://projecteuclid.org/euclid.cmp/1103943444))

* Randy A. Baadhio, _On the global gravitational instanton and soliton that are homotopy spheres_, Journal of Mathematical Physics 32, 2869 (1991) ([doi:10.1063/1.529078](https://doi.org/10.1063/1.529078))

Further discussion of exotic $4$-manifolds from the [[general relativity]] point of view is in 

* [[Carl Brans]], Duane Randall, _Exotic differentiable structures and general relativity_ Gen. Rel. Grav., 25 (1993) 205--220

* [[Carl Brans]], _Exotic smoothness and physics_ J. Math. Phys. 35, (1994), 5494--5506.

The following paper contained a first proof to localize exotic smoothness in an exotic $\mathbb{R}^4$:

* [[Carl Brans]], _Localized exotic smoothness_ Class. Quant. Grav., 11, (1994), 1785--1792.

A more philosophical discussion can be found in:

* [[Carl Brans]], _Absolute spacetime: the twentieth century ether_ Gen. Rel. Grav. 31, (1999),  597--609



#### Generation of source terms (fields)

Brans conjectured in the papers above, that exotic smoothness should be a source of an additional [[gravity|gravitational field]] (Brans conjecture). This conjecture was confirmed for compact $4$-manifolds (using implicitly a mapping of basic classes):


Using the invariant of L. Taylor [arXiv](http://de.arxiv.org/abs/math/9807143), Sladkowski confirmed the conjecture for the exotic $\mathbb{R}^4$ in:

* Jan S&#322;adkowski _Gravity on exotic R4 with few symmetries_ Int.J. Mod. Phys. D, 10, (2001) 311--313



#### Quantum (field) theory

The first real connection between exotic smoothness and [[quantum field theory]] is Witten's TQFT:

* [[Edward Witten]], _Topological quantum field theory_ Comm. Math. Phys., 117, (1988), 353--386.

and the whole work of Seiberg and Witten leading to the celebrated invariants.

The relation to particle physics by using the algebra of smooth functions can be found in

* Jan S&#322;adkowski, _Exotic smoothness, noncommutative geometry and particle physics_ Int. J. Theor. Phys., 35, (1996), 2075&#8211;2083

* Jan S&#322;adkowski, _Exotic smoothness and particle physics_ Acta Phys. Polon., B 27, (1996), 1649&#8211;1652

* Jan S&#322;adkowski, _Exotic smoothness, fundamental interactions and noncommutative geometry_ [arXiv] (http://arxiv.org/abs/hep-th/9610093)

The relation between TQFT and differential-topological invariants of smooth manifolds was clarified in:

* [[Hendryk Pfeiffer]] _Quantum general relativity and the classification of smooth manifolds_ [arXiv](http://arxiv.org/abs/gr-qc/0404088)

* [[Hendryk Pfeiffer]] _Diffeomorphisms from finite triangulations and absence of 'local' degrees of freedom_ Phys.Lett. B, 591, (2004), 197-201 


#### String theory
 {#ReferencesInStringTheory}

An argument for interpreting exotic smooth spheres as [[gravitational instantons]] and to cancel the gravitational [[anomalies]] of [[string theory]] is in ([Witten 85](#Witten85)).

The influence of exotic smoothness for [[Kaluza-Klein mechanism|Kaluza-Klein models]] was discussed here:

* [[Matthias Kreck]], [[Stefan Stolz]], _A diffeomorphism classification of $7$-dimensional homogeneous Einstein manifolds with $\mathfrak{su}(3) \times \mathfrak{su}(2) \times \mathfrak{u}(1)$-symmetry_ Ann. Math. 127, (1988), 373--388.

A discussion of topological effects (also of string theory) in relation to exotic smoothness is in

* Ryan Rohm, _Topological Defects and Differential Structures_ Annals Of Physics, 189, (1989), 223--239.






 
#### Cosmology


An overview can be also found in

* Jan S&#322;adkowski, _Exotic smoothness and astrophysics_ Act. Phys. Polon. B, 40, (2009), 3157--3163


#### Quantum gravity

A first calculation of the state sum in [[quantum gravity]] by inclusion of exotic smoothness

* Kristin Schleich, Donald Witt, _Exotic Spaces in Quantum Gravity I: Euclidean Quantum Gravity in Seven Dimensions_ Class.Quant.Grav., 16, (1999), 2447--2469

A semi-classical approach to the functional integral is discussed here:

* Christofer Duston, _Exotic smoothness in 4 dimensions and semiclassical Euclidean quantum gravity_ [arxiv](http://arxiv.org/abs/0911.4068)

The inclusion of singularities for asymptotically flat spacetimes is discussed here (with an example of a singularity coming from exotic smoothness):

* Kristin Schleich, Donald Witt, _Singularities from the Topology and Differentiable Structure of Asymptotically Flat Spacetimes_, [arxiv](http://arxiv.org/abs/1006.2890)


[[!redirects exotic smooth structure]]
[[!redirects exotic smooth structures]]

[[!redirects exotic sphere]]
[[!redirects exotic spheres]]

