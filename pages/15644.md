+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Theta functions
+--{: .hide}
[[!include theta functions - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The _Dirichlet L-functions_ $L_\chi$ are a kind of [[L-function]] induced by [[Dirichlet characters]] $\chi$ 

$$
  L_\chi(s) \coloneqq \underoverset{n=1}{\infty}{\sum} \chi(n)n^{-s}
  \,.
$$

(e.g. [Goldfeld-Hundley 11 (2.2.1)](#GoldfeldHundley11), [Continuations](#Continuations)). 

The completion of this by a [[Gamma function]] factor (and a power of $\pi$ and of the [[conductor]]) is the [[Mellin transform]] of the [[Dirichlet theta function]] (e.g. [Continuations, p. 8](#Continuations)).


By [[Artin reciprocity]] Dirichlet L-function are equal to suitable [[Artin L-functions]] induced by 1-dimensional [[Galois representations]].

In terms of the [[adelic integral]] representation of L-functions via [[Iwasawa-Tate theory]], given a [[Dirichlet character]] $\chi$ then the corresponding Dirichlet L-functions are simply the [[adelic integrals]] (e.g. [Garrett 11, section 2.2](#Garrett11))

$$
  s \mapsto \int_{\mathbb{I}} \chi(x) \;f(x)\; {\vert x\vert}^s
$$

for suitable Schwartz functions $f$ on the [[idele group]].

Hence Dirichlet L-functions are [[Mellin transforms]] of suitable [[theta functions]] ("theta kernels"), see. e.g. ([Stopple, p. 3](#Stopple)).

Where [[Dirichlet characters]] (see there) are essentially [[automorphic forms]] for the [[idele group]] (hence for $n = 1$) the generalization to automorphic forms for $n \geq 1$ is the concept of _[[automorphic L-function]]_.

The differential geometric analog of a Dirichlet L-function is the _[[eta function]]_ (see there for more) of a differential operator.


## Related concepts

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

## References

* E. Kowalski, section 1.3 of  _Automorphic forms, L-functions and number theory (March 12&#8211;16) Three Introductory lectures_ ([pdf](http://www.math.ethz.ch/~kowalski/lectures.pdf))

* {#Continuations} section 3 of _Continuations and functional equations_ ([pdf](http://people.reed.edu/~jerry/361/lectures/feqn.pdf))

* Wikipedia, _[Dirichlet L-function](http://en.wikipedia.org/wiki/Dirichlet_L-function)_

* {#GoldfeldHundley11} [[Dorian Goldfeld]], [[Joseph Hundley]], chapter 2 of _Automorphic representations and L-functions for the general linear group_, Cambridge Studies in Advanced Mathematics 129, 2011 ([pdf](https://www.maths.nottingham.ac.uk/personal/ibf/text/gl2.pdf))

* {#Garrett11} [[Paul Garrett]], section 1.6 _Iwasawa-Tate on &#950;-functions and L-functions_
([pdf](http://www-users.math.umn.edu/~garrett/m/mfms/notes_c/Iwasawa-Tate.pdf))

* {#Stopple95} [[Jeffrey Stopple]], _Theta and $L$-function splittings_, Acta Arithmetica LXXII.2 (1995) ([pdf](http://matwbn.icm.edu.pl/ksiazki/aa/aa72/aa7221.pdf))

Analogs of Dirichlet L-functions in [[chromatic homotopy theory]] are constructed in 

* Ningchuan Zhang, _Analogs of Dirichlet L-functions in chromatic homotopy theory_, ([arXiv:1910.14582](https://arxiv.org/abs/1910.14582))


[[!redirects Dirichlet L-functions]]

[[!redirects Dirichlet L-series]]

