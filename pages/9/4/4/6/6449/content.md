
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
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

There are two kinds of higher dimensional generalizations of ordinary 3-dimensional [[Chern-Simons theory]] that are often called "higher dimensional Chern-Simons theory" in the literature. Both are special cases of [[schreiber:infinity-Chern-Simons theory]].

Recall that for $\mathfrak{g}$ a [[Lie algebra]] (not necessarily abelian) with non-generate binary [[invariant polynomial]] $\langle -,-\rangle$, the corresponding [[schreiber:infinity-Chern-Simons theory]] [[QFT]] is ordinary [[Chern-Simons theory]] in dimension 3.

But also every other [[invariant polynomial]] $\langle-,-,\cdots,-\rangle$ on $\mathfrak{g}$ induces an [[schreiber:infinity-Chern-Simons theory]], now in higher dimension. 

Moreover, every [[line Lie n-algebra]] $b^n \mathbb{R}$ carries a canonical invariant polynomial. The [[schreiber:infinity-Chern-Simons theory]] associated with that is often called _abelian higher dimensional CS theory_ .

(...)

More general "higher"-generalization of Chern-Simons theory to [[schreiber:infinity-Chern-Simons theory]] allow $\mathfrak{g}$ to be a (nonabelian) [[Lie 2-algebra]] or more generally a (nonabelian) [[L-infinity algebra]] or fully generally a [[L-infinity algebroid]].

## Higher abelian Chern-Simons theory.

### Definition

The definition of higher abelian Chern-Simons theory is simple _locally_ when certain global [[cohomology|cohomological]] effects can be ignored. We first give the simple local definition and then the full global definition.

Let $k \in \mathbb{N}$ be a [[natural number]], let $d = 4 k + 3$ and let $\Sigma$ be a [[compact space|compact]] [[smooth manifold]] of [[dimension]] $d$.

Then the _simple version_ of abelian $d$-dimensional Chern-Simons theory is defined as follows. 

* the [[configuration space]] is the [[space]] of [[differential form]]s on $\Sigma$ of degree $2k+1$

  $$
    Conf_{simpl} = \Omega^{2k+1}(\Sigma)
    \,,
  $$

* the [[Lagrangian]] is 

  $$
    L : B \mapsto B \wedge d_{dR} B
    \,,
  $$

* and the [[action functional]]

  $$
    S : \Omega^{2k+1}(\Sigma) \to \mathbb{R}
  $$

  is therefore

  $$
    S : B \mapsto \int_\Sigma B \wedge d_{dR}B
    \,.
  $$

Notice that generally for an $n$-form $B$ on a closed $(2n+1)$-dimensional manifold $\Sigma$ we have

$$
  \int_\Sigma B \wedge d_{dR} B
  =
  (-1)^{1+n + n(1+n)}
  \int_\Sigma B \wedge d_{dR} B
$$

by first using integration by parts and then switching the order of the wedge factors. Therefore this kind of action vanishes identically when $deg B$ is even. This is the reason for the above assumption that $deg B = 2k+1$ for $k \in \mathbb{N}$ and hence that the Chern-Simons theory is in dimension $4k+3$.

In the full theory instead the configuration space is 

$$
  Conf = \mathbf{H}_{diff}^{2k+2}(\Sigma)
  \,,
$$

the space of [[circle n-bundle with connection|circle (2k+1)-bundles with connection]] (given by [[cocycle]]s in degree $2k+2$ [[ordinary differential cohomology]]). This contains the above simplified configuration space as the subspace of $(2k+1)$-connections whose underlying circle $(2k+1)$-bundle is trivial. 

The action functional is given by

$$
  S : \hat B \mapsto \int_\Sigma \hat B \cup \hat B
  \,,
$$

where now the integral is [[fiber integration in ordinary differential cohomology]] and in the integrand we have the [[cup product in ordinary differential cohomology]] of differential cocycles.

