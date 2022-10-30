
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--
#Contents#
* table of contents
{:toc}

## Idea

For $X_\Gamma$ a [[hyperbolic manifold]] of odd [[dimension]], and given a [[flat connection|flat]] $GL$-[[principal connection]] $\rho$ on $X_\Gamma$, the _Ruelle zeta function_ is the [[meromorphic function]] $R_\rho$
given for $Re(s)  \gt (dim(X_\gamma)-1)/2 $ by the [[infinite product]] ([[Euler product]]) over the [[characteristic polynomials]] of the [[monodromy]]/[[holonomy]] of the flat connection along [[prime geodesics]]

$$
  R_\rho(s) 
   = 
  \underset{\gamma}{\prod} \det 
  \left( 
    Id - hol_\rho(\gamma) e^{-s l(\gamma)} 
  \right)
$$

and defined from there by [[analytic continuation]].

Here 

* the product is over [[prime geodesics]] $\gamma$;

* of [[length]] $l(\gamma)$;

* and $hol_\rho(\gamma)$ denotes the [[holonomy]] of $\rho$ along $\gamma$.

## Properties

### Relation to the Selberg zeta function

for the moment see at _[[Selberg zeta function]]_.

### Analogy to the Artin L-function
 {#AnalogyToTheArtinLFunction}

The Ruelle zeta function is [[analogy|analogous]] to the standard definition of an [[Artin L-function]] if one interprets a) a [[Frobenius map]] $Frob_p$ (as discussed there) as an element of the [[arithmetic fundamental group]] of an [[arithmetic curve]] and b) a [[Galois representation]] as a [[flat connection]].

So under this analogy the Ruelle zeta function for hyperbolic 3-manifolds as well as the [[Artin L-function]] for a [[number field]] both are like an [[infinite product]] over primes ([[prime geodesics]] in one case, [[prime ideals]] in the other, see also at _[Spec(Z) -- As a 3-dimensional space containing knots](Spec%28Z%29#As3dSpaceContainingKnots)_) of determinants of monodromies of the given flat connection.

See at _[Artin L-function -- Analogy with Selberg/Ruelle zeta function](Artin%20L-function#AnalogyWithSelbergZeta)_ for more. This analogy has been highlighted in ([Brown 09](#Brown09), [Morishita 12, remark 12.7](#Morishita12)).

### Relation to volume and analytic torsion

The [[special values of L-functions|special value]] of $R_\rho$ at the origin encodes 

* the [[Reidemeister torsion]] ([Fried 86, theorem 1](#Fried86));

* the [[volume]] of the hyperbolic manifold ([Mathai 92](#Mathai92), [Lott 92](#Lott92)).



## References

Original articles include

* {#Fried86} [[David Fried]], _Analytic torsion and closed geodesics on hyperbolic manifolds_, Invent. math. 84, 523-540 (1986) ([pdf](http://gdz-lucene.tc.sub.uni-goettingen.de/gcs/gcs?&&action=pdf&metsFile=PPN356556735_0084&divID=LOG_0026&pagesize=original&pdfTitlePage=http://gdz.sub.uni-goettingen.de/dms/load/pdftitle/?metsFile=PPN356556735_0084%7C&targetFileName=PPN356556735_0084_LOG_0026.pdf&))


* {#BunkeOlbrich94a} [[Ulrich Bunke]], [[Martin Olbrich]], _Theta and zeta functions for odd-dimensional locally symmetric spaces of rank one_ ([arXiv:dg-ga/9407012](http://arxiv.org/abs/dg-ga/9407012))

Seminar notes include

* _Selberg and Ruelle zeta functions for compact hyperbolic manifolds_ ([pdf](http://www.math.uni-bonn.de/people/xenia/Oberseminar%202014/Oberseminar%202014.pdf))

Relation to the [[volume]] of hyperbolic manifolds is discussed in

* {#Mathai92} [[Varghese Mathai]], section 6 of _$L^2$-analytic torsion_, Journal of Functional Analysis Volume 107, Issue 2, 1 August 1992, Pages 369&#8211;386

* {#Lott92} [[John Lott]], _Heat kernels on covering spaces and topological invariants_, J. Diff. Geom. 35 no 2 (1992) ([pdf](https://math.berkeley.edu/~lott/covering.pdf))


The [[analogy]] with the [[Artin L-function]] is discussed in

* {#Brown09} Darin Brown, _Lifting properties of prime geodesics_, Rocky Mountain J. Math. Volume 39, Number 2 (2009), 437-454 ([euclid](http://projecteuclid.org/euclid.rmjm/1239113439))

* {#Morishita12} [[Masanori Morishita]], section 12.1 of _Knots and Primes: An Introduction to Arithmetic Topology_, 2012 ([web](https://books.google.co.uk/books?id=DOnkGOTnI78C&pg=PA156#v=onepage&q&f=false))
