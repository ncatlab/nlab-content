
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

What is called _Wick rotation_ (after [[Gian-Carlo Wick]]) is a method in [[physics]] for finding a construction in [[relativistic field theory]] on [[Minkowski spacetime]] or, more generally, on [[Lorentzian manifolds]], from a related construction in [[Euclidean field theory]] on [[Riemannian manifolds]] in a way that involves or generalizes the idea of [[analytic continuation]] for the _[[time]]_ [[coordinates]]. 

<center>
<img src="https://ncatlab.org/nlab/files/WickRotation.jpg" width="400">
</center>

> The [[complex plane]] for a complexified [[time]] [[coordinate]] $t + i s$. After Wick rotation it is the [[imaginary part]] $s$ that replaces the "[[real part|real]]" time $t$.

>  graphics grabbed from [Fulling-Ruijsenaars 87](#FullingRuijsenaars87)


This is motivated by the observation that the [[Minkowski metric]] (with the $(-1,1,1,1)$ convention for [[spacetime signature]]) and the four-Euclidean metric are equivalent if the [[time]] components of either are allowed to have [[imaginary part|imaginary]] values. Hence Wick rotation, when it applies, involves [[analytic continuation]] of [[n-point functions]] to [[complex number|complex valued]] [[time]] [[coordinates]].

For [[relativistic field theory|relativistic]]/[[Euclidean field theory|Euclidean]] [[quantum field theory]] on [[Minkowski spacetime]] $\mathbb{R}^{d,1}$/[[Euclidean space]] $\mathbb{R}^{d+1}$ Wick rotation is rigorously understood and takes the form of a [[theorem]] relating the [[Wightman axioms]] for [[n-point functions]] in [[relativistic field theory]] to the _[[Osterwalder-Schrader axioms]]_ for [[correlators]] in [[Euclidean field theory]]. 

See for instance [Fulling-Ruijsenaars 87, section 2](#FullingRuijsenaars87) for a clear account.

More generally, in this context Wick rotation applies to relativistic field theory in [[thermal equilibrium]] [[states]] at [[positive number|positive]] [[temperature]] $T$ ("[[KMS states]]"), and then relates this to [[Euclidean field theory]] with compact/periodic Euclidean time of length $\beta = 1/T$ (see [Fulling-Ruijsenaars 87, section 3](#FullingRuijsenaars87)):

$$
  \array{
  \left.
  \array{
     \text{relativistic field theory}
     \\
     \text{on Minkowski spacetime}
     \\
     \mathbb{R}^{d,1}
     \\
     \text{in a thermal equilibrium state}
     \\
     \text{at temperature}\; T
  }
  \right\}
  &
  \;\;\;\;
  \overset{ \text{Wick rotation} }{\leftrightarrow}
  \;\;\;\;
  &
  \left\{
  \array{
    \text{Euclidean field theory}
    \\
    \text{on Euclidean space}
    \\
    \mathbb{R}^d \times S^1_{\beta}
    \\
    \text{with compact/periodic Euclidean time}
    \\
    \text{of length} \; \beta = 1/T
  }
  \right.
  \\
  \phantom{A}
  \\
  \underset{
    {
    \text{equal-time n-point function} 
    \atop 
    \text{of relativistic fields}
    }
    \atop
    \text{ in thermal equilibrium state } \; \vert T\rangle
  }{
  \underbrace{
    \left\langle  T\vert  :\mathbf{\Phi}(x_1,t) \mathbf{\Phi}(x_2,t) \cdots \mathbf{\Phi}(x_n,t) : \vert T \right\rangle_{\mathbb{R}^{d,1}}
  }}
  &\;=\;&
  \underset{
    \text{correlator of Euclidean fields}
    \atop
    \text{ for "Euclidean time" of periodicity}\; \beta = 1/T
  }{
  \underbrace{
  \left\langle 0 \vert \mathbf{\Phi}(x_1,t) \mathbf{\Phi}(x_2,t) \cdots \mathbf{\Phi}(x_n,t)  \vert 0 \right\rangle_{\mathbb{R}^{d} \times S^1_{\beta}}
  }}
  }
$$


In this form, Wick rotation is also known as _[[thermal quantum field theory]]_. See there for more.


<center>
<img src="https://ncatlab.org/nlab/files/EuclideanTime.jpg" width="580">
</center>

> graphics grabbed form [Frolov-Zelnikov 11](#FrolovZelnikov11)

Wick rotation also applies on suitable [[black hole]]-[[spacetimes]] spring
thermodynamics, such as the [[Bekenstein-Hawking entropy]], find elegant explanations, at least at the level of the manipulation of formulas (see e.g. [Fulling-Ruijsenaars 87, section 4](#FullingRuijsenaars87)). 

### Example

Consider the Minkowski metric with the $-1,1,1,1$ convention for the tensor:

$d s^{2}= -(d t)^{2} + (d x)^{2} + (d y)^{2} + (d z)^{2}$

and the four-dimensional Euclidean metric:

$d s^{2}= d \tau^{2} + (d x)^{2} + (d y)^{2} + (d z)^{2}$.

Notice that if $d t = i\cdot d \tau$, the two are equivalent.

### Method

A typical method for employing Wick rotation would be to make the substitution $t=i\tau$ in a problem in Minkowski space.  The resulting problem is in Euclidean space and is sometimes easier to solve, after which a reverse substitution can (sometimes) be performed, yielding a solution to the original problem.

Technically, this works for any four-vector comparison between Minkowski space and Euclidean space, not just for space-time intervals.

## Related concepts

* [[reflection positivity]]

## References


Wick rotation between [[relativistic field theory]] in terms of [[Wightman axioms]] for [[n-point functions]] on [[Minkowski spacetime]] and [[Euclidean field theory]] in terms of [[Osterwalder-Schrader axioms]] for [[correlators]] on [[Euclidean space]] is due to 

* {#OsterwalderSchrader73} [[Konrad Osterwalder]], [[Robert Schrader]], _Axioms for Euclidean Green's functions_, Comm. Math. Phys. Volume 31, Number 2 (1973), 83-112 ([Euclid:1103858969](https://projecteuclid.org/euclid.cmp/1103858969))

The generalization of this for [[positive number|positive]] [[thermal equilibrium]] [[vacuum states]], relating to [[thermal quantum field theory]] with compact/periodic Euclidean time is discussed in

* {#KleinLandau81} Abel Klein, Lawrence Landau, _Periodic Gaussian Osterwalder-Schrader positive processes and the two-sided Markov property on the circle_, Pacific Journal of Mathematics, Vol. 94, No. 2, 1981 ([
DOI: 10.2140/pjm.1981.94.341](https://msp.org/pjm/1981/94-2/p12.xhtml), [pdf](https://msp.org/pjm/1981/94-2/pjm-v94-n2-p12-s.pdf))

The idea here apparently goes back to 

* {#Bloch58} Claude Bloch, _Sur la détermination de l'état fondamental d'un système de particules_,  Nucl. Phys. 7 (1958) 451

This has maybe first been made precise, for the case of 1+1 dimensions, in 

* {#HoeghKrohn74} [[Raphael Høegh-Krohn]], _Relativistic Quantum Statistical Mechanics in two-dimensional Space-Time_, Communications in Mathematical Physics 38.3 (1974): 195-224 ([pdf](https://www.duo.uio.no/bitstream/handle/10852/44072/1973-22.pdf))

Good review on the relation to [[thermal quantum field theory]] and [[black hole thermodynamics]] is in

* {#FullingRuijsenaars87} S.A. Fulling, S.N.M. Ruijsenaars, _Temperature, periodicity and horizons_, Physics Reports Volume 152, Issue 3, August 1987, Pages 135-176 ([pdf](https://www1.maths.leeds.ac.uk/~siru/papers/p26.pdf), <a href="https://doi.org/10.1016/0370-1573(87)90136-0">doi:10.1016/0370-1573(87)90136-0</a>)

* {#GibbonsPerry78} [[Gary Gibbons]], Malcolm J. Perry, _Black Holes and Thermal Green Functions_, Vol. 358, No. 1695 (1978) ([jstor:79482](https://www.jstor.org/stable/79482))

Discussion of thermal Wick rotation on global [[anti-de Sitter spacetime]] (which is already periodic in _real_ time) is in

* {#AllenFolacciGibbons87} B. Allen, A. Folacci, [[Gary Gibbons]], _Anti-de Sitter space at finite temperature_, Physics Letters B Volume 189, Issue 3, 7 May 1987, Pages 304-310 (<a href="https://doi.org/10.1016/0370-2693(87)91437-7">doi:10.1016/0370-2693(87)91437-7</a>)

See also

* Dirk Schlingemann, _From euclidean field theory to quantum field theory_ ([arXiv:hep-th/9802035](http://arxiv.org/abs/hep-th/9802035))

* [[Graeme Segal]], _Wick rotation and the positivity of energy in quantum field theory_ ([video](https://www.youtube.com/watch?feature=player_embedded&v=vTvXHL6ZJik))

* {#Witten13} [[Edward Witten]], _The Feynman $i \epsilon$ in String Theory_ ([arXiv:1307.5124](http://arxiv.org/abs/1307.5124))

On the (non-)existence of Wick rotation for [[quantum field theory on curved spacetimes]]:

MathOverflow comments:

* [[Igor Khavkine]] ([MO:a/165317](https://mathoverflow.net/a/165317/381))

* [[Robert Bryant]] ([MO:a/165345](https://mathoverflow.net/a/165345/381))

See also:

* {#HollandsWald14} [[Stefan Hollands]], [[Robert Wald]], p. 7-8 in: _Quantum fields in curved spacetime_, Physics Reports Volume 574, 16 April 2015, Pages 1-35 ([arXiv:1401.2026](https://arxiv.org/abs/1401.2026), [doi:10.1016/j.physrep.2015.02.001](https://doi.org/10.1016/j.physrep.2015.02.001))


[[!redirects Wick rotations]]
