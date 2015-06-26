
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--

> under construction

#Contents#
* table of contents
{:toc}

## Idea

Motivated by the resemblance of the [[Selberg trace formula]] to Weil's formula for the sum of zeros of the [[Riemann zeta function]], ([Selberg 56](#Selberg56)) defined for any compact hyperbolic [[Riemann surface]] a [[zeta function]]-like expression, the _[[Selberg zeta function of a Riemann surface]]_. (e.g. [Bump, below theorem 19](#Bump)). There is also a Selberg zeta function "of odd type" for odd-dimensional manifolds  ([Millson 78](#Millson78), [Bunke-Olbrich 94a, prop. 4.5](#BunkeOlbrich94a)).

## Definition

### For even-dimensional manifolds

(...)

### For odd-dimensional manifolds
 {#DefinitionForOdd}

Let 

* $n \in \mathbb{N}$, $n \geq 1$;

* $G = SO(n,1)$ the [[Lorentz group]] or $G = Spin(n,1)$ its [[spin group]];

* $K = SO(n)$ the [[special orthogonal group]] or $K = Spin(n)$ the [[spin group]];

* $K \hookrightarrow G$ the canonical inclusion, exhibiting a [[maximal compact subgroup]];

* $G = K A N$ an [[Iwasawa decomposition]];

* $\Gamma \hookrightarrow G$ a [[discrete group|discrete]] [[subgroup]];

* $E$ a [[complex vector space|complex]] [[finite dimensional vector space]] 

* $\chi \colon \Gamma \to U(E)$ a [[unitary representation]] of $\Gamma$.

Then the [[quotient]]

$$
  X \coloneqq \Gamma \backslash G / K
$$

is a [[hyperbolic manifold]] of odd [[dimension]] with [[fundamental group]] being $\pi_1(X) \simeq \Gamma$. Accordingly the representation $\chi$ is equivalently a [[flat vector bundle]] on $X$.

Write $Conj(\Gamma)$ for the set of [[conjugacy classes]] of $\Gamma$ and write

$$
  Prim(\Gamma) \hookrightarrow Conj(\Gamma)
$$

for the [[subset]] of elements $[g]$ for which $n_\Gamma(g) = 1$. Regarded as elements of the [[fundamental group]] as above, these elements correspond to paths which are [[prime geodesics]] in $X$.

**Definition**

The _Selberg zeta function_ $\zeta_\chi$ of this data is defined for $Re(s)\gt \rho \coloneqq (n-1)/2$ to be the [[infinite product]]

$$
  \zeta_\chi(s) =
  \underset{{[g] \in Prim(\Gamma)} \atop {[g] \neq 1}}{\prod}
  \;
  \underoverset{k = 0}{\infty}{\prod} 
  \det\left(
    1 - 
    e^{-(\rho + s)l(g)}
    S^k(Ad(g)^{-1}_{\mathbf{n}})
    \sigma(m)
    \;
    \chi(g)
  \right)
$$

(...) ([BunkeOlbrich 94a, def. 4.1](#BunkeOlbrich94a))

## Properties

### Analogy with Artin L-function
 {#AnalogyWithArtinLFunction}

That the Selberg zeta function is equivalently an [[Euler product]] of [[characteristic polynomials]] is due to ([Gangolli 77, (2.72)](#Gangolli77), [Fried 86, prop. 5](#Fried86)).

That it is in particular the Euler product of [[characteristic polynomials]] of the [[determinants]] of the [[monodromies]] of the [[flat connection]] corresponding to the given [[group representation]] (similar to the [[Ruelle zeta function]]) is ([Bunke-Olbrich 94, prop. 6.3](#BunkeOlbrich94)) for the even-dimensional case and ([Bunke-Olbrich 94a, def. 4.1](#BunkeOlbrich94a)) for the odd-dimensional case. (Or rather, the [[Ruelle zeta function]] ([Bunke-Olbrich 94a, def. 5.1](#BunkeOlbrich94a))).

This is [[analogy|analogous]] to the standard definition of an [[Artin L-function]] if one interprets a) a [[Frobenius map]] $Frob_p$ (as discussed there) as an element of the [[arithmetic fundamental group]] of an [[arithmetic curve]] and b) a [[Galois representation]] as a [[flat connection]].

So under this analogy the Selberg zeta function for hyperbolic 3-manifolds as well as the [[Artin L-function]] for a [[number field]] both are like an [[infinite product]] over primes ([[prime geodesics]] in one case, [[prime ideals]] in the other, see also at _[Spec(Z) -- As a 3-dimensional space containing knots](Spec%28Z%29#As3dSpaceContainingKnots)_) of determinants of monodromies of the given flat connection.

See at _[Artin L-function -- Analogy with Selberg zeta function](Artin%20L-function#AnalogyWithSelbergZeta)_ for more. This analogy has been highlighted in ([Brown 09](#Brown09), [Morishita 12, remark 12.7](#Morishita12)).

### Relation to the eta-function
 {#RelationToTheEtaFunction}

Under suitable conditions, the Selberg zeta function of odd type is an exponential of the [[eta function]] of a suitable [[Dirac operator]] 

$$
  \zeta_S(0) = \exp\left(i \pi \eta_D(0)\right)
$$

([Millson 78](#Millson78), [Bunke-Olbrich 94a, prop. 4.5](#BunkeOlbrich94a), [Park 01, theorem 1.2](#Park01), [Guillarmou-Moroianu-Park 09](#GuillarmouMoroianuPark09)). 

### Relation to analytic torsion 
 {#RelationToAnalyticTorsion}

The [[Ruelle zeta function]] at 0 gives a power of [[analytic torsion]]

([Fried 86](#Fried86), [Bunke-Olbrich 94a, theorem 5.5.](#BunkeOlbrich94a))

* [analytic torsion -- relation to Selberg zeta function](analytic+torsion#RelationToSelbergZeta)



### Relation to prime geodesic asymptotics

The Selberg zeta function controls the [[asymptotics]] of [[prime geodesics]] via the [[prime geodesic theorem]] in direct [[analogy]] to how the [[Riemann zeta function]] controls the asymptotics of [[prime numbers]] via the [[prime number theorem]].

## Related concepts

* [[Ruelle zeta function]]

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

## References

The original article is

* {#Selberg56} [[Atle Selberg]], _Harmonic analysis and discontinuous groups in weakly symmetric Riemannian spaces with applications to Dirichlet series_, Journal of the Indian Mathematical Society 20 (1956) 47-87.

Review includes

* Wikipedia, _[Selberg zeta function](http://en.wikipedia.org/wiki/Selberg_zeta_function)_


* {#Watkins} [[Matthew Watkins]], citation collection on _[Selberg trace formula and zeta functions](http://empslocal.ex.ac.uk/people/staff/mrwatkin/zeta/physics4.htm)_

* {#Bump} Bump, below theorem 19 in _Spectral theory of $\Gamma \backslash SL(2,\mathbb{R})$_ ([[BumpSpectralTheory.pdf:file]])

* _Selberg and Ruelle zeta functions for compact hyperbolic manifolds_ ([pdf](http://www.math.uni-bonn.de/people/xenia/Oberseminar%202014/Oberseminar%202014.pdf))


Expression of the Selberg/Ruelle zeta function as an [[Euler product]] of [[characteristic polynomials]] is due to 

* {#Gangolli77} Ramesh Gangolli, _Zeta functions of Selberg's type for compact space forms of symmetric spaces of rank one_, Illinois J. Math. Volume 21, Issue 1 (1977), 1-41. ([Euclid](http://projecteuclid.org/euclid.ijm/1256049498))

* {#Fried86} [[David Fried]], _The zeta functions of Ruelle and Selberg. I_, Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 19 no. 4 (1986), p. 491-517 ([Numdam](http://www.numdam.org/item?id=ASENS_1986_4_19_4_491_0))

The analogy with the [[Artin L-function]] is highlighted in 

* {#Brown09} Darin Brown, _Lifting properties of prime geodesics_, Rocky Mountain J. Math. Volume 39, Number 2 (2009), 437-454 ([euclid](http://projecteuclid.org/euclid.rmjm/1239113439))

* {#Morishita12} [[Masanori Morishita]], section 12.1 of _Knots and Primes: An Introduction to Arithmetic Topology_, 2012 ([web](https://books.google.co.uk/books?id=DOnkGOTnI78C&pg=PA156#v=onepage&q&f=false))

Discussion of the relation between, on the one hand, [[zeta function of an elliptic differential operator|zeta function]] of [[Laplace operators]]/[[eta function of a self-adjoint operator|eta funcstions]] of [[Dirac operators]] and, on the other hand, Selberg zeta functions includes


* {#DHokerPhong86} [[Eric D'Hoker]] [[Duong Phong]], _Communications in Mathematical Physics_, Volume 104, Number 4 (1986), 537-545 ([Euclid](http://projecteuclid.org/euclid.cmp/1104115166))

* {#Sarnak87} [[Peter Sarnak]], _Determinants of Laplacians_, Communications in Mathematical Physics, Volume 110, Number 1 (1987), 113-120. ([Euclid](http://projecteuclid.org/euclid.cmp/1104159171))

* [[Ulrich Bunke]], [[Martin Olbrich]], Andreas Juhl, _The wave kernel for the Laplacian on the classical locally symmetric spaces of rank one, theta functions, trace formulas and the Selberg zeta function_, Annals of Global Analysis and Geometry February 1994, Volume 12, Issue 1, pp 357-405

* {#BunkeOlbrich94} [[Ulrich Bunke]], Martin Olbrich, _Theta and zeta functions for locally symmetric spaces of rank one_ ([arXiv:dg-ga/9407013](http://arxiv.org/abs/dg-ga/9407013))

and for odd-dimensional spaces also in

* {#Fried86} [[David Fried]], _Analytic torsion and closed geodesics on hyperbolic manifolds_, Invent. math. 84, 523-540 (1986) ([pdf](http://gdz-lucene.tc.sub.uni-goettingen.de/gcs/gcs?&&action=pdf&metsFile=PPN356556735_0084&divID=LOG_0026&pagesize=original&pdfTitlePage=http://gdz.sub.uni-goettingen.de/dms/load/pdftitle/?metsFile=PPN356556735_0084%7C&targetFileName=PPN356556735_0084_LOG_0026.pdf&))


* {#Millson78} [[John Millson]], _Closed geodesic and the $\eta$-invariant_, Ann. of Math., 108, (1978) 1-39 ([jstor](http://www.jstor.org/stable/1970928))

* {#BunkeOlbrich94a} [[Ulrich Bunke]], [[Martin Olbrich]], _Theta and zeta functions for odd-dimensional locally symmetric spaces of rank one_ ([arXiv:dg-ga/9407012](http://arxiv.org/abs/dg-ga/9407012))

* {#BunkeOlbrich94b} [[Ulrich Bunke]], [[Martin Olbrich]] _$\Gamma$-Cohomology and the Selbeg zeta function_ ([arXiv:dg-ga/9411004](http://arxiv.org/abs/dg-ga/9411004))

* [[Ulrich Bunke]], [[Martin Olbrich]], _Group cohomology and the singularities of the Selberg zeta function associated to a Kleinian group_ ([arXiv:dg-ga/9603003](http://arxiv.org/abs/dg-ga/9603003))

* {#BunkeOlbrich95} [[Ulrich Bunke]], [[Martin Olbrich]], _Selberg zeta and theta functions: a differential operator approach_, Akademie Verlag 1995

* {#Park01} Jinsung Park, _Eta invariants and regularized determinants for odd dimensional hyperbolic manifolds with cusps_ ([arXiv:0111175](http://arxiv.org/abs/math/0111175))


* {#Friedman04} [[Joshua Friedman]], _The Selberg trace formula and Selberg zeta-function for cofinite Kleinian groups with finite-dimensional unitary representations_ ([arXiv:math/0410067](http://arxiv.org/abs/math/0410067))

* {#Friedman06} [[Joshua Friedman]], _Regularized determinants of the Laplacian for cofinite Kleinian groups with finite-dimensional unitary representations_, Communications in Mathematical Physics ([arXiv:math/0605288](http://arxiv.org/abs/math/0605288))

* {#GuillarmouMoroianuPark09} Colin Guillarmou, Sergiu Moroianu, Jinsung Park, _Eta invariant and Selberg Zeta function of odd type over convex co-compact hyperbolic manifolds_ ([arXiv:0901.4082](http://arxiv.org/abs/0901.4082))



[[!redirects Selberg zeta function of a Riemann surface]]