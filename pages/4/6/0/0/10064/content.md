33
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An _iterated integral_ is a expression involving nested [[integrals]], such as
$$ \int_{x=a}^b \bigg(\int_{y=g(x)}^{h(x)} f(x,y) \,\mathrm{d}y\bigg) \,\mathrm{d}x ,$$
where the grouping parentheses are usually left out.  Iterated integrals are the subject of [[Fubini theorem]]s.

Iterated integrals include nested [[integration of differential forms]] of the kind as it appears in the formulation of [[parallel transport]] for nonabelian-value [[connection on a bundle|connection]] form (known as the _[[Dyson formula]]_ in [[physics]]).

Applied to higher degree forms iterated integrals serve to express generalized [[transgression]] of differential forms to [[loop spaces]] and other [[mapping spaces]] realized as [[diffeological spaces]].

## Related concepts

* [[Dyson formula]]

* [[Chen connection]]

* [[higher holonomy]]

* [ordinary homology -- description in terms of higher linear algebra](ordinary%20homology#InTermsOfHigherLinearAlgebra)


## References

The notion of iterated integration of differential forms originates in informal observation like the [[Dyson formula]] for [[parallel transport]]. It was formalized in the context of [[differential geometry]] on [[diffeological spaces]] ([[Chen spaces]]) (especially [[loop spaces]]) in 

* [[Kuo Tsai Chen]], _Iterated integrals of differential forms and loop space homology_, Ann. Math. __97__ (1973), 217&#8211;246. [JSTOR](http://www.jstor.org/stable/1970846)

* [[Kuo Tsai Chen]], _Iterated integrals, fundamental groups and covering spaces_, Trans. Amer. Math. Soc. __206__ (1975) 83--98. [doi:10.1090/S0002-9947-1975-0377960-0](https://doi.org/10.1090/S0002-9947-1975-0377960-0)

* [[Kuo Tsai Chen]], _Iterated path integrals_. Bull. Amer. Math. Soc. __83__(5):831--879, 1977 [doi:10.1090/S0002-9904-1977-14320-6](https://doi.org/10.1090/S0002-9904-1977-14320-6)

Essentially these formulas are used in 

* [[Kiyoshi Igusa]], _Iterated integrals of superconnections_ ([arXiv:0912.0249](https://arxiv.org/abs/0912.0249))

for expressing [[higher holonomy]] of certain [[flat infinity-connections]] given by [[Lie infinity-algebroid representation|infinity-representations]] of [[tangent Lie algebroids]].

A review of this and more discussion in the context of a higher [[Riemann-Hilbert correspondence]] is in 

* [[Jonathan Block]], Aaron Smith, _A Riemann--Hilbert correspondence for infinity local systems_ ([arXiv:0908.2843](https://arxiv.org/abs/0908.2843))

A relation to [[algebraic cycles]] is discussed in 

* [[Richard Hain]], _Iterated integrals and algebraic cycles: examples and prospects_ ([arXiv:math/0109204](https://arxiv.org/abs/math/0109204))

Chen iterated integrals in the context of stochastic analysis

* Terry J. Lyons,_ Differential equations driven by rough signals_, Rev. Mat. Iberoamericana __14__(2):215--310, 1998 [pdf](https://ems.press/content/serial-article-files/37943)

[[!redirects iterated integral]]
[[!redirects iterated integrals]]
[[!redirects Chen integral]]
[[!redirects Chen iterated integral]]