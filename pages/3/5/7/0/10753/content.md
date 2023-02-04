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

### Propositions as types

In the [[propositions as types]] interpretation of [[type theory]], every pointed type represents a [[true]] [[proposition]]. Contrast this to an inhabited type, which only represents the [[double negation]] of a true proposition. 

## Type of pointed types

For a given type universe $\mathcal{U}$ the type of pointed types is

$$\mathcal{U}_+\equiv \sum_{X:\mathcal{U}}X$$ 

## Related entries

* [[maybe monad]]

* [[loop space type]]

* [[reduced suspension type]]

* [[prespectrum type]]


## References

* [[Univalent Foundations Project]], [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* [[Martín Escardó]], *[Pointed types](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html#pointed-types)*, §33.5 in: *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580),  [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html)&rbrack;




[[!redirects pointed types]]