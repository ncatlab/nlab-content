
# Floors and ceilings
* table of contents
{: toc}

## Idea

The floor and ceiling of a [[real number]] are [[integers]], the result of rounding the real number down or up (respectively).  When viewed as [[functions]] from $\mathbb{R}$ to itself (or to $\mathbb{Z}$), these are standard examples of functions exhibiting partial notions of [[continuity]]: the floor function is both [[right-continuous map|right-continuous]] and [[upper semicontinuous map|upper semicontinuous]], while the ceiling function is both [[left-continuous map|left-continuous]] and [[lower semicontinuous map|lower semicontinuous]].  They are [[step functions]] used to approximate definite [[integrals]] of [[continuous maps]] and otherwise to relate integrals and [[series]].  They provide convenient notation to express various notions of [[rounding]].  From the perspective of [[order theory]], the maps may be seen as the [[right adjoint]] and [[left adjoint]] (respectively) of the [[inclusion map]] from $\mathbb{Z}$ to $\mathbb{R}$.


## Definitions

Given a [[real number]] $x$, the __floor__ of $x$, denoted $\lfloor{x}\rfloor$ or $[x]$, is the largest integer $n$ such that $n \leq x$, and the __ceiling__ of $x$, denoted $\lceil{x}\rceil$, is the smallest integer $n$ such that $n \geq x$.

Typically the notation $\lfloor{x}\rfloor$ is used when both floor and ceiling appear, but $[x]$ is often easier when only the floor is considered.  Since
$$ \lceil{x}\rceil = -\lfloor{-x}\rfloor ,$$
this is not actually a restriction.

The floor of $x$ is also called the __integer part__ of $x$, and then one refers as well to the __fractional part__ of $x$, denoted $\{x\}$, defined by
$$ \{x\} = x - [x] .$$

One must of course prove that the floor of $x$ exists; this fails in [[constructive mathematics]], although the floor of $x$ exists for [[full set|almost all]] $x$, and all of these functions can still be defined as continuous maps between appropriate [[locales]].


## References

Wikipedia summarizes the basic properties:

* English Wikipedia. Floor and ceiling functions. [Web](https://en.wikipedia.org/wiki/Floor_and_ceiling_functions).

I ([[Toby Bartels]]) use the floor and ceiling functions to relate integrals and series when teaching Calculus; see throughout Chapter 3 of these notes (soon to be replaced by an updated version):

* Toby Bartels. One-variable Calculus for Calculus 2. [Web](http://tobybartels.name/MATH-1700/2017WN/calcbook/) (the first set of notes at that link).


[[!redirects floor]]
[[!redirects floors]]
[[!redirects floor operation]]
[[!redirects floor operator]]
[[!redirects floor function]]
[[!redirects floor functor]]
[[!redirects floor map]]
[[!redirects floor mapping]]

[[!redirects ceiling]]
[[!redirects ceilings]]
[[!redirects ceiling operation]]
[[!redirects ceiling operator]]
[[!redirects ceiling function]]
[[!redirects ceiling functor]]
[[!redirects ceiling map]]
[[!redirects ceiling mapping]]
