

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Killing spinor_ on a ([[pseudo-Riemannian manifold|pseudo]]-)[[Riemannian manifold]] $X$ is a _[[spinor]]_  -- a [[section]] of some [[spinor bundle]] $v \in \Gamma(S)$ -- that is taken by the  [[covariant derivative]] of the corresponding [[Levi-Civita connection]] to a multiple of itself

$$
  \nabla_v \psi = \kappa \gamma_v \psi
$$

for some constant $\kappa$.

If that constant is 0, hence if the spinor is _covariant constant_, then one also speaks of a _covariant constant spinor_ or _parallel spinor_ (with respect to the given metric structure).

More generally, a _twistor spinor_ or _conformal Killing spinor_ is a $\psi$ such that

$$
  \nabla_v \psi = \frac{1}{dim(X)} \gamma_v D \psi
  \,,
$$

where $D$ is the given [[Dirac operator]] (e.g. [Baum 00](#Baum00)).

A Killing spinor with non-vanishing $\kappa$ may be understood as a genuine covariantly constant spinor, but with respect to a [[super-Cartan geometry]] modeled not on [[super-Euclidean space]]/[[super-Minkowski spacetime]], but on its spherical/hyperbolic or deSitter/anti-deSitter versions ([Egeileh-Chami 13, p. 60 (8/8)](#EgeilehChami13)).

Similarly a _[[Killing vector]]_ is a covariantly constant [[vector field]].

Pairing two covariant constant spinors to a vector yields a Killing vector. 

In [[supergravity]], [[super spacetimes]] which solves the [[equations of motion]] and admit Killing spinors are _[[BPS states]]_ (at least if they are asymptotically flat and of finite mass).

## Related concepts

* [[Killing vector]]

* [[Killing tensor]]

* [[Killing-Yano tensor]]

* [[superisometry]]

* [[supersymmetry and Calabi-Yau manifolds]]


## References

### General

Lecture notes include

* _Parallel and Killing spinor fields_ ([[KillingSpinors.pdf:file]])

* {#Baum00} [[Helga Baum]], _Twistor and Killing spinors in Lorentzian geometry_, S&#233;minaires & Congr&#232;s, 4, 2000 ([pdf](http://www.emis.de/journals/SC/2000/4/pdf/smf_sem-cong_4_35-52.pdf))

* [[Helga Baum]], _Conformal Killing spinors and the holonomy problem in Lorentzian geometry_ ([pdf](http://www.mathematik.hu-berlin.de/~baum/publikationen-fr/Publikationen-ps-dvi/IMA06-neu.pdf))

See also

* &#214;zg&#252;r A&#231;&#305;k, _Field equations from Killing spinors_ ([arXiv:1705.04685](https://arxiv.org/abs/1705.04685))

* Ángel Murcia, C. S. Shahbazi, 
_Parallel spinors on globally hyperbolic Lorentzian four-manifolds_ ([arXiv:2011.02423](https://arxiv.org/abs/2011.02423))


Discussion relating to [[Killing vectors]] in [[supergeometry]] ([[superisometries]]) is in

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], pages 1198-1199 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

and later in

* [[Dmitri Alekseevsky]], [[Vicente Cortés]], [[Chandrashekar Devchand]], [[Uwe Semmelmann]], _Killing spinors are Killing vector fields in Riemannian Supergeometry_ ([arXiv:dg-ga/9704002](http://arxiv.org/abs/dg-ga/9704002))

See also 

* [[Christian Bär]], _Real Killing spinors and holonomy_, Comm. Math. Phys.
Volume 154, Number 3 (1993), 509-521 ([Euclid](https://projecteuclid.org/euclid.cmp/1104253076))


Discussion regarding the conceptualization of Killing spinors in [[super-Cartan geometry]] is in

* {#EgeilehChami13} Michel Egeileh, Fida El Chami, _Some remarks on the geometry of superspace supergravity_, J.Geom.Phys. 62 (2012) 53-60 ([spire](http://inspirehep.net/record/1333125))

Discussion relating to [[special holonomy]] includes

* Andrei Moroianu, [[Uwe Semmelmann]], _Parallel spinors and holonomy groups_, Journal of Mathematical Physics 41 (2000), 2395-2402 ([arXiv:math/9903062](http://arxiv.org/abs/math/9903062))


Discussion of classification includes

* [[Thomas Friedrich]], _Zur Existenz paralleler Spinorfelder &#252;ber Riemannschen Mannigfaltigkeiten_ Czechoslavakian-GDR-Polish scientific school on differential geometry Boszkowo/ Poland 1978, Sci. Comm., Part 1,2; 104-124 (1979)

* [[Thomas Friedrich]], _Zur Existenz paralleler Spinorfelder &#252;ber Riemannschen Mannigfaltigkeiten_, Colloquium Mathematicum vol. XLIV, Fasc. 2 (1981), 277-290.

### Relation to supersymmetry

General discussion of Killing with an eye towards applications in [[supersymmetry]] is around page 907 in volume II of

* [[Pierre Deligne]], P. Etingof, [[Dan Freed]], L. Jeffrey, D. Kazhdan, J. Morgan, D.R. Morrison and [[Edward Witten]], (eds.)  _Quantum Fields and Strings, A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

specifically

in [[heterotic supergravity]]:

* [[Ulf Gran]], [[George Papadopoulos]], Diederik Roest, _Supersymmetric heterotic string backgrounds_, Phys.Lett.B656:119-126, 2007 ([arXiv:0706.4407](https://arxiv.org/abs/0706.4407))

in [[11-dimensional supergravity]]:

* [[Jerome Gauntlett]], Stathis Pakis, _The Geometry of $D=11$ Killing Spinors_, JHEP 0304 (2003) 039 ([arXiv:hep-th/0212008](http://arxiv.org/abs/hep-th/0212008))

for [[G2-structures]] in [[M-theory on G2-manifolds]]:

* [[Thomas Friedrich]], Stefan Ivanov, _Parallel spinors and connections with skew-symmetric torsion in string theory_, AsianJ.Math.6:303-336,2002 ([arXiv:math/0102142](http://arxiv.org/abs/math/0102142))



[[!redirects Killing spinors]]

[[!redirects covariantly constant spinor]]
[[!redirects covariantly constant spinors]]

[[!redirects Killing spinor field]]
[[!redirects Killing spinor fields]]

[[!redirects parallel spinor]]
[[!redirects parallel spinors]]

[[!redirects twistor spinor]]
[[!redirects twistor spinors]]

[[!redirects parallel spinor field]]
[[!redirects parallel spinor fields]]
