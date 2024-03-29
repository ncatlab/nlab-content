
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

The _completion monad_ is a [[monad (in computer science)]] which is used for _exact_ computations with [[real numbers]], in the sense of [[constructive analysis]]. It has been used for [[certified programming]] with guaranteed exactness of real number approximations.

## References

The completion monad was introduced in

* [[Russel O'Connor]], _A Monadic, Functional Implementation of Real Numbers_ MSCS, 17(1):129-159, 2007 ([arXiv:cs/0605058](http://arxiv.org/abs/cs/0605058))

and implemented in [[Coq]] in

* [[Russel O'Connor]], _Certified Exact Transcendental Real Number Computation in Coq_ In TPHOLs 2008, volume 5170 of LNCS, pages 246261, 2008.

For more see

* Robbert Krebbers, [[Bas Spitters]], _Type classes for efficient exact real arithmetic in Coq_ ([arXiv:1106.3448](http://arxiv.org/abs/1106.3448/))