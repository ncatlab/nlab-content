
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
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For a suitable [[linear operator]] $H$ (say on [[section]] of a [[line bundle]] over a [[Riemann surface]]), its _zeta function_ is the [[analytic continuation]] of the [[trace]]

$$
  \zeta_H(s) \coloneqq Tr(H^{-s})
$$

of the $-s$ power of $H$, which, if $H$ is suitably self-adjoint, is
the [[sum]] of the $-s$-powers of all its [[eigenvalues]], as a function of $s$. This is analogous to the _[[Riemann zeta function]]_ and the [[Dedekind zeta function]] (or would be if there were something like a [[Laplace operator]] on [[Spec(Z)]] or more generally on an [[arithmetic curve]], see at _[[function field analogy]]_).

The exponential of the derivative of the zeta function at $n = 0$ also encodes the [[functional determinant]] of $H$, a [[regularization (physics)|regularized]] version ("[[zeta function regularization]]") of the naive and generally ill-defined product of all eigenvalues. As such, zeta functions play a central role in [[quantum field theory]].

Generally, the values of $\zeta_H(s)$ of interest in [[physics]] (when regarding $H$ as a [[Hamilton operator]]) are those for (low) integral $s$. These are just the _[[special values of L-functions]]_.

## Definition

### The zeta function

Given an [[elliptic differential operator]] with positive lower bound $c$,  write $H$ for its [[self-adjoint extension]] and write 

$$
  0 \lt \lambda_1 \leq \lambda_2 \leq \cdots
$$

for its [[eigenvalues]].

