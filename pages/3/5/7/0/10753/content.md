+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

##Idea

A **pointed type** is a [[type]] equipped with a [[term]] of that type.

The [[categorical semantics]] is a [[pointed object]].

## Properties

There is a way of pointing any type $X$ by forming the sum $X+\mathbf{1}$ and taking $inr(\star_{\mathbf{1}})$ as the base point. 

## Type of pointed types

For a given type universe $\mathcal{U}$ the type of pointed types is

$$\mathcal{U}_+\equiv \sum_{X:\mathcal{U}}X$$ 

## Related entries

* [[maybe monad]]

* [[loop space type]]

* [[prespectrum type]]

* [[suspension type]]

## References

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects pointed types]]