(See for instance ([GT, section 4.1](#GT)), ([FMS, (1.28)](#FMS))).

### Formulation in $\infty$-Chern-Simons theory

We discuss how the above definition arises as a special case of the general notion of 
[[schreiber:infinity-Chern-Simons theory]].

These theories are defined by

* an [[L-infinity algebroid]] $\mathfrak{a}$;

* equipped with an [[invariant polynomial]] $\langle \rangle$.

The abelian higher dimensional Chern-Simons theories in dimension $4k+3$ are the special case of this general situation where

* $\mathfrak{a} = b^{2k+1}\mathbb{R}$ is the [[line Lie n-algebra|line Lie (2k+1)-algebra]], the $(2k+1)$-fold [[delooping]] of the abelian [[Lie algebra]] $\mathbb{R}$;

* $\langle - \rangle$ is the canonical quadratic [[invariant polynomial]] on this.

(...)

See ([FRS, 4.1.4](#FRS)).

### Examples

Higher dimensional abelian Chern-Simons theories appear automatically as components of systems of higher [[supergravity]], for instance in [[11-dimensional supergravity]] (they are automatically induced by the requirement of  [[local supersymmetry]] in these higher dimensional supergravity theories).

* see at _[[M5-brane]]_ the section _[Conformal blocks and 7d Chern-Simons dual](http://ncatlab.org/nlab/show/M5-brane#7dCSDual)_.

### Properties

#### Holographic relation to $4k+2$-dimensional theory

Higher Chern-Simons theory in dimension $4k+3$ is related by a [[holographic principle]] to [[self-dual higher gauge theory]] in dimension $4k+2$ (at least in the abelian case). 

* $(k=0)$: ordinary 3-dimensional [[Chern-Simons theory]] is related to a [[string]] [[sigma-model]] on its boundary;

* $(k=1)$: 7-dimensional Chern-Simons theory is related to a [[fivebrane]] model on its boundary;

* $(k=2)$: 11-dimensional Chern-Simons theory is related to a parts of a [[type II string theory]] on its bounday (or that of the space-filling 9-[[brane]], if one wishes) ([BelovMoore](#BelovMoore))


#### Background charges and square root action functionals
 {#BackgroundCharge}

The [[supergravity C-field]] is an example of a general phenomenon of 
higher abelian Chern-Simons QFTs in the presence of 
_background charge_. This phenomenon was originally noticed
in ([Witten](#Witten96)) and then made precise in 
([HopkinsSinger 05](#HopkinsSinger05)).
The holographic dual of this phenomenon is that of
self-dual higher gauge theories, which for the supergravity $C$-field
is the 2-form theory on the [[M5-brane]] -- see there for a discussion of this example. Here we discuss this effect generally, for higher abelian Chern-Simons theory in arbitrary dimension $4k+3$.


Fix some natural number $k \in \mathbb{N}$ and an [[orientation|oriented]] [[manifold]]
([[compact topological space|compact]] [[manifold with boundary|with boundary]]) $X$ of [[dimension]] $4 k + 3$. 
The gauge equivalence class of a $(2k+1)$-form gauge field $\hat G$ on $X$ is an element in the [[ordinary differential cohomology]] group $\hat H^{2k+2}(X)$.
The [[cup product]] $\hat G \cup \hat G \in \hat H^{4k+4}(X)$ of this with itself  has a natural [[higher holonomy]] over $X$, denoted
$$
  \exp(i S (-)) : \hat H^{2k+2}(X) \to U(1)
$$
$$
  \hat G \mapsto \exp(i \int_X \hat G \cup \hat G)
  \,.
$$
This is the exponentiated [[action functional]] for bare $(4k+3)$-dimensional
abelian Chern-Simons theory, as discussed above. 

Observe now that
the above action functional may be regarded as a 
_[[quadratic form]]_ on the [[cohomology group]] 
$\hat H^{2k+2}(X)$. The corresponding [[bilinear form]] is the 
("[[secondary characteristic class|secondary]]", 
since $X$ is of dimension $4k+3$ instead of $4k+4$)
_[[intersection pairing]]_

$$
  \langle -,-\rangle : \hat H^{2k+2}(X) \times \hat H^{2k+2}(X) \to U(1)
$$
$$
  (\hat a_1 , \hat a_2) \mapsto \exp(i \int_X \hat a_1 \cup \hat a_2 )
  \,.
$$

But note that from $\exp(i S(-))$ we do _not_ obtain a 
_[[quadratic refinement]]_  
of the pairing. A quadratic refinement is, by definition, a function
$$
  q : \hat H^{2k+2}(X) \to U(1)
$$
(not necessarily homogenous of degree 2 as $\exp(i S(-))$ is), such that
the [[intersection pairing]] is reobtained from it by the polarization formula
$$
  \langle \hat a_1, \hat a_2\rangle 
    = 
  q(\hat a_1 + \hat a_2)
  q(\hat a_1)^{-1}
  q(\hat a_2)^{-1}
  q(0)
  \,.
$$
If we took $q := \exp(i S(-))$, then the above formula would yield not 
$\langle -,-\rangle$, but the square $\langle -,-\rangle^2$, given by
(the exponentiation of) _twice_ the integral. 

The observation in ([Witten96](#Witten96)) was 
that for the correct [[holographic principle|holographic]] physics, we need instead an action functional
which is indeed a genuine [[quadratic refinement]] of the [[intersection pairing]].

But since the [[differential cohomology|differential classes]] in $\hat H^{2k+2}(X)$ refine 
_[[integral cohomology]]_, we cannot in general simply divide by 2 and
pass from $\exp( i \int_X \hat G \cup \hat G)$ to 
$\exp( i  \int_X \frac{1}{2} \hat G \cup \hat G)$. The integrand in the
latter expression does not make sense in general in differential cohomology.
If one tried to write it out in the "obvious" local formulas one would
find that it is a functional on fields which is not 
[[gauge invariance|gauge invariant]].
The analog of this fact is familiar from nonabelian $G$-[[Chern-Simons theory]]
with [[simply connected space|simply connected]] $G$, where also the theory is consistent only at 
interger _levels_. The "level" here is nothing but the 
underlying integral class $G \cup G$. 


Therefore the only way to obtain a [[square root]] of the [[quadratic form]]
$\exp(i S(-))$ is to _shift its origin_. Here we think of 
the analogy with a
quadratic form $q : x \mapsto x^2$ on the [[real numbers]] (a parabola in the plane).
Replacing this by $q^{\lambda} : x \mapsto x^2 + \lambda x$ for some real number
$\lambda$ means keeping the shape of the form, but shifting its [[minimum]] from 0 to
$-\frac{1}{2}\lambda$. If we think of this as the potential term for a scalar field
$x$ previously with rotation-symmetric dynamics about $x = 0$, then the new potential
exhibits [[spontaneous symmetry breaking]]: its ground state is now at $x = -\frac{1}{2}\lambda$
(and has [[energy]] $-\frac{1}{4}\lambda^2$ there). We may say that there is
a _background field_ or _background [[charge]]_ that pushes
the field out of its free equilibrium.

To lift this reasoning to our action quadratic form 
$\exp(i S(-))$ on differential cocycles, we need a 
differential class $\hat \lambda \in H^{2k+2}(X)$ such that 
for every $\hat a \in H^{2k+2}(X)$ the composite class
$$
  \hat a \cup \hat a + \hat a \cup \hat \lambda
  \in 
  H^{4k+4}(X)
$$
is even, hence is divisible by 2. Because then we could define a shifted
action functional

$$
  \exp(i S^\lambda(-)) : \hat a \mapsto \exp(i \int_X \frac{1}{2}(\hat a \cup \hat a + \hat a \cup \hat \lambda))
  \,,
$$

where now the fraction $\frac{1}{2}$ in the integrand does make sense. One directly
sees that if this exists, then this shifted action is indeed now a
[[quadratic refinement]] of the [[intersection pairing]]

$$
  \exp(i S^\lambda(\hat a + \hat b))
  \exp(i S^\lambda(\hat a))^{-1}
  \exp(i S^\lambda(\hat b))^{-1}
  \exp(i S^\lambda(0)
  = 
  \exp(i \int_X \hat a \cup \hat b))
  \,.
$$

The condition on the existence of $\hat \lambda$ here means equivalently that the
image of the underlying integral class in cohomology with coefficients
in $\mathbb{Z}_2$ vanishes:
$$
   (a)_{\mathbb{Z}_2} \cup (a)_{\mathbb{Z}_2} 
     + 
   (a)_{\mathbb{Z}_2} \cup (\lambda)_{\mathbb{Z}_2}  
   = 
   0 \in H^{4k+4}(X, \mathbb{Z}_2)
  \,,
$$

Precisely such a class $(\lambda)_{\mathbb{Z}_2}$ does uniquely exist on 
every oriented manifold. It is called the _[[Wu class]]_ 
$\nu_{2k+2} \in H^{2k+2}(X,\mathbb{Z}_2)$, and may be _defined_ by this condition.
Moreover, if $X$ is a [[spin structure|Spin-manifold]], then every second
[[Wu class]], $\nu_{4k}$, has a pre-image in [[integral cohomology]], 
hence $\lambda$ does exist as required above

$$
  (\lambda)_{\mathbb{Z}_2}
    = 
  \nu_{2k+2}
  \,.
$$

It is given by  [[polynomials]] in the [[Pontryagin classes]] of $X$. For instance
the degree-4 Wu class (for $k = 1$) is refined by the 
[[first fractional Pontryagin class]]
$\frac{1}{2}p_1$

$$
  (\frac{1}{2}p_1)_{\mathbb{Z}_2} = \nu_4
  \,.
$$

This was the original observation in [Witten96, around (3.3)](#Witten96).

Notice that the [[equations of motion]] of the shifted action $\exp(i S^\lambda(\hat a))$
are no longer $F_a = 0$, but are now $F_a = - \frac{1}{2}F_\lambda$.
Comparing this to the [[Maxwell equations]], we see that $-\frac{1}{2}\hat \lambda$
here plays the role of a _background [[charge]]_ (or rather, of the
_background [[current]]_ that underlies a background charge). We therefore think of
$\exp(i S^\lambda(-))$ as the exponentiated action functional for
_higher dimensional abelian Chern-Simons theory with background charge 
$-\frac{1}{2}\lambda$_.


This of course only makes sense if $X$ is such that 
$\lambda$ is further divisible by 2, which we will
assume now. In ([Hopkins-Singer 05](#HopkinsSinger05)) is discussed a way to
make sense of the further division in general if one passes to a certain notion of  twisted differential cohomology. One can also adopt a different perspective and interpret the condition that $\frac{1}{2}p_1$ is further divisible by 
2 precisely as a $\mathrm{String}^{2a}$-structure
([SSS3](http://ncatlab.org/schreiber/show/Twisted+Differential+String+and+Fivebrane+Structures)). This is a higher analog
of a [[Spin^c structure]].


With respect to the shifted action functional it makes sense to introduce the
shifted field

$$
  \hat G  := \hat a  + \frac{1}{2}\lambda
  \,.
$$

This is simply a re-parameterization such that the 
Chern-Simons equations of motion again look homogenous, namely $FieldStrength(\hat G) = 0$.
In terms of this shifted field the action $\exp(i S^\lambda(\hat a))$
from above equivalently reads

$$
  \exp(i S^\lambda(\hat G)) = 
  \exp(
    i \int_X \frac{1}{2}(\hat G \cup \hat G - (\frac{1}{2}\hat \lambda)^2)
  )
  \,.
$$

This is the form of the action functional first given as ([Witten96 (3.6)](#Witten96)) in for the case $k = 1$.


In the language of [[twisted differential c-structures]], we may summarize this sitation
as follows: 

in order for the action functional of higher abelian Chern-Simons theory 
to be correctly divisible, the images of the fields in $\mathbb{Z}_2$-cohomology
need to form a [[twisted Wu structure]]. Therefore the fields themselves
need to constitute a _twisted $\lambda$-structure_. For $k = 1$ this is
a [[twisted differential string structure|twisted string structure]] and explains for instance the quantization
condition on the [[supergravity C-field]] in [[11-dimensional supergravity]]. For that case see also the corresponding discussion at _[[M5-brane]]_.


## Higher-dimensional non-abelian CS theory

Chern-Simons actions for [[Lie algebra]]s $\mathfrak{g}$ but with higher-degree [[invariant polynomial]]s have in particular received attention for $\mathfrak{g} = \mathfrak{siso}$ the [[super Poincare Lie algebra]]. In this case these action functionals can be regarded as defining higher [[Chern-Simons supergravity]].

### 1d Chern-Simons theory

* [[1d Chern-Simons theory]]

### 2d Chern-Simons theory

* [[2d Chern-Simons theory]]

  * [[Poisson sigma-model]]

### 3d Chern-Simons theory

* [[3d Chern-Simons theory]]

  * [[Chern-Simons theory]]

  * [[Dijkgraaf-Witten model]]

  * [[Courant sigma-model]]

### 4d Chern-Simons theory

* [[4d Chern-Simons theory]]

  * [[Yetter model]]

### 5d Chern-Simons theory

* [[5d Chern-Simons theory]]

### 6d Chern-Simons theory

* [[6d Chern-Simons theory]]

### 7d Chern-Simons theory

* [[7d Chern-Simons theory]]

### 11d Chern-Simons theory

* [[11d Chern-Simons theory]]

### Infinite-dimensional Chern-Simons theory

* [[infinite-dimensional Chern-Simons theory]]

### AKSZ $\sigma$-models

* [[AKSZ sigma-model]]

### String field theory

* [[string field theory]]




## Related concepts

* [[Wu classes]]

* [[schreiber:infinity-Chern-Simons theory]]

  * [[Chern-Simons theory]]

  * **higher dimensional Chern-Simons theory**

    * [[Chern-Simons gravity]]

  * [[AKSZ sigma-model]]

    * [[Poisson sigma model]]

      * [[A-model]], [[B-model]]

    * [[Courant sigma-model]]

      * [[Chern-Simons theory]]

  * [[1-dimensional Chern-Simons theory]]

* [[higher dimensional WZW models]]

## References

### General

For higher dimensional non-abelian Chern-Simons theory see for instance 

* M&#225;ximo Ba&#241;ados, _Higher dimensional Chern-Simons theories and black holes_ ([pdf](http://worldscibooks.com/etextbook/4388/4388_chap01.pdf))

* M&#225;ximo Ba&#241;ados, Luis Garay, [[Marc Henneaux]], _Existence of local degrees of freedom for higher dimensional pure Chern-Simons theories_ Phys. Rev. D 53, R593&#8211;R596 (1996)  ([pdf](http://prd.aps.org/pdf/PRD/v53/i2/pR593_1))

* M&#225;ximo Ba&#241;ados, Luis Garay, [[Marc Henneaux]], _The dynamical structure of higher dimensional Chern-Simons theory_ ([arXiv:hep-th/9605159](http://arxiv.org/abs/hep-th/9605159))

* G Giachetta, L Mangiarotti, G Sardanashvily, _Noether conservation laws in higher-dimensional Chern-Simons theory_ Modern Physics Letters A Volume 18(2003) ([pdf](http://gnsardan.appfarm.ru/a84.pdf))

* Danhua Song, Mengyao Wu, Ke Wu, Jie Yang, *Higher Chern-Simons based on (2-)crossed modules*, JHEP **2023** 207 (2023) &lbrack;[arXiv:2212.04667](https://arxiv.org/abs/2212.04667), <a href="https://link.springer.com/article/10.1007/JHEP07(2023)207">doi:10.1007/JHEP07(2023)207</a>&rbrack;


### Formulation in differential cohomology

For the formulation of abelian Chern-Simons theory by fiber integration over cup products in [[ordinary differential cohomology]] see

* Enore Guadagnini, Frank Thuillier, _Deligne-Beilinson cohomology and abelian links invariants_ SIGMA 4 (2008), 078, 30 ([arXiv:0801.1445](http://arxiv.org/abs/0801.1445))
  {#GT}

* R. Floreanini, R. Percacci, _Higher dimensional abelian Chern-Simons theory_ Physics Letters B Volume 224, Issue 3, 29 (1989)

* [[Daniel Freed]], [[Gregory Moore]], [[Graeme Segal]], _The Uncertainty of Fluxes_ ([arXiv:hep-th/0605198](http://arxiv.org/abs/hep-th/0605198))
  {#FMS}

### Relation to self-dual theories

The idea of describing [[self-dual higher gauge theory]] by abelian Chern-Simons theory in one dimension higher originates in 

* [[Edward Witten]], _Five-Brane Effective Action In M-Theory_ Journal of Geometry and Physics, Volume 22, Issue 2, May 1997, Pages 103-133  ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))
 {#Witten96}

(there for the [[6d (2,0)-susy QFT]] on the [[fivebrane]]) and

* [[Edward Witten]], _Duality Relations Among Topological Effects In String Theory_ ([arXiv:hep-th/9912086](http://arxiv.org/abs/hep-th/9912086))

Motivated by this the [[differential cohomology]] of self-dual fields had been discussed in 

* {#HopkinsSinger05} [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_, 2005
 

More discussion of the general principle is in 

* Dmitriy Belov, [[Greg Moore]], _Holographic Action for the Self-Dual Field_ ([arXiv:hep-th/0605038](http://arxiv.org/abs/hep-th/0605038))


The application of this to the description of 
[[type II string theory]] in 10-dimensions to [[schreiber:infinity-Chern-Simons theory|11-dimensional Chern-Simons theory]] is in the followup 

* Dmitriy Belov, [[Greg Moore]], _Type II Actions from 11-Dimensional Chern-Simons Theories_ ([arXiv:hep-th/0611020](http://arxiv.org/abs/hep-th/0611020))
 {#BelovMoore}

### Higher Chern-Simons (super)gravity

There are various discussions identifying or conjecturing higher dimensional Chern-Simons theories as parts of or related to [[gravity]] and [[supergravity]]. 

An original articles includes

* M&#225;ximo Ba&#241;ados, Ricardo Troncoso, Jorge Zanelli, _Higher dimensional Chern-Simons supergravity_ Phys. Rev. D 54, 2605&#8211;2611 (1996) ([pdf](http://cdsweb.cern.ch/record/293524/files/9601003.pdf))

An introduction and survey is in 

* Jorge Zanelli, _Lecture notes on Chern-Simons (super-)gravities_ ([arXiv:hep-th/0502193](http://arxiv.org/abs/hep-th/0502193))

For more references see at

* _[[Chern-Simons gravity]]_ .


### Higher Chern-Simons invariants
 {#ReferencesInvariants}

* F. Thuillier, _Deligne-Beilinson cohomology and abelian link invariants: torsion case_ J. Math. Phys. 50, 122301 (2009)

* B. Broda, _Higher-dimensional Chern-Simons theory and link invariants_ Physics Letters B Volume 280, Issues 3-4, 30 (1992) Pages 213-218 

* L. Gallot, E. Pilon, F. Thuillier, _Higher dimensional abelian Chern-Simons theories and their link invariants_ ([arXiv:1207.1270](http://arxiv.org/abs/1207.1270))

### Formulation in $\infty$-Chern-Simons theory

Below (5.11) of ([Hopkins-Singer 05](#HopkinsSinger05)).

Section 4.1.4 of

* {#FRS} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher Chern-Weil Derivation of AKSZ Sigma-Models]]_
 

Section 4.4 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

### Boundary theories

Boundary [[higher dimensional WZW models]] for nonabelian [[higher dimensional Chern-Simons theory]] are discussed in

* J. Gegenberg , G. Kunstatter, _Boundary Dynamics of Higher Dimensional Chern-Simons Gravity_ ([arXiv:hep-th/0010020](http://arxiv.org/abs/hep-th/0010020))

* J. Gegenberg , G. Kunstatter, _Boundary Dynamics of Higher Dimensional AdS Spacetime_ ([arXiv:http://arxiv.org/abs/hep-th/9905228](http://arxiv.org/abs/hep-th/9905228))



[[!redirects higher Chern-Simons theory]]
[[!redirects higher Chern-Simons theories]]

[[!redirects higher dimensional Chern-Simons theories]]