+-- {: .num_defn #ZetaBySeries}
###### Definition

The _zeta function_ of $H$ is the [[holomorphic function]] defined by the [[series]]

$$
  \begin{aligned}
    \zeta_H(s) 
    & \coloneqq 
    Tr( H^{-s} )
    \\
    & \coloneqq
    \underoverset{n = 1}{\infty}{\sum} \frac{1}{(\lambda_n)^s}
  \end{aligned}
  \,.
$$

where this [[convergence|converges]] and then extended by [[analytic continuation]].

=--

(e.g. ([Duistermaat-Guillemin 75 (2.13)](#DuistermaatGuillemin75), [Berline-Getzler-Vergne 04, section 9.6](#BerlineGetzlerVergne04) ) ).

### Functional determinant and zeta-function regularization
 {#FunctionalDeterminant}

Notice that the first [[derivative]] $\zeta^\prime_H$ of this zeta function is, where the original series converges, given by

$$
  \zeta_H^\prime(s)
  =
  \sum_{n = 1}^\infty \frac{- \ln \lambda_n}{ (\lambda_n)^s}
  \,.
$$



Therefore one says ([Ray-Singer 71](#RaySinger71)) that the _[[functional determinant]]_ of $H$ is the exponential of the derivative of zeta function of $H$ at 0:

$$
  det_{reg} H
  \coloneqq
  \exp(- \zeta_H^\prime(0))
  \,.
$$

Via the [[analytic continuation]] involved in defining $\zeta_H(0)$ in the first place, this may be thought of as a _[[regularization (physics)|regularization]]_ of the ill-defined  naive definition "$\prod_n \lambda_n$" of the [[determinant]] of $H$. As such functional determinants often appear in [[quantum field theory]] as what is called _[[zeta function regularization]]_.

Conversely, the [[logarithm]]

$$
  Z \coloneqq - \frac{1}{2}\zeta_H^\prime(0) = \tfrac{1}{2} log\,det_{reg} H
$$

is what is called the _[[vacuum energy]]_ in [[quantum field theory]] (for $H^{-1}$ the [[Feynman propagator]]).
 
If $H = D^2$ has a square root $D$ (a [[Dirac operator]]-type square root as in [[supersymmetric quantum mechanics]]) then under some conditions on the growth of the eigenvalues, then the functional determinant may also be expressed in terms of the [[eta function]] of $D$ as

$$
  det H 
  =
  det (D^2) 
   = 
  \exp( \frac{\partial}{\partial s}\frac{\partial}{\partial c} \eta_{D}(0))
  \,.
$$

See at _[eta invariant -- Relation to zeta function](eta+invariant#RelationToTheZetaFunction)_ for more on this.

### Relation to partition functions and number-theoretic zeta/theta functions 
 {#AnalogyWithNumberTheoreticZetaFunctions}

By basic [[integration]] identities we have that

+-- {: .num_prop #IntegralKernelExpression}
###### Proposition

The series expression in def. \ref{ZetaBySeries} is equal to the [[Mellin transform]] of the [[partition function]]

$$
    \zeta_H(s)
     =
     \int_{(0,\infty)}
     t^{s-1}
     \left(
        \underset{\lambda_k \neq 0}{\sum}
        \exp(-t \lambda_k)
     \right)
     d t
  \,.
$$

=--

(see e.g. [Quine-Heydari-Song 93 (8)](#QuineHeydariSong93), [Richardson, pages 8-9](#Richardson), [BCEMZ 03, section A.2](#BCEMZ03), [Connes-Marcolli 06, theorem 13.11](#ConnesMarcolli06)).

+-- {: .num_remark}
###### Remark

If one thinks of the operation $H$ as a [[Hamiltonian]] of a [[quantum mechanical system]], then the term

$$
  Tr(\exp(-\beta H))
  \coloneqq
   \underset{\lambda_k \neq 0}{\sum}
        \exp(-\beta \lambda_k)
   + 1
$$

is the _[[partition function]]_ of this system. Accordingly, prop. \ref{IntegralKernelExpression} says that the zeta function of $H$ is obtained from its partition function by

$$
  \zeta_H(s)
  =
   \int_{(0,\infty)}
     \beta^{s-1}
     \;
     \left(Tr(\exp(-\beta H)) - 1 \right)
     \;
   d \beta 
   \,.
$$

=--


Further, by a change of integration variable $t\coloneqq x^2$ 
in the expression in prop. \ref{IntegralKernelExpression} 
one obtains

+-- {: .num_prop #IntegralKernelExpressionInSquares}
###### Proposition

The series expression in def. \ref{ZetaBySeries} is equal to

$$
  \begin{aligned}
     \zeta_H(s)
     & =
     2
     \int_{(0,\infty)}
     x^{2s-1}
     \left(
        \underset{\lambda_k \neq 0}{\sum}
        \exp(- x^2 \lambda_k)
     \right)
      d x      
  \end{aligned}
 \,.
$$

In particular if $H = D^2$ is the square of a [[Dirac operator]]/[[supersymmetric quantum mechanics]]-type square root operator $D$ with [[eigenvalues]] $\pm \alpha_k$,then $\lambda_k = \alpha_k^2$ and hence in this case the series is

$$
  \begin{aligned}
     \zeta_H(s)
     & =
     2
     \int_{(0,\infty)}
     x^{2s-1}
     \left(
        \underset{\alpha_k \neq 0}{\sum}
        \exp(- (x \alpha_k)^2)
     \right)
      d x      
  \end{aligned}
 \,.
$$


=--


By comparison one observes:

+-- {: .num_remark}
###### Remark


The integral expression in prop. \ref{IntegralKernelExpressionInSquares}
is analogous to the expression of [[zeta functions]] in [[number theory]]/[[arithmetic geometry]] as integrals of a [[theta function]] (for instance discussed [here](Riemann%20zeta%20function#RelationToThetaFunctions) for the [[Riemann zeta function]])

$$
  \hat\zeta_f(2 s)
  = 
  \int_{(0,\infty)} (\theta(x^2) - 1) x^{2s-1} d x
  \,.
$$

Under this analogy the [[theta function]] in the case of the differential operator $H$ is

$$
  \theta_H(x)
   \coloneqq  
   \underset{\lambda_k \neq 0}{\sum}
        \exp(- x \lambda_l)
   \,.
$$

This is formally the same definition as that of adelic theta functions (e.g.[Garrett 11, section 1.8](Iwasawa-Tate%20theory#Garrett11))

=--


+-- {: .num_remark}
###### Remark

The [[determinant line bundle]] of the [[functional determinant]] of the [[Dirac operator]] on a [[complex torus]] is a complex-analytic [[theta function]] as above, quotiented by the [[Dedekind eta function]]. 

Early references explaining this include [Alvarez-Gaum&#233; & Moore & Vafa 86](#AlvaresGaumeMooreVafa86), [Alvarez-Gaum&#233; & Bost & Moore & Nelson & Vafa 87](#AlvaresGaumeBostMooreNelsonVafa87). In a bigger perspective, this relation plays a central role in the general discussion of [[self-dual higher gauge theory]] ([Witten 96](self-dual%20higher%20gauge%20theory#Witten96)).

=--

## Examples

### Of Laplace operator on complex torus and Dedekind eta function

For $\mathbb{C}/(\mathbb{Z}\oplus \tau \mathbb{Z})$
a [[complex torus]] (complex [[elliptic curve]]) equipped with its
standard flat [[Riemannian metric]], then the [[zeta function of an elliptic differential operator|zeta function]] of the corresponding [[Laplace operator]] $\Delta$ is

$$
  \zeta_{\Delta} = (2\pi)^{-2 s} E(s)
   \coloneqq
   (2\pi)^{-2 s} \underset{(k,l)\in \mathbb{Z}\times\mathbb{Z}-(0,0)}{\sum}
  \frac{1}{{\vert k +\tau l\vert}^{2s}}
  \,.
$$

The corresponding [[functional determinant]] is

$$
  \exp(
    E^\prime_{\Delta}(0)
  )
  = (Im \tau)^2 {\vert \eta(\tau)\vert}^4
  \,,
$$

where $\eta$ is the [[Dedekind eta function]]. 

(recalled e.g. in [Todorov 03, page 3](#Todorov03))


For more see also at _[[zeta function of a Riemann surface]]_.

### Analytic torsion

The functional determinant of a [[Laplace operator]] of a [[Riemannian manifold]] acting on [[differential n-forms]] is up to a sign in the exponent a factor in what is called the _[[analytic torsion]]_ of the manifold.

## Related concepts

* [[partition function]]

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

## References

### General

An early reference is

* {#DuistermaatGuillemin75} [[Hans Duistermaat]], [[Victor Guillemin]], _The Spectrum of Positive Elliptic Operators and Periodic Bicharacteristics_,Inventiones mathematicae (1975) Volume: 29, page 39-80 ([EuDML](https://eudml.org/doc/142329))

 (see also at _[[Duistermaat-Guillemin trace formula]]_)

Textbook accounts include

* {#BerlineGetzlerVergne04} [[Nicole Berline]], [[Ezra Getzler]], [[Michèle Vergne]], section 9.6 of _Heat Kernels and Dirac Operators_

Review includes

* {#Richardson} [[Ken Richardson]], section 3 of _Introduction to the Eta invariant_ ([pdf](http://faculty.tcu.edu/richardson/Seminars/etaInvariant.pdf))

* {#QuineHeydariSong93} J. R. Quine, S. H. Heydari, R. Y. Song, _Zeta regularized products_, Transactions of the AMS volume 338, number 1, 1993 ([[QuineZetaRegularization.pdf:file]])

* Wikipedia, _[Functional determinant -- Zeta function version](http://en.wikipedia.org/wiki/Functional_determinant#Zeta_function_version)_

* Wikipedia, _[Zeta function regularization](http://en.wikipedia.org/wiki/Zeta_function_regularization)_

* {#ConnesMarcolli06} [[Alain Connes]], [[Matilde Marcolli]], _A walk in the noncommutative garden_ ([arXiv:0601054](http://arxiv.org/abs/math/0601054))

### Zeta function regularization

* {#Speer71} [[Eugene Speer]], _On the structure of Analytic Renormalization_, Comm. math. Phys. 23, 23-36 (1971) ([Euclid](http://projecteuclid.org/euclid.cmp/1103857549))

* {#BCEMZ03} A. Bytsenko, G. Cognola, [[Emilio Elizalde]], [[Valter Moretti]], S. Zerbini, section 2 of _Analytic Aspects of Quantum Fields_, World Scientific Publishing, 2003, ISBN 981-238-364-6

### Functional determinant

The definition of a _[[functional determinant]]_ via the exponential of the derivative of the zeta function at 0 originates in

* {#RaySinger71} D. Ray, [[Isadore Singer]], _R-torsion and the Laplacian on Riemannian manifolds_, Advances in Math. 7: 145&#8211;210, (1971) doi:10.1016/0001-8708(71)90045-4, MR 0295381


Discussion in the special case of [[2d CFT]] ([[worldsheet]] [[string theory]]) is in 


* {#AlvaresGaumeMooreVafa86} [[Luis Alvarez-Gaumé]], [[Gregory Moore]], [[Cumrun Vafa]], _Theta functions, modular invariance, and strings_, Communications in Mathematical Physics Volume 106, Number 1 (1986), 1-4 ([Euclid](http://projecteuclid.org/euclid.cmp/1104115581))

* {#AlvaresGaumeBostMooreNelsonVafa87} [[Luis Alvarez-Gaumé]], [[Jean-Benoit Bost]], [[Gregory Moore]], Philip Nelson, [[Cumrun Vafa]], _Bosonization on higher genus Riemann surfaces_, Communications in Mathematical Physics, Volume 112, Number 3 (1987), 503-552 ([Euclid](http://projecteuclid.org/euclid.cmp/1104159982))

* {#Todorov03} [[Andrey Todorov]], _The analogue of the Dedekind eta function for CY threefolds_, 2003 [pdf](http://www.ma.huji.ac.il/conf/crelle.pdf)


[[!redirects zeta functions of elliptic differential operators]]
