
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

The terms *epivalence* ([Keller 1990 p. 18](#Keller1990)), *detecting functor* ([Baues 1995](#Baues1995)) and *smothering functor* ([Riehl & Verity 2015](#RiehlVerity2015))
refer to [[functors]] that are at least close to be "[[equivalences of categories]]" except that they may not be [[faithful functor|faithful]]. 

Smothering functors tend to arise when comparing "different [[homotopy categories]]" of the same category that impose more or less refined notions of [[homotopy equivalence]].  Frequently they can be treated more or less like equivalences.

## Definition

A functor $F:C\to D$ is **smothering** if it is

1. [[surjective on objects functor|surjective on objects]],
1. [[full functor|full]], and
1. [[conservative functor|conservative]].

If instead of being surjective on objects $F$ is [[essentially surjective]] on objects, we may say that $F$ is **weakly smothering**.

## Properties

* Each (strict) [[fiber]] of a smothering functor is an [[inhabited]] [[connected]] [[groupoid]]. ([RV, 3.3.2](#RV))
* If $F:C\to D$ is smothering and $x,y\in C$ satisfy $F x \cong F y$ in $D$, then $x \cong y$ in $C$, by fullness combined with conservativity.  In other words, $F$ is "full on isomorphisms" (but since it is not faithful, it is not [[pseudomonic]]).
* Further combining this with surjectivity on objects, every smothering functor is an [[isofibration]].

## Examples

* For any [[model category]] $C$, the functor $Ho(C^{\mathbf{2}}) \to Ho(C)^{\mathbf{2}}$ is weakly smothering, where $\mathbf{2}$ denotes the [[interval category]].  This property appears in the axiom (Der5) for [[derivators]].

## Related pages

* [[smothering 2-functor]]

* [[derivator]]

## References

Use of the term *epivalence*:

* {#Keller1990} [[Bernhard Keller]]; p. 18 of: *Chain Complexes and Stable Categories*, Manus. Math. **67** (1990) 379--417 &lbrack;[doi:10.1007/BF02568439](https://doi.org/10.1007/BF02568439), [pdf](https://webusers.imj-prg.fr/~bernhard.keller/publ/csc.pdf)&rbrack;

Use of the term "detecting functor":

* {#Baues1995} [[Hans-Joachim Baues]]; p. 25 of: _Homotopy types_, in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_, North Holland (1995) \[<a href="https://doi.org/10.1016/B978-0-444-81779-2.X5000-7">doi:10.1016/B978-0-444-81779-2.X5000-7</a>, [ISBN:9780080532981](https://www.elsevier.com/books/handbook-of-algebraic-topology/james/978-0-444-81779-2), [[Baues-HomotopyTypes.pdf|pdf:file]]\]


Use of the term *smothering functor*:

* {#RiehlVerity2015} [[Emily Riehl]], [[Dominic Verity]]: _The 2-category theory of quasi-categories_, Advances in Mathematics **280** (2015) 549--642 &lbrack;[arXiv:1306.5144](http://arxiv.org/abs/1306.5144)&rbrack;

Discussion of Examples:

* [[Claus Michael Ringel]]; section 1 of: *On the representation dimension of Artin algebras* &lbrack;[pdf](https://www.math.uni-bielefeld.de/~ringel/opus/repdim2.pdf)&rbrack;


[[!redirects epivalence]]
[[!redirects epivalences]]

[[!redirects detecting functor]]
[[!redirects detecting functors]]

[[!redirects smothering functors]]

[[!redirects weakly smothering functor]]
[[!redirects weakly smothering functors]]




