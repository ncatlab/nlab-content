
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Theta functions
+--{: .hide}
[[!include theta functions - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition


+-- {: .num_defn #SeriesDefinition}
###### Definition

Given a [[self-adjoint operator]] $D$ (usually first-order, such as a [[Dirac operator]] acting on [[sections]] of a [[vector bundle]] on a [[closed manifold|closed]] [[Riemannian manifold]]) with [[eigenvalues]] with multiplicities $\{\lambda_n\}$, then its _eta function_ is given by the [[series]]

$$
  \begin{aligned}
    \eta(s) 
     & \coloneqq
    \underoverset{n = -\infty}{^\infty }{\sum} sgn(\lambda_n) \frac{1}{ {\vert \lambda_n\vert}^s}
  \end{aligned}
$$

expression wherever this [[convergence|converges]], and extended by [[analytic continuation]] from there.

=--

+-- {: .num_remark}
###### Remark

At the [[special values of L-functions|special value]] $s = 1$ the series in def. \ref{SeriesDefinition} does not converge, but if $D$ is indeed a [[Dirac operator]] then it is the expression of the [[Dirac propagator]]. Indeed the definition of $\eta$ by [[analytic continuation]] at $s = 1$ is the [[regularization (physics)|regularized]] [[Dirac propagator]].

=--

+-- {: .num_remark}
###### Remark

The eta function of $D$ is related to the [[zeta function of an elliptic differential operator]] $H = D^2$ (regarding $D$ as a [[Dirac operator]]/[[supersymmetric quantum mechanics]]-like square root of $H$) see [below](RelationToTheZetaFunction).

=--


+-- {: .num_defn #EtaInvariant}
###### Definition

The _eta invariant_ of $D$ is the [[special values of L-functions|special value]] $\eta(0)$.

=--

(e.g. [Richardson, first page](#Richardson))

+-- {: .num_remark }
###### Remark

Def. \ref{EtaInvariant} means that $\eta_0$ is the
[[zeta function regularization|regularized]] number of positive minus negative eigenvalues of $D$.

=--


(Notice that if $D$ itself happens to have only positive [[eigenvalues]], then its eta function already is on the notre the [[zeta function of an elliptic differential operator]].)


## Properties

### Relation to the theta-function / Mellin transform

The eta function is a kind of odd version of the [[Mellin transform]] of an odd version of the [[theta function]]:

$$
  \eta_D(s)
  =
  \frac{1}{\Gamma((s+1)/2)}
  \underoverset{0}{\infty}{\int}
  t^{(s-1)/2}
  Tr(D\,\exp(-t D^2))
  \,
  d t
  \,.
$$

e.g. ([M&#252;ller 94 (0.2)](#M&#252;ller94)).


### Relation to the zeta function
 {#RelationToTheZetaFunction}

#### Generally

Let $D$ be a [[self-adjoint operator]] such that

1. its eta function $\eta(s)$ is defined and [[analytic function|analytic]] at $s= 0$;

1. for $c \in I \subset \mathbb{R}$ in an interval such that no $-c$ is an [[eigenvalue]] of $D$ such that both the eta series $\eta_{D+c}$ and the [[zeta function of an elliptic differential operator|zeta function]] series $\zeta_{(D+c)^2}((s+1)/2)$ have a common lower bound $s \gt B$ for the values on wich the series converges

then 

$$
  \frac{d}{d c} \eta_{D+c}(s) = s \zeta_{(D + c)^2}((s+1)/2)
  \,,
$$

where on the left we have the [[zeta function of an elliptic differential operator]] for $(D+c)^2$.

(e.g. [Richardson prop. 2](#Richardson)).

In particular this means that under the above assumptions the [[functional determinant]] of $D^2$ is given by

$$
  det (D^2) 
   = 
  \exp\left( 
    \frac{\partial}{\partial s}\frac{\partial}{\partial c} \eta_{D}(0)
  \right)
  \,.
$$

#### On odd-dimensional manifolds
 {#OnOddDimensionalManifolds}

Under suitable conditions the exponentiated $\eta$-invariant $\exp(\pi i \eta(0))$ equals the [[Selberg zeta function]] of odd type.  ([Millson 78](#Millson78), [Park 01, theorem 1.2](#Park01), [Guillarmou-Moroianu-Park 09](#GuillarmouMoroianuPark09)).

### Relation with L-function
 {#AnalogyWithLSeries}

Relation of eta functions to [[Dirichlet L-functions]] includes ([Atiyah-Donelly-Singer 83](#AtiyahDonellySinger83), [Podesta 14](#Podesta14))

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]


### Boundaries, determinant line bundles and perturbative Chern-Simons
 {#OnManifoldsWithBoundary}

Let $\pi \colon X \to Z$ be a $Z$-parameterized collection of [[spin structure|spin]] [[Riemannian manifold]] of odd [[dimension]] with [[boundary]].

Equip the corresponding collection of [[Dirac operators]] $D_X$ with the [[boundary condition]] given by a choice of [[isometry]]

$$
  Ker^+ D_{\partial X} \simeq Ker^- D_{\partial X}
  \,.
$$

e.g. ([M&#252;ller 94, below (0.3)](#M&#252;ller94))

Define then the exponentiated eta-invariant to be the element

$$
  \tau_X 
   \coloneqq 
  \exp\left(
    \pi i 
    \left(   
        \eta_X(0)  + dim\left(ker D_X\right)
    \right)
  \right)
  \in
  Det^{-1}_{\partial X}
$$

in the inverse of the [[determinant line]]

$$
  Det_{\partial X} 
    \coloneqq
  \left(
    det\left(ker^- D_{\partial X}\right)
  \right)
  \otimes
  \left(
    det\left(ker^+ D_{\partial X}\right)
  \right)^{-1}
  \,.
$$

(Here it is maybe noteworthy that, by the [above](#OnOddDimensionalManifolds), $\zeta_S = \exp(i \pi\, \eta_X(0))$ is the [[Selberg zeta function]].)

In fact this is a smooth [[section]] of the [[determinant line bundle]] as $X$ varies. 

+-- {: .num_prop #ExponentiatedEtaSatisfiesSewing}
###### Proposition

These sections given by the exponentiated eta invariant satisfy the [[sewing law]].

=--

This is due to ([Dai-Freed 94](#DaiFreed94)), reviewed in ([Freed 95a](#Freed95a)). See also ([Witten 15](#Witten15)) for discussion in relation to [[anomaly cancellation]] of [[fermions]] (specifically for the eta invariant in the [[Green-Schwarz mechanism]] see [Witten 99, section 2.2](Green-Schwarz+mechanism#Witten99)).

+-- {: .num_remark}
###### Remark

Prop. \ref{ExponentiatedEtaSatisfiesSewing} means that the eta-invariant satisfies something like the Atiyah-axioms for [[TQFT]] (but of course $\eta$ depends on a [[Riemannian metric|metric]]), a point of view highlighted in ([Bunke 94](#Bunke94)).  
Indeed, this exponentiated eta invariant is one factor (together with [[analytic torsion]] and the classical CS invariant) of the [[perturbation theory|perturbative]] [[path integral quantization]] of [[Chern-Simons theory]] ([Witten 89 (2.17) (2.23)](#Witten89)), see at _[Chern-Simons theory -- Perturbative path integral quantization](Chern-Simons+theory#PerturbativePathIntegralQuantization)_.

=--

+-- {: .num_remark}
###### Remark


Also the [[theta function]] is a section of, up to [[isomorphism]], this determinant line bundle (or maybe its inverse) ([Freed 95b, p. 31](#Freed95b)).

> (and hopefully it coincides with the section given by the exponentiated $\eta$ under suitable conditions?)

=--

## Examples

### For Dirac operator on Riemann surfaces

For the [[Dirac operator]] on a [[Riemann surface]]/[[complex curve]] the eta function was discussed in ([Millson 78](#Millson78)).

See at _[[zeta function of a Riemann surface]]_ for more on this case.


## Related concepts

* [[e-invariant]]

* [[index of an operator]]

* [[Spin Chern-Simons theory]]

## References

The $\eta$-invariant was introduced by Atiyah-Patodi-Singer in the series of articles

* [[Michael Atiyah]], V. K. Patodi and [[Isadore Singer]], _Spectral asymmetry and Riemannian geometry I_ Proc. Cambridge Philos. Soc. 77 (1975), 43-69.

   _Spectral asymmetry and Riemannian geometry II. Proc. Cambridge Philos. Soc.

  _Spectral asymmetry and Riemannian geometry III_, Proc. Cambridge Philos. Soc. 79 (1976), 71-99.

as the [[boundary]] correction term  for the [[analytic index|index formula]] on a [[manifold with boundary]].


Introductions and surveys include

* [[Jean-Michel Bismut]], _Local index theory, eta invariants and holomorphic torsion: a survey_, pp. 1-76, in: Surveys in diff. geom. 3 (C.-C. Hsiung, S.-T. Yau, eds.) 1996. International Press

* {#Richardson} [[Ken Richardson]], _Introduction to the Eta invariant_ ([pdf](http://faculty.tcu.edu/richardson/Seminars/etaInvariant.pdf))

* [[Xianzhe Dai]], _Eta invariant and holonomy_ Chern Centennial (2011) ([pdf slides](http://www.nim.nankai.edu.cn/activites/conferences/Chern-Centennial-20111024/ppt_pdf/1027pm-XZDai.pdf))

* Wikipedia, _[Eta invariant](http://en.wikipedia.org/wiki/Eta_invariant)_


Formulation in the broader context of bordism theory is in 

* [[Ulrich Bunke]], _On the topological contents of eta invariants_ ([arXiv:1103.4217](http://arxiv.org/abs/1103.4217))

Further discussion of the relation to [[holonomy]] is in

* [[Xianzhe Dai]], [[Weiping Zhang]], _Eta invariant and holonomy, the even dimensional case_, [arXiv:1205.0562](http://arxiv.org/abs/1205.0562)

* _Eta invariant and Selberg  zeta function of odd type over convex co-compact hyperbolic manifolds_ ([pdf](http://www.imar.ro/~sergium/fisiere/Eta-Selberg2501.pdf))

Discussion of relation to [[L-functions]] includes

* {#AtiyahDonellySinger83} [[Michael Atiyah]],  H. Donnelly; , [[Isadore Singer]], _Eta invariants, signature defects of cusps, and values of L-functions_, Annals of Mathematics. Second Series 118 (1): 131&#8211;177 (1983) doi:10.2307/2006957, ISSN 0003-486X, MR 707164

* {#Podesta14} Ricardo A. Podest&#225;, _The eta function and eta invariant of Z2r-manifolds_ ([ariv:1407.7454](http://arxiv.org/abs/1407.7454))

Discussion of the case over [[Riemann surfaces]] includes

* {#Millson78} [[John Millson]], _Closed geodesic and the $\eta$-invariant_, Ann. of Math., 108, (1978) 1-39 ([jstor](http://www.jstor.org/stable/1970928))

* {#Park01} Jinsung Park, _Eta invariants and regularized determinants for odd dimensional hyperbolic manifolds with cusps_ ([arXiv:0111175](http://arxiv.org/abs/math/0111175))

* {#GuillarmouMoroianuPark09} Colin Guillarmou, Sergiu Moroianu, Jinsung Park, _Eta invariant and Selberg Zeta function of odd type over convex co-compact hyperbolic manifolds_ ([arXiv:0901.4082](http://arxiv.org/abs/0901.4082))


Discussion in relation to [[analytic torsion]] and [[perturbation theory|perturbative]] quantum [[Chern-Simons theory]] goes back to

* {#Witten89} [[Edward Witten]] _Quantum Field Theory and the Jones Polynomial_ Commun. Math. Phys. 121 (3) (1989) 351&#8211;399. MR0990772 ([project EUCLID](http://projecteuclid.org/euclid.cmp/1104178138))

with more in  

* {#Lott90} [[John Lott]], _Eta and torsion_, 1990 ([pdf](http://math.berkeley.edu/~lott/lhouches.pdf))

* [[Lisa Jeffrey]], _Symplectic quantum mechanics and Chern-Simons gauge theory I_,  ([arxiv/1210.6635](http://arxiv.org/abs/1210.6635))

* [[Lisa Jeffrey]], Brendan McLellan, _Eta-Invariants and Anomalies in U(1) Chern-Simons Theory_ ([pdf](http://www.math.toronto.edu/mclellan/eta%20invariants%20and%20anomalies.pdf))

* {#Young} M. B. Young, section 2 of _Chern-Simons theory, knots and moduli spaces of connections_ ([pdf](http://www.math.sunysb.edu/~myoung/CS.pdf))

Discussion of the eta-invariant on manifolds with boundary is in

* {#M&#252;ller94} Werner M&#252;ller, _Eta invariants and manifolds with boundary_, J. Diff. Geom. 40 (1994) 311-377 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/mueller.pdf))

* {#Bunke94} [[Ulrich Bunke]], _The $\eta$-Invariant as a Lagrangian of a Topological Quantum Field Theory_ ([arXiv:hep-th/9408162](http://arxiv.org/abs/hep-th/9408162))

* {#Witten15} [[Edward Witten]], _Anomalies revisited_, talk at [Strings2015](https://strings2015.icts.res.in) ([pdf slides](https://strings2015.icts.res.in/talkDocuments/6-2.00-2.30-Edward-Witten.pdf))

and regarding the result as taking values in the determinant line over the boundary is due to

* {#DaiFreed94} [[Xianzhe Dai]] [[Daniel Freed]], _$\eta$-Invariants and Determinant Lines_, J. Math. Phys. 35 (1994),
5155&#8211;5194 and C. R. Acad. Sci. Paris (1995),
585&#8211;592 ([arXiv:hep-th/9405012](http://arxiv.org/abs/hep-th/9405012))

with review and streamlined results in

* {#Freed95a} [[Daniel Freed]], _Determinant line bundles revisited_ ([dg-ga/9505002](http://arxiv.org/abs/dg-ga/9505002))


* {#Freed95b} [[Daniel Freed]], _On determinant line bundles_, Math. aspects of [[string theory]], ed. S. T. Yau, World Sci. Publ. 1987,  ([revised pdf](http://www.math.utexas.edu/~dafr/Index/determinants.pdf))



[[!redirects eta-invariant]]
[[!redirects Eta invariant]]

[[!redirects eta invariants]]
[[!redirects eta-invariants]]
[[!redirects Eta invariants]]

[[!redirects eta function]]
[[!redirects eta functions]]

[[!redirects eta function of a self-adjoint operator]]