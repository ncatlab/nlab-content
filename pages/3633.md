
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

What is called _Wick rotation_ (after [[Gian-Carlo Wick]]) is a method in [[physics]] for finding a construction in [[relativistic field theory]] on [[Minkowski spacetime]] or, more generally, on [[Lorentzian manifolds]], from a related construction in [[Euclidean field theory]] on [[Riemannian manifolds]]. This is motivated by the observation that the [[Minkowski metric]] (with the $-1,1,1,1$ convention) and the four-Euclidean metric are equivalent if the [[time]] components of either are allowed to have [[imaginary part|imaginary]] values. Hence Wick rotation, when it applies, involves [[analytic continuation]] of [[n-point functions]] to [[complex number|complex vaklued]] [[time]] [[coordinates]].

In some special cases Wick rotation has been rigorously understood and takes the form of a [[theorem]]. Notably the _[[Osterwalder-Schrader theorem]]_ gives a precise meaning to Wick rotation for [[quantum field theory]] on [[Minkowski spacetime]] formalized by the [[axioms]] of [[AQFT]].

More generally, in this context Wick rotation applies to relativistic field theory in [[thermal equilibrium]] [[states]] at finite [[temperature]] $T$, and then relates this to [[Euclidean field theory]] with compact/periodic Euclidean time of length $\beta = 1/T$:

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
    \text{n-point function of relativistic fields}
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
    \text{ for "Eculidean time" of periodicity}\; \beta = 1/T
  }{
  \underbrace{
  \left\langle 0 \vert \mathbf{\Phi}(x_1) \mathbf{\Phi}(x_2) \cdots \mathbf{\Phi}(x_n)  \vert 0 \right\rangle_{\mathbb{R}^{d} \times S^1_{\beta}}
  }}
  }
$$

In this form, Wick rotation is also known as _[[thermal quantum field theory]]_. See there for more.


However, Wick rotation is sometimes also appealed to in situations where the assumptions of theorems like this are evidently violated. For instance, it has been appealed to a lot in an approach to [[quantum gravity]] often known as "Euclidean quantum gravity", where, however, by definition the assumption of global spacetime translation invariance is manifestly violated. In such a context the exact meaning of Wick rotation remains mysterious, and yet on this basis some subtle relations between quantum mechanics and thermodynamics, such as the [[Bekenstein-Hawking entropy]], find elegant explanations, at least at the level of the manipulation of formulas. 

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


See also at _[[Osterwalder-Schrader theorem]]_.

* Dirk Schlingemann, _From euclidean field theory to quantum field theory_ ([arXiv:hep-th/9802035](http://arxiv.org/abs/hep-th/9802035))

* [[Graeme Segal]], _Wick rotation and the positivity of energy in quantum field theory_ ([video](https://www.youtube.com/watch?feature=player_embedded&v=vTvXHL6ZJik))

* {#Witten13} [[Edward Witten]], _The Feynman $i \epsilon$ in String Theory_ ([arXiv:1307.5124](http://arxiv.org/abs/1307.5124))


The idea of Wick rotating thermal relativistic field theory to compact periodic Euclidean time apparently goes back to 

* {#Bloch58} Claude Bloch, _Sur la détermination de l'état fondamental d'un système de particules_,  Nucl. Phys. 7 (1958) 451

This has maybe first been made precise, for the case of 1+1 dimensions, in 

* {#HoeghKrohn74} [[Raphael Høegh-Krohn]], _Relativistic Quantum Statistical Mechanics in two-dimensional Space-Time_, Communications in Mathematical Physics 38.3 (1974): 195-224 ([pdf](https://www.duo.uio.no/bitstream/handle/10852/44072/1973-22.pdf))

Good review on the relation to [[thermal quantum field theory]] is in

* {#FullingRuijsenaars87} S.A. Fulling, S.N.M. Ruijsenaars, _Temperature, periodicity and horizons_, Physics Reports Volume 152, Issue 3, August 1987, Pages 135-176 ([pdf](https://www1.maths.leeds.ac.uk/~siru/papers/p26.pdf), <a href="https://doi.org/10.1016/0370-1573(87)90136-0">doi:10.1016/0370-1573(87)90136-0</a>)


