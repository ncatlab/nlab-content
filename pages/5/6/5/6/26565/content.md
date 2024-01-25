
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A [[function]] between [[measure space|measure-]] or [[probability spaces]] is called *measure-preserving* if its [[preimages]] preserve the measures of subsets.

Such measure-preserving functions are closed under [[composition]], hence they constitute the [[morphisms]] of a [[category]] whose [[objects]] are [[measure spaces]]. When restricted to [[objects]] that are [[probability spaces]], the category is usually denoted by *Prob*.

## Definition

Let $(X,\mathcal{A},p)$ and $(Y,\mathcal{B},q)$ be [[probability spaces]]. 

A function $f \colon X\to Y$ is called 

* *[[measurable function|measurable]]* if for every $B\in\mathcal{B}$ we have $f^{-1}(B)\in\mathcal{A}$;

* *measure-preserving* if it is measurable, and moreover for every $B\in\mathcal{B}$,

   $$
     p\big(f^{-1}(B)\big) \,=\, q(B) 
     \,.
   $$

The [[category]] *Prob* has 
 
* as [[objects]], [[probability spaces]];

* as [[morphisms]], measure-preserving functions.


## Related concepts

* [[probability space]]

* [[Markov kernel]]

* [[measurable function]]

* [[category of couplings]]

* [[categorical probability]]

* [[entropy]]


category: category


[[!redirects measure-preserving map]]
[[!redirects measure-preserving maps]]
[[!redirects measure preserving map]]
[[!redirects measure preserving maps]]
[[!redirects measure-preserving function]]
[[!redirects measure-preserving functions]]
[[!redirects measure preserving function]]
[[!redirects measure preserving functions]]