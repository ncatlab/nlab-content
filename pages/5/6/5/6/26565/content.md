
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

A function between measure or probability spaces is called *measure-preserving* if its preimages preserve the measures of subsets.

Measure-preserving functions are closed under composition, hence they form a category. When the objects are probability spaces, the category is usually denoted by *Prob*.

## Definition

Let $(X,\mathcal{A},p)$ and $(Y,\mathcal{B},q)$ be [[probability spaces]]. 
A function $f:X\to Y$ is called 

* [[measurable function|measurable]] if for every $B\in\mathcal{B}$, $f^{-1}(B)\in\mathcal{A}$ ;
* **measure-preserving** if it is measurable, and moreover for every $B\in\mathcal{B}$,
$$
p(f^{-1}(B)) = q(B) .
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