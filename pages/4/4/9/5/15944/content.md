[[!redirects Arithmetic cryptography]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic cryptography
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Arithmetic cryptography is the developing subject that describes [public key cryptography](http://en.wikipedia.org/wiki/Public-key_cryptography) systems based on the use of arithmetic geometry of schemes (or [[global analytic spaces]]) over $\mathbb{Z}$.

There are two well known examples of such systems:

1. The first and most used one, which is very efficient **because** it is conformal to the [KISS principle](http://en.wikipedia.org/wiki/KISS_principle), is based on the fact that it is very difficult (from the computational viewpoint) to factorize a natural number into a product of two big prime numbers.

1. The second one is based on the [discrete logarithm](http://en.wikipedia.org/wiki/Discrete_logarithm) problem on elliptic curves (or more generally abelian varieties) over finite fields. It has the advantage on the first algorithm of allowing to make shorter keys, without compromising security (NSA has generalized the use of [elliptic curve cryptography](http://en.wikipedia.org/wiki/Elliptic_curve_cryptography) algorithm both for commercial and classified use, as explained on the wikipedia page on elliptic curve cryptography).

The basic idea of arithmetic cryptography is to use a finite family $X$ of polynomials with integer coefficients $P_1,\dots,P_m\in \mathbb{Z}[X_1,\dots,X_n]$ (or more generally a quasi-projective scheme $X$ of finite type over $\mathbb{Z}$, or even maybe a [[global analytic space]] $X$ over a convenient Banach ring), encoded in a finite number of integers (the coefficients and degrees of the corresponding polynomials), together with some additional data (such as a way to cut a part of the associated motive) to define a [public key cryptosystem](http://en.wikipedia.org/wiki/Public-key_cryptography).

Some computational aspects of general motives have been investigated in the case of motives of modular forms by Bass Edixhoven and Jean-Marc Couveignes, using &#233;tale cohomological methods. Kedlaya and Lauder-Wan also studied the Dwork approach from a computational viewpoint.

## Necessary tools

Since the space $X$ to be used is given by a non-linear equation, it is not directly adapted to the use of computational methods. One will thus need to extract linear invariants from $X$, by the use of a kind of  `differential calculus` (in Quillen's sense, i.e., using a convenient [[tangent (infinity,1)-category]]) and/or the definition of convenient `cohomological invariants`.

It seems that &#233;tale cohomological methods, that were originally used by Grothendieck and Deligne (and more recently, Laumon) to prove the full Weil conjectures, are not so easy to implement on a computer (see however the book of Edixhoven and Couveignes). It seems that "[[p-adic]] methods", based on p-adic differential calculus and Fourier transform, and now completely developed by Berthelot, Lestum, Caro and Kedlaya (p-adic proof of the Weil-conjectures) are better adapted to computations (e.g., of L-functions over finite fields, i.e., characteristic polynomials of frobenius acting on cohomology).

It thus looks like an important project to develop "[[p-adic]] methods" in [[global analytic geometry]], starting with the definition of two types of cohomology theories for [[global analytic spaces]]: an [[absolute cohomology]] theory (related to the Chern character from K-theory to negative cyclic cohomology) and a [[geometric cohomology]] theory (with characteristic $0$ coefficients, e.g., in the full ring $\mathbb{A}$) of ad&#232;les). It may also be interesting to develop a notion of [[global Fourier transform]].

One of these cohomology theories (the absolute one) should give a natural way to study various conjectures on [[special values of L-functions]] and the other (the geometric one) should give a natural way to study the position of zeroes and poles of L-functions by spectral methods.

The [[geometric cohomology theory]] should also be (since it has characteristic $0$ coefficients) related to the theory of motives and [[global automorphic representations]], and thus give more generally a spectral way of studying zeroes and poles of the L-function of the rational motive of an [[arithmetic variety]].

## Aims

The aim of arithmetic cryptography is to define a good [[geometric cohomology]] theory for [[global analytic spaces]] based on analytic methods and differential calculus that would allow the definition of [public key cryptography](http://en.wikipedia.org/wiki/Public-key_cryptography) systems based on the datum of a [[global analytic space]] $X$ and of (say) a part $M$ of the associated (maybe absolute) rational motive $M(X)$. The definition of such methods would not give any new attacks to the previous ones, but may give a bigger class of public keys, that may allow the use of shorter ones. However, it is not yet clear that such a general approach will be conformal to the [KISS principle](http://en.wikipedia.org/wiki/KISS_principle). In particular, as explained by Edixhoven in a preprint, it seems to be quite a hard computational task to determine if two cohomology classes are equal, at least in the $\ell$-adic setting.

## Possible constraints on the theory

The constraints on such a theory would be the following:

1. find back the discrete logarithm elliptic public key cryptography when one starts from an elliptic curve over a finite field (or maybe a corresponding weak formal scheme over the ring of p-typical Witt vectors).

1. find back the original prime factorization public key cryptography when one starts from $\mathbb{Z}$. It must be clearly stressed here that the proper theoretical setting for such a general theory may be very hard to develop, since it should involve the definition of a proper cohomology for the Riemann zeta function, that would allow a spectral proof of its functional equation (as in Tate's thesis) `and` of the [[Riemann hypothesis]]. The full project thus looks like a very far reaching one, since there is, up to now, no precise idea of a way of constructing such a [[geometric cohomology]] theory (even if ideas on the constraints that it should fulfill are widespread in the mathematical litterature, e.g., in Deninger's work, in the [[field with one element]] litterature, in [[Langlands program]] and in the study of [[Weil-étale cohomology]]). However, one may use the classical conjectures (without proving them) to get the needed estimates.

## Possible methods

It is not at all clear that the following propositions will be conformal to the KISS principle. They may also be attacked by quantum computing methods, by higher dimensional generalizations of Shor's algorithm, but one may hope that allowing the use of arbitrary arithmetic schemes may make the quantum computing methods more difficult to apply and/or implement in general. This also means that these propositions may be very hard to implement in practice.

A starting point for crash-testing the compatibility of higher dimensional arithmetic cryptography with the [KISS principle](http://en.wikipedia.org/wiki/KISS_principle) may be to test it in the finite characteristic case (with p-adic methods, say derived analytic spaces over $\mathbb{Z}_p$, for computational purposes). First remark that the discrete logarithm problem for an elliptic curve over $\mathbb{F}_p$ may be understood as a discrete logarithm problem in the first (&#233;tale torsion) cohomology group of the curve, given by torsion points. One may try to generalize this problem to the higher dimensional situation by giving an algebraic cohomology class $[c]$, and computing $[d]=n.[c]$. The public key is given by the pair $([c],[d])$ and the message is the number $n$. As pointed out by Edixhoven in a preprint, computing a cohomology class may be a very hard computational task, so that this idea may not be conformal to the KISS principle.

One may also devise another "product type" approach to the definition of a public key: given two prime cohomology classes $[c]$ and $[d]$ (classes of irreductible subvarieties of a given codimension), compute their product class $[e]=[c].[d]$ in the cohomology ring. One may try, given $[e]$, to find back $[c]$ and $[d]$, and this may be a very hard problem.

## Related references

Computing zeta functions of arithmetic schemes, David Harvey, [arXiv](http://arxiv.org/abs/1402.3439)