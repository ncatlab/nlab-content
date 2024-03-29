
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A _presymplectic structure_ on a [[smooth manifold]] or more generally on a [[smooth space]] $X$  is simply a closed [[differential 2-form]] $\omega \in \Omega^2(X)$. 

(In parts of the literature a pre-symplectic 2-form is required to have constant rank. However, other parts of the literature do not require this, e.g. [Bottacin, def. 3.1](#Bottacin). )

If the 2-form is happens to be _non-degenerate_ (have maximal rank) then it is a _[[symplectic structure]]_ on $X$. 

Given a presymplectic structure, the [[quotient]] of $X$ by the [[flow]] of the [[vector fields]] in the [[kernel]] of $\omega$ is, if it exists in a reasonable way, a [[symplectic manifold]].

One speaks of closed 2-forms as presymplectic structures if one is interested in eventually forming this quotient and obtaining a symplectic structure. 

The central application of this appears in the theory of [[quantization]] of [[action functionals]]. The [[covariant phase space]] of a [[local action functional]] is canonically presymplectic, and one is interested in its quotientient by symmetries to obtain a symplectic structure. This quotient generically is very ill behaved, though, when taken in the naive way. The [[BV-BRST formalism]] is all about forming this quotient "up to homotopy", such that it exists in a reasonable way. See [[derived critical locus]] for more on this.

The notion of presymplectic structure is a weakening of the notion of [[symplectic structure]] roughly orthogonal to the notion of [[Poisson structure]].

## Properties

### Ambient symplectic manifold

Under mild technical conditions, presymplectic manifolds arise as submanifolds of ambient symplectic manifolds. See ([EMR, theorem 3](#EMR)).


## Examples

* [[covariant phase space]]

## Related concepts

* [[symplectic structure]], [[almost symplectic structure]]

* [[geometric quantization]], [[geometric quantization of non-integral forms]]

[[!include symplectic reduction - table]]
  

## References

The generalization of [[symplectic reduction]] for presymplectic manifolds, _[[presymplectic reduction]]_ is discussed in

* Francesco Bottacin, _A Marsden-Weinstein  reduction theorem for presymplectic manifold_ ([pdf](http://www.math.unipd.it/~bottacin/papers/presympred.pdf))
  {#Bottacin}

* A. Echeverr&#237;a-Enr&#237;quez, M.C. Mu&#241;oz-Lecanda, N. Rom&#225;n-Roy, _Reduction of Presymplectic Manifolds with Symmetry_ ([arXiv:math-ph/9911008](http://arxiv.org/abs/math-ph/9911008))
 {#EMR}

The [[geometric quantization]] of presymplectic manifolds by [[geometric quantization by push-forward]] is discussed in 

* Ana Canas da Silva, [[Yael Karshon]], Susan Tolman, _Quantization of Presymplectic Manifolds and Circle Actions_, Trans. Amer. Math. Soc. 352 (2000), 525-552 ([arXiv:dg-ga/9705008](http://arxiv.org/abs/dg-ga/9705008))



[[!redirects presymplectic structures]]

[[!redirects pre-symplectic form]]
[[!redirects presymplectic form]]
[[!redirects pre-symplectic forms]]
[[!redirects presymplectic forms]]

[[!redirects presymplectic smooth space]]
[[!redirects presymplectic smooth spaces]]

[[!redirects presymplectic manifold]]
[[!redirects presymplectic manifolds]]

[[!redirects pre-symplectic manifold]]
[[!redirects pre-symplectic manifolds]]

