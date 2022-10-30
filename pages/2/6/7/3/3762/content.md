
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Theta functions
+--{: .hide}
[[!include theta functions - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of _zeta function_ originates in [[number theory]], but to get an idea of what they "really are" it is helpful to proceed anachronistically:

$\zeta$-functions are [[meromorphic functions]] $s \mapsto \zeta(s)$ on the [[complex plane]], which behave like like [[analytic continuations]] of [[traces]] of powers 

$$
  s \mapsto Tr \left(\frac{1}{H}\right)^s
$$ 

of suitable [[elliptic differential operators]] $H$ (in [[physics]] these are [[regularization (physics)|regularized]] [[traces]] of [[Feynman propagators]] leading to expressions for [[vacuum amplitudes]]), which means that for sufficiently nice such $H$ these are analytic continuations in $s$ of sums of the form

$$
  s \mapsto \underset{\lambda}{\sum}  \lambda^{-s}
  \,,
$$

where the summation is over the [[eigenvalues]] $\lambda$ of $H$.

Indeed, such _[[zeta functions of elliptic differential operators]]_ constitutes one class of examples of zeta functions.  Of particular interest is the case where $H$ is a [[Laplace operator]] of a [[hyperbolic manifold]] and in particular on a hyperbolic [[Riemann surface]], for that case one obtains the _[[zeta function of a Riemann surface]]_, in particular the _[[Selberg zeta function]]_.

In modern language one also speaks of _[[L-functions]]_. Where a zeta function of some space is like the [[Feynman propagator]] of _the_ canonical [[Laplace operator]] of that space, an L-function is defined from an extra "twisting" information such as that of a [[flat bundle]]/[[local system of coefficients]] on the space (and is hence like the [[Feynman propagator]] of the corresponding twisted/coupled [[Laplace operator]]). The major properties satisfied by anything that qualifies as a zeta function or [[L-functions]] are: these are [[meromorphic functions]] $s \mapsto L(s)$ on the [[complex plane]] such that

1. for $\Re(s) \gt 1$ they have a [[convergence|converging]] [[series]] expansion of the above form, and/or a [[infinite product|multiplicative series]] expression, the _[[Euler product]]_;

1. such that [[analytic continuation]] of the series expression exists to a meromorphic function $L(-)$ on the complex plane;

1. and such that the result satisfies a _[[functional equation]]_ which says that the product $\hat L$ of $L$ with some correcion functions satisfies $\hat L(1-s) = \hat L(s)$.
 
Proceeding from the above class of examples in [[complex analytic geometry]] one may wonder if there are [[analogy|analogs]] also in [[arithmetic geometry]]. Indeed, by the [[function field analogy]] there are. All the way down "on [[Spec(Z)]]" the analog of the [[Selberg zeta function]] is the [[Riemann zeta function]], which _historically_ is the first of all zeta functions, defined by [[analytic continuation]] of the [[series]]

$$
   s \mapsto \underoverset{n = 1}{\infty}{\sum} n^{-s}
  \,.
$$

The _[[Riemann hypothesis]]_ [[conjecture|conjectures]] a characterization of the [[roots]] of this zeta function and is regarded as one of the outstanding problems in [[mathematics]]. It has evident analogs for all other zeta functions (for some of which it has been proven).

More generally, over [[arithmetic curves]] which are [[spectrum of a commutative ring|spectra]] of [[rings of integers]] of more general [[number fields]], the Riemann zeta function has generalization to the _[[Artin L-functions]]_ defined intrinsically in terms of [[characteristic polynomials]] of [[Galois representations]]. When the Galois representation is 1-dimensional, then the Artin L-function may be expressed (by "[[Artin reciprocity]]") in terms of "more arithmetic" data by [[Dirichlet L-functions]] and [[Hecke L-functions]]. When the Galois representation is higher dimensional, then the [[Langlands correspondence]] [[conjecture]] asserts that the Artin L-function may be expressed "arithmetically" as the [[automorphic L-function]] of an [[automorphic form]].

Similarly on [[arithmetic curves]] given by [[function fields]] there is the [[Goss zeta function]] and in [[higher dimensional arithmetic geometry]] the [[Weil zeta function]], famous from the _[[Weil conjectures]]_. The 

When interpreting the [[Frobenius morphisms]] that appear in the [[Artin L-functions]] geometrically as flows (as discussed at _[Borger's arithmetic geometry -- Motivation](Borger's+absolute+geometry#Motivation)_) then this induces an evident analog of [[zeta function of a dynamical system]]. This in turn has strong analogies with [[Alexander polynomials]] in [[knot theory]] (see at _[[arithmetic topology]]_).

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]


## Properties

### Function field analogy
 {#FunctionFieldAnalogy}

One way to understand the plethora of different zeta functions is to see them as the incarnation of the same general concept in different flavors of [[geometry]]. This is expressed at least in parts by the

[[!include function field analogy -- table]]

## Related concepts

* [[multiple zeta values]], [[motivic multiple zeta values]], [[motivic integration]], [[motive]]

* [[Weil conjecture]]

* [[Riemann hypothesis]]

* there are attempts to understand the Riemann zeta function as the spectrum of a [[Hamiltonian]] of a [[quantum mechanical system]]. See at _[[Riemann hypothesis and physics]]_.

* [[Beilinson regulator]]

* [[zeta function of a Riemann surface]]


## References

### General

A useful survey of the zoo of zeta functions is in 

* [[Jeffrey Lagarias]], _Number theory zeta functions and Dynamical zeta functions_ ([pdf](http://www.math.lsa.umich.edu/~lagarias/doc/numberthzeta.pdf))

Further general review includes

* {#Kowalski} E. Kowalski, first part of _Automorphic forms, L-functions and number theory (March 12&#8211;16) Three Introductory lectures_ ([pdf](http://www.math.ethz.ch/~kowalski/lectures.pdf))

* [[Alain Connes]], [[Matilde Marcolli]], chapter II of _[[Noncommutative Geometry, Quantum Fields and Motives]]_

Discussion in the more general context of [[higher dimensional arithmetic geometry]] is in 

* {#Fesenko08} [[Ivan Fesenko]], _Adelic approch to the zeta function of arithmetic schemes in dimension two_, Moscow Math. J. 8 (2008), 273&#8211;317 ([pdf](https://www.maths.nottingham.ac.uk/personal/ibf/ada.pdf))

### In algebraic geometry

* [[Yuri Manin]], _Lectures on zeta functions and motives (according to Deninger and Kurokawa)_, Ast&#233;risque __228__:4 (1995) 121--163, and preprint MPIM1992-50 [pdf](http://www.mpim-bonn.mpg.de/preblob/4793)

* Nobushige Kurokawa, _Zeta functions over $F_1$_,  Proc. Japan Acad. Ser. A Math. Sci. __81__:10 (2005) 180-184 [euclid](http://projecteuclid.org/euclid.pja/1135791771)



### Categorical approaches

* [[Michael Larsen|M. Larsen]], [[Valery Lunts|V. A. Lunts]], _Motivic measures and stable birational geometry_, Mosc. Math. J. __3__, 1 (2003) 85--95; _Rationality criteria for motivic zeta functions_, Compos. Math. __140__:6 (2004) 1537&#8211;1560
* [[Vladimir Guletskii]], _Zeta functions in triangulated categories_, Mathematical Notes __87__, 3 (2010) 369--381, [math/0605040](http://arxiv.org/abs/math/0605040) 
* [[Maxim Kontsevich|M. Kontsevich]], _Notes on motives in finite characteristics_, [math.AG/0702206](http://arxiv.org/abs/math.AG/0702206) 

* [[John Baez]], _[[johnbaez:Zeta functions]]_

* [[Sergey Galkin]], [[Evgeny Shinder]], _On a zeta-function of a dg-category_, [arXiv:1506.05831](http://arxiv.org/abs/1506.05831).

[[!redirects zeta functions]]