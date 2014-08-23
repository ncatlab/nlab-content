
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The archetypical example of a [[zeta function]]:

$$
   \zeta \colon s \mapsto \underoverset{n = 1}{\infty}{\sum} \frac{1}{n^s}
  \,.
$$


## Properties

### The completed zeta function
 {#TheCompletedZetaFunction}

The _completed_ Riemann zeta function is 

$$
  \hat \zeta(s) \coloneqq \pi^{-s/2}\Gamma(s/2)\zeta(s)
 \,.
$$

This may be viewed as the [[adelic integral]]

$$
  \hat \zeta(s) 
   = 
  \int_{\mathbb{A}_{\mathbb{Q}}^\times } 
    f(x) {\vert x\vert}^s 
   d \mu_{\mathbb{A}_{\mathbb{Q}}^\times}(x) 
$$

with respect to a suitable [[Haar measure]] $d \mu_{\mathbb{A}_{\mathbb{Q}}^\times}$ on the [[group of ideles]] and where $f(x)$ is the [[tensor product]] of the [[characteristic functions]] of the [[p-adic integers]] and of $\exp(-\pi x^2)$ at the [[place at infinity]].

([Fesenko 08 0.1](#Fesenko08))

when we start to compute this integral $\int_{A^\times} f(\alpha) |\alpha|^s d\mu_{A^\times}(\alpha)$, see for more detail p. 47-50 (and also p. 51-52 of my remark there) in Goldfeld-Hundley, what we first do is use a filtration on $A^\times$ which we know from class field theory (but no class field theory is used anywhere in this computation): $A^\times> \bbb Q^\times$, so we write $\alpha=xn$ where $x$ runs through representatives of $A^\times/\bbb Q^\times$ and can be chosen as ideles  $x=(x_2,x_3,...x_\infty)$ with non-archimedean coordinates being units in $\bbb Z_p$ and $x_\infty$ a positive real number, and $n$ is a non-zero rational number,  and the computation is reduced to the internal integral  $\int_{Q^\times} f(x n)  dn$. Due to the definition of  $f$,
we have $xn\in \bbb Z_p$ for all p, and since $x_p\in  \bbb Z_p^\times$ we deduce $n\in \bbb Z_p$ for all p. Since Q intersected with all $\bbb Z_p$ is $\bbb Z$, the last integral is just the series $\sum_{n\in\bbb Z\setminus 0} exp(-\pi n^2 x_\infty^2)$, i.e. $\theta(x_\infty^2)-1$, and the original zeta integral becomes $\int_{\bbb R_{>0}}( \theta(y^2)-1) y^s dy/y$, $y=x_\infty$.  

### Relation to the Jacobi theta function
 {#RelationToThetaFunctions}


The completed zeta function from [above](#TheCompletedZetaFunction) has an [[integral]]-representation in terms of the [[Jacobi theta function]]

$$
  \theta(x)\coloneqq \underset{n \in \mathbb{Z}}{\sum} \exp(- \pi n ^2 x)
$$

in the form

$$
  \hat \zeta(s)
  = 
   \int_0^\infty (\theta(x^2)-1) x^s  \frac{d x}{x}
 \,.
$$

e.g. ([Fesenko 08, section 0.1](#Fesenko08), [Kowalski, example 2.2.5 ](#Kowalski))

### Functional equation

The [above](#RelationToThetaFunctions) integral representation now directly implies the [[functional equation]] 

$$
 \hat \zeta(1-s) = \hat \zeta(s)
$$

of the completed zeta function from the [[functional equation]] of the theta function 

$$
  \theta(x^2) x = \theta(x^{-2})
$$

which in turn follows from the [[Poisson summation formula]].

In terms of the adelic integral expression, the functional equation of the theta function (and of the zeta integral)
corresponds to the analytic duality furnished by Fourier transform on the adelic spaces and its subspaces. ([Fesenko 08 0.1](#Fesenko08))

### Analogs over number fields, function fields and complex curves

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

See also at _[[function field analogy]]_.

## References


Discussion in the more general context of [[higher arithmetic geometry]] is in 

* {#Fesenko08} [[Ivan Fesenko]], _Adelic approch to the zeta function of arithmetic schemes in dimension two_, Moscow Math. J. 8 (2008), 273&#8211;317 ([pdf](https://www.maths.nottingham.ac.uk/personal/ibf/ada.pdf))

* {#Kowalski} E. Kowalski, first part of _Automorphic forms, L-functions and number theory (March 12&#8211;16) Three Introductory lectures_ ([pdf](http://www.math.ethz.ch/~kowalski/lectures.pdf))


[[!redirects Riemann zeta-function]]