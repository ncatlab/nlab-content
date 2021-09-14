
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

The _Riemann zeta function_ is the archetypical example of a [[zeta function]], defined by the formula

$$
  \zeta \colon s \mapsto \underoverset{n = 1}{\infty}{\sum} \frac{1}{n^s}
  \,.
$$

From the point of view of [[arithmetic geometry]] and the [[function field analogy]], the Riemann zeta function is the basic case "over [[F1]]" of a tower of [[zeta functions]] for [[arithmetic curves]] given by more general [[number fields]] -- the [[Dedekind zeta functions]] -- and over [[function fields]] -- the [[Weil zeta function]] -- and for [[complex curves]] -- the Selberg [[zeta function of a Riemann surface]] -- and in another direction for higher dimensional [[arithmetic schemes]] -- the [[arithmetic zeta functions]].

## Properties

### Special values

Some of [[special values of L-functions|special values]] of the Riemann zeta function found (for the non-trivial region of non-positive integers) by [[Leonhard Euler]] in 1734 and 1749 are

| n | -5 | -3 | -1 |  0 | 2 | 4 | 6 | 8 |
|---|----|----|----|----|---|---|---|---|
| $\zeta(n)$ | $-\frac{1}{252}$ |  $\frac{1}{120}$ | $-\frac{1}{12}$ | $-\frac{1}{2}$ | $\frac{\pi^2}{6}$ | $\frac{\pi^4}{90}$ | $\frac{\pi^6}{945}$ | $\frac{\pi^8}{9450}$

