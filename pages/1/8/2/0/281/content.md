
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Definition


An __automorphism__ of an [[object]] $x$ in a [[category]] $C$ is an [[isomorphism]] $f : x \to x$.  In other words, an automorphism is an [[endomorphism]] that is an [[isomorphism]].


## Automorphism group

Given an object $x$, the automorphisms of $x$ form a [[group]] under [[composition]], the __automorphism group__ of $x$, which is a submonoid of the [[endomorphism monoid]] of $x$:
$$
  Aut_C(x) = End_C(x) \cap Iso(C) = Iso_C(x,x)
,$$
which may be written $Aut(x)$ if the category $C$ is understood.  Up to equivalence, every group is an automorphism group; see [[delooping]].

## Examples

(...)

* [[permutation|Permutations]] are automorphisms in [[FinSet]]. 

* [[automorphism of a vertex operator algebra]]


## Related concepts

* **automorphism group**

  * [[inner automorphism group]]

  * [[outer automorphism group]]

  * [[automorphism Lie group]]

* [[automorphism 2-group]]

* [[automorphism ∞-group]]


## References

Discussion of automorphism groups [[internalization|internal]] to [[sheaf toposes]] ("automorphism sheaves"):

* [[Simon Henry]], [MO:a/262687](https://mathoverflow.net/a/262687/381)

* Robert Friedman, John W. Morgan, §2.1 in: *Automorphism sheaves, spectral covers, and the Kostant and Steinberg sections* &lbrack;[arXiv:math/0209053](https://arxiv.org/abs/math/0209053)&rbrack;


[[!redirects automorphisms]]
[[!redirects automorphism group]]
[[!redirects automorphism groups]]

[[!redirects group of automorphisms]]
[[!redirects groups of automorphisms]]
