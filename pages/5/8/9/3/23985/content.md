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

## Idea

In [[dependent type theory]], and particularly [[homotopy type theory]], an **identification** is a word sometimes used for an inhabitant of an [[identity type]]. Alternatives to the term identification include **[[identity]]**, **[[path]]**, or **[[equality]]**, though those phrases are also used in different contexts. 

Thus an identification $p:\mathrm{Id}(a, b)$ provides a "reason", a "witness", or a "proof" that $a$ and $b$ "are equal", or more precisely a *way in which to identify them*. one can say that $a$ and $b$ are **identified**. The distinguishing feature of homotopy type theory is that in general, there may be more than one way to identify two things, i.e. more than one identification between two given elements.

## $n$-ary identifications

One also has [[identity type#ForAFamilyOfElements|identity types for a family of elements]] $\mathrm{Id}_{I, A}(\overline{x})$ indexed by $\overline{x}:I \to A$ given index type $I$, instead of the usual identity types for two elements $\mathrm{Id}_A(x, y)$. The elements of these identity types are also called **identifications**. 

If the index type $I$ is the standard [[finite type]] with $n$ elements $\mathrm{Fin}(n) \coloneqq \sum_{m:\mathbb{N}} m \lt n$, then $\mathrm{Id}_{A}(\overline{x})$ is called the [[n-ary identity type]] and elements of said type can be called **$n$-ary identifications**. For $n = 2$, these result in the usual notion of **binary identificaiton**. 

## See also

* [[function application to identities]]
* [[transport]]
* [[unique identification]]
* [[bridge]]

## References ##

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* [[Univalent Foundations Project]], [[Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

[[!redirects identification]]
[[!redirects identifications]]

[[!redirects identified]]

[[!redirects binary identification]]
[[!redirects binary identifications]]

[[!redirects n-ary identification]]
[[!redirects n-ary identifications]]