where for instance the value $\zeta(-1) = -\frac{1}{12}$ turns out to be the [Euler characteristic of the moduli stack of complex elliptic curves](moduli+stack+of+elliptic+curves#EulerCharacteristic) and as such controls much of [[string theory]].


### The completed zeta function
 {#TheCompletedZetaFunction}

The following slight variant of the actual Riemann zeta function typically exhibits its special properties more explicitly.

+-- {: .num_defn #CompletedRiemannZetaFunction}
###### Definition

The _completed_ Riemann zeta function is 

$$
  \hat \zeta(s) \coloneqq \pi^{-s/2}\Gamma(s/2)\zeta(s)
 \,,
$$

where $\Gamma(-)$ denotes the [[Gamma function]].

=--

+-- {: .num_prop #AdelicIntegralIncarnationOfCompletedZeta}
###### Proposition


The completed Riemann zeta function, def. \ref{CompletedRiemannZetaFunction}, is the [[adelic integral]]

$$
  \hat \zeta(s) 
   = 
  \int_{\mathbb{A}_{\mathbb{Q}}^\times } 
    \exp(-S(x))
    \;
    {\vert x\vert}^s 
    \;
   d \mu_{\mathbb{A}_{\mathbb{Q}}^\times}(x) 
$$

where

* $\exp(-S(-))\colon \mathbb{A}_{\mathbb{Q}}^\times$ denotes the function which sends an [[idele]] $x \in \mathbb{A}_{\mathbb{Q}}^\times$ with canonical components $x = (x_\infty, x_2, \cdots, x_p, \cdots)$
 
  to the product

  $$
    \exp(-S(x)) \coloneqq \exp(-\pi x_\infty^2)\prod_{p \; prime} \chi_{\mathbb{Z}_p}(x_p)
    \,,
  $$
 
  where $\chi_{\mathbb{Z}_p}$ denotes the [[characteristic function]] of the [[p-adic integers]] inside the [[ring of adeles]];

  ([Goldfeld-Hundley 11, def. 2.2.5](#GoldfeldHundley11)).


* the [[measure]] is essentially the [[Haar measure]] on the [[idele group]]

  $$
    d \mu_{\mathbb{A}_{\mathbb{Q}}^\times}
    \coloneqq
    \underset{p \leq \infty}{\prod}
    d^\times x_p
  $$ 

  $$
    d^\times x_p 
      \coloneqq
    \left\{
       \array{
           \frac{d x_\infty}{{\vert x_\infty\vert}_\infty} & if \; p = \infty
           \\
           \frac{1}{1-p^{-1}}\frac{d x_p}{{\vert x_p\vert}_p} & if\; p \; finite \; prime
       }
    \right.
  $$

  ([Goldfeld-Hundley 11, def. 2.2.3](#GoldfeldHundley11))

=--

(reviewed e.g. in [Fesenko 08 0.1](#Fesenko08), [Garrett 11, section 1](#Garrett11), [Goldfeld-Hundley 11 (2.2.6)](#GoldfeldHundley11)).


### Relation to the Jacobi theta function
 {#RelationToThetaFunctions}


+-- {: .num_prop }
###### Proposition

The completed zeta function, def. \ref{CompletedRiemannZetaFunction}, is the [[Mellin transform]] of the [[Jacobi theta function]]

$$
  \theta(x)\coloneqq \underset{n \in \mathbb{Z}}{\sum} \exp(- \pi n ^2 x)
$$

in that

$$
  \begin{aligned}
    \hat \zeta(s)
    &= 
    \int_0^\infty (\theta(x^2)-1) x^s  \frac{d x}{x}
    \\
    & \stackrel{\tau := x^2}{=} 
    \frac{1}{2} \int_0^\infty (\theta(\tau)-1) \tau^{s/2}  \frac{d \tau}{\tau}  
  \end{aligned}
 \,.
$$

e.g. ([Fesenko 08, section 0.1](#Fesenko08), [Kowalski, example 2.2.5 ](#Kowalski))

=--

In terms of [[idelic integral]] expression for the complete zeta-function of prop. \ref{AdelicIntegralIncarnationOfCompletedZeta}, this comes out as follows:

We compute the integral $\int_{\mathbb{A}^\times} \exp(-S(\alpha))) |\alpha|^s d\mu_{\mathbb{A}^\times}(\alpha)$ -- as in ([Goldfeld-Hundley 11, pages 47-50](#GoldfeldHundley11)) and the remarks by [[Ivan Fesenko]] in ([Goldfeld-Hundley 11, pages 51-51](#GoldfeldHundley11)). 

We decompose by the [strong approximation theorem for ideles](group+of+ideles#StrongApproximationTheorem) the integration domain into the [[idele class group]]

$$
  \mathbb{Q}^\times \backslash \mathbb{A}_{\mathbb{Q}}^\times
  =
  (0,\infty)
  \times
  \underset{p}{\prod} \mathbb{Z}_p^\times
$$

and a factor of the non-zero [[rational numbers]]: so we write 

$$
  \alpha=x n
$$ 

where $x$ runs through representatives of $\mathbb{A}^\times/\mathbb{Q}^\times$ and can be chosen as [[ideles]]  $x=(x_2,x_3,...x_\infty)$ with non-archimedean coordinates being units in $\mathbb{Z}_p$ and $x_\infty$ a [[positive number|positive]] [[real number]], and $n$ is a non-zero [[rational number]].  

This way the inner integration is $\int_{\mathbb{Q}^\times} \exp(-S(x n))  d n$. Due to the definition of  $\exp(-S(-))$ in prop. \ref{AdelicIntegralIncarnationOfCompletedZeta}, the integrand here is supported on elements $x n\in \mathbb{Z}_p$ for all $p$, and since  $x_p\in  \mathbb{Z}_p^\times$ we deduce $n\in \mathbb{Z}_p$ for all $p$. Since $\mathbb{Q}$ intersected with all $\mathbb{Z}_p$ is $\mathbb{Z}$ (by the [arithmetic fracture square](fracture+theorem#ArithmeticFractureSquares)),
we have

$$
  \begin{aligned}
     \int_{\mathbb{Q}^\times}\exp(-S(x n))  d n
     & = 
     \sum_{n\in \mathbb{Z}^\times} exp(-\pi n^2 x_\infty^2)
     \\
     & = \theta(x_\infty^2)-1
  \end{aligned}
$$

Therefore the full integral becomes $\int_{\mathbb{R}_{\gt 0}}( \theta(y^2)-1) y^s \frac{d y}{y}$ with $y=x_\infty$.  


### Functional equation

The [[adelic integral]] representation of prop. \ref{AdelicIntegralIncarnationOfCompletedZeta} directly implies the [[functional equation]] 

$$
 \hat \zeta(1-s) = \hat \zeta(s)
$$

of the completed zeta function from the [[functional equation]] of the theta function 

$$
  \theta(x^2) x = \theta(x^{-2})
$$

which in turn follows from the [[Poisson summation formula]] (see at _[Jacobi theta function -- Functional equation](Jacobi+theta+function#FunctionalEquation)_).

In terms of the adelic integral expression, the functional equation of the theta function (and of the zeta integral)
corresponds to the analytic duality furnished by Fourier transform on the adelic spaces and its subspaces. (due to [Tate 50](#Tate50), reviewed for instance in [Fesenko 08 0.1](#Fesenko08), [Garrett 11, section 1.9](#Garrett11), [Goldfeld-Hundley 11 theorem 2.2.12](#GoldfeldHundley11))

This [[adelic integral]]-method generalizes to [[Dedekind zeta functions]] for any [[algebraic number field]]. This is due to ([Tate 50](#Tate50)), highlighted in ([Goldfeld-Hundley 11, Remark (1) by Ivan Fesenko](#GoldfeldHundley11)).

### Euler product form

...[[Euler product]]...

$$
  \sum_{n=1}^\infty \frac{1}{n^s}
  =
  \underset{p\; prime}{\prod} \frac{1}{1-p^{-s}}
$$


### Analogs over number fields, function fields and complex curves

The [[function field analogy]] in view of the discussion at _[[zeta function of an elliptic differential operator]]_ says that the Riemann zeta function is [[analogy|analogous]] to the regulated [[functional determinant|functional trace]] of a would-be "[[Dirac operator]] on [[Spec(Z)]]".

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

Other identifications/analogies of the Riemann zeta function (and more generally the [[Dedekind zeta-function]]) with [[partition functions]] in [[physics]] have been proposed, in particular the _[[Bost-Connes system]]_.


See also at _[[function field analogy]]_.


## Related concepts

* [[Riemann hypothesis]]



## References


Discussion in the context of [[adelic integration]] and [[higher arithmetic geometry]] is in 

* {#Tate50} [[John Tate]], _Fourier analysis in number fields, and Hecke's zeta-functions_, Algebraic Number Theory (Proc. Instructional Conf., Brighton, 1965), Thompson, Washington, D.C., pp. 305&#8211;34 1950

* {#Fesenko08} [[Ivan Fesenko]], _Adelic approch to the zeta function of arithmetic schemes in dimension two_, Moscow Math. J. 8 (2008), 273&#8211;317 ([pdf](https://www.maths.nottingham.ac.uk/personal/ibf/ada.pdf))

with review including 

* {#Garrett11} [[Paul Garrett]], _Iwasawa-Tate on &#950;-functions and L-functions_, 2011 ([pdf](http://www-users.math.umn.edu/~garrett/m/mfms/notes_c/Iwasawa-Tate.pdf)

* {#Kowalski} E. Kowalski, first part of _Automorphic forms, L-functions and number theory (March 12&#8211;16) Three Introductory lectures_ ([pdf](http://www.math.ethz.ch/~kowalski/lectures.pdf))

* {#GoldfeldHundley11} [[Dorian Goldfeld]], [[Joseph Hundley]], chapter 2 of _Automorphic representations and L-functions for the general linear group_, Cambridge Studies in Advanced Mathematics 129, 2011 ([pdf](https://www.maths.nottingham.ac.uk/personal/ibf/text/gl2.pdf))

Discussion in the context of [[p-adic string theory]]:

* [[An Huang]], [[Bogdan Stoica]], [[Shing-Tung Yau]], _General relativity from $p$-adic strings_ ([arXiv:1901.02013](https://arxiv.org/abs/1901.02013))


[[!redirects Riemann zeta-function]]

[[!redirects complete Riemann zeta function]]
[[!redirects complete Riemann zeta-function]]