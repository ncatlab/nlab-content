

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Harmonic analysis
+-- {: .hide}
[[!include harmonic analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[function]] on a [[Cartesian space]] is called _rapidly decreasing_ if every the product with any power of the canonical [[coordinate functions]] is a [[bounded function]] (def. \ref{RapidlyDecreasingFunction} below).

Of particular interest are the [[smooth functions]] with are rapidly decreasing and all whose [[partial derivatives]] are rapidly decreasing, too (def. \ref{FunctionsWithRapidlyDecreasingPartialDerivatives} below). These _[[Schwartz functions]]_ enjoy the special property that the operation of [[Fourier transform]] is an [[endomorphism]] on the _[[Schwartz space]]_ of all these functions. This gives them a central place in [[harmonic analysis]]. A _[[tempered distribution]]_ is a [[continuous linear functional]] on this [[Schwartz space]].

## Definition


### Rapidly decreasing functions

+-- {: .num_defn #RapidlyDecreasingFunction}
###### Definition
**(rapidly decreasing function)**

For $n \in \mathbb{N}$, an _[[integrable function]]_ 

$$ 
  f \colon \mathbb{R}^n \to \mathbb{R}
$$ 

on a [[Cartesian space]] $\mathbb{R}^n$ is called _rapidly decreasing_ if for all $\alpha \in \mathbb{N}^n$ the product function  

$$
  x \mapsto x^\alpha f(x)
$$

is a [[bounded function]]. Here

$$
  x^\alpha \;\coloneqq\; (x^1)^{\alpha_1} \cdots (x^n)^{\alpha_n}
$$

is any given product of powers of the canonical [[coordinate functions]].

=--


### Functions with rapidly decreasing partial derivatives

+-- {: .num_defn #FunctionsWithRapidlyDecreasingPartialDerivatives}
###### Definition
**(function with rapidly decreasing [[partial derivatives]])**

A [[smooth function]] 

$$
  f \;\colon\; \mathbb{R}^n \longrightarrow \mathbb{R}
$$

is a _function with rapidly decreasing partial derivatives_ or _Schwartz function_ for short, if all its [[partial derivatives]] are rapidly decreasing functions in the sense of def. \ref{RapidlyDecreasingFunction}, hence if for all $\alphe, \beta \in \mathbb{N}^n$ we have that 

$$
  x \mapsto x^\alpha \partial_{\beta} f
$$

is a [[bounded function]], where

$$
  \partial_\beta 
  \;\coloneqq\;
  \frac{\partial^{\beta_1}}{\partial (x^1)^{\beta_1}}
  \cdots
  \frac{\partial^{\beta_n}}{\partial (x^n)^{\beta_n}}
$$

are the given [[partial derivatives]].

=--


+-- {: .num_prop #Smooth0TypeIsSheavesOnSmoothMfd}
###### Remark

These Schwartz functions (def. \ref{FunctionsWithRapidlyDecreasingPartialDerivatives}) form the _[[Schwartz space]]_ $\mathcal{S}(\mathbb{R}^n)$ used in the definition of [[tempered distributions]] in [[functional analysis]].

=--

## Properties

+-- {: .num_prop #RapidlyDecreasingFunctionsAreIntegrable}
###### Proposition
**([[rapidly decreasing functions]] are [[integrable functions]])**

If $f \colon \mathbb{R}^n \longrightarrow \mathbb{R}$ is a [[rapidly decreasing function]], then its [[integral]] exists

$$
  \int_{x \in \mathbb{R}^n} f(x) \, dvol(x)
   \;\lt \;
   \infty
  \,.
$$

In fact for all $\alpha \in \mathbb{N}^n$ the integral of $x \mapsto x^\alpha f(x)$ exists:

$$
  \int_{x \in \mathbb{R}^n} x^\alpha f(x) \, dvol(x)
   \;\lt \;
   \infty
  \,.
$$

=--


## Examples


+-- {: .num_example #CompactlySupportedSmoothFunctionsAreFunctionsWithRapidlyDecreasingDerivatives} 
###### Example
**([[compactly supported function|compactly supported]] [[smooth funtions]] are [[functions with rapidly decreasing partial derivatives]])**

Every [[compactly supported function|compactly supported]] [[smooth function]] ([[bump function]]) $b \in C^\infty_{cp}(\mathbb{R}^n)$ is rapidly decreasing (def. \ref{RapidlyDecreasingFunction}) has rapidly decreasing partial derivatives (def. \ref{FunctionsWithRapidlyDecreasingPartialDerivatives}):

$$
  C^\infty(\mathbb{R}^n)
   \hookrightarrow
  \mathcal{S}(\mathbb{R}^n)
  \,.
$$

=--

+-- {: .num_example}
###### (Non-)Example

Not every rapidly decreasing function (def. \ref{RapidlyDecreasingFunction}) has rapidly decreasing partial derivatives (def. \ref{FunctionsWithRapidlyDecreasingPartialDerivatives}).

For example the function $f \colon \mathbb{R} \to \mathbb{R}$

$$
  f(x) \coloneqq e^{-x^2}\sin(e^{x^2})
$$ 

is rapidly decreasing, but its first [[derivative]]

$$
  f'(x) = -2xe^{-x^2}\sin(e^{x^2})+2x\cos(e^{x^2})
$$

is asymptotically linearly increasing, due to the second term.

=--


## Related concepts

* [[continuous function]], [[differentiable function]], [[smooth function]]

* [[integrable function]], [[square-integrable function]]

* [[bounded function]]

* [[compactly supported function]]

* [[measurable function]]


[[!redirects rapidly decreasing functions]] 

[[!redirects rapidly decaying function]]
[[!redirects rapidly decaying functions]]

[[!redirects function with rapidly decreasing partial derivatives]]
[[!redirects functions with rapidly decreasing partial derivatives]]

[[!redirects function with rapidly decaying partial derivatives]]
[[!redirects functions with rapidly decaying partial derivatives]]


[[!redirects Schwartz function]]
[[!redirects Schwartz functions]]
