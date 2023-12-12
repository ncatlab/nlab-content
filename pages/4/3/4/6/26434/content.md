
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


# Contents

\tableofcontents

## Idea

Unlike the [[extension system|bind operation]] of a [[monad]] which is of type
$$
  (\forall\alpha)
  (\forall\beta)
  \big(
    m\alpha \to (\alpha\to m\beta) \to m\beta
  \big)
$$
a *polymonadic bind* involves three abstract types:
$$
  (\forall\alpha)
  (\forall\beta)
  \big(
    m_1\alpha\to(\alpha\to m_2\beta)\to m_3\beta
  \big)
  \,.
$$

This notion subsumes monads in the sense that every set of monads and monad morphisms can be encoded using polymonads while obeying the polymonad laws. Moreover, it encompasses the [[monad (in computer science)|monad-like programming patterns]].

## Definition

A polymonad is the data of a collection $\mathcal{M}$ of unary type constructors cointaining an element $\mathrm{Id}$, and a bind set $\Sigma_{\mathcal{M}}$ containing an element $b_{\mathrm{Id},\mathrm{Id},\mathrm{Id}}$ (reverse apply).

It must obey the following polymonad laws:

* functorial law;
* left identity;
* right identity;
* associativiy;
* paired morphisms law;
* composition closure law.

The first four laws are chosen to generalise monads, and the last two are chosen so that if certain binds can be uniquely defined in terms of other ones, then these must be present in $\Sigma$.

## Examples

* [[Hoare monad]]

* [[effect monad]]

## References

* Nataliya Guts, [[Michael Hicks]], Nikhil Swamy, Daan Leijen, [[Gavin Bierman]], _Polymonads_, Extended version of POPL'13 submission &lbrack;[pdf](https://www.cs.umd.edu/~mwh/papers/polymonadsTR.pdf), [[GHSLB-Polymonads.pdf:file]]&rbrack;

* [[Michael Hicks]], [[Gavin Bierman]], Nataliya Guts, Daan Leijen, Nikhil Swamy, *Polymonadic Programming*, EPTCS **153** 79-99 (2014) &lbrack;[arXiv:1406.2060](https://arxiv.org/abs/1406.2060), [doi:10.4204/EPTCS.153.7](https://doi.org/10.4204/EPTCS.153.7)&rbrack;

* Jan Bracker, Henrik Nilsson, _Polymonad programming in Haskell_, Proceedings of the 27th Symposium on the Implementation and Application of Functional Programming, (2015) 1-12 &lbrack;[doi:10.1145/2897336.2897340](https://dl.acm.org/doi/10.1145/2897336.2897340)&rbrack;

[[!redirects polymonad]]
[[!redirects polymonads]]
