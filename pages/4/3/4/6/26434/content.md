# Contents

{: toc}

## Idea

Unlike a monadic bind which has the following type
$$(\forall\alpha)(\forall\beta)(m\alpha\to(\alpha\to m\beta)\to m\beta)$$
a polymonadic bind involves three abstract types.
$$(\forall\alpha)(\forall\beta)(m_1\alpha\to(\alpha\to m_2\beta)\to m_3\beta)$$

It subsumes monads in the sense that every set of monads and monad morphisms can be encoded using polymonads while obeying the polymonad laws. Moreover, it encompasses the monad-like programming patterns.

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

* Nataliya Guts, Michael Hicks, Nikhil Swamy, Daan Leijen, and Gavin Bierman, _Polymonads_, Extended version of POPL'13 submission.
* Jan Bracker, and Henrik Nilsson, _Polymonad programming in Haskell_, Proceedings of the 27th Symposium on the Implementation and Application of Functional Programming, (2015) 1-12 ([doi:10.1145/2897336.2897340](https://dl.acm.org/doi/10.1145/2897336.2897340)).

[[!redirects polymonad]]
[[!redirects polymonads]]
