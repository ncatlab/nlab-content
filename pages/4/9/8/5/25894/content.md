
> This is about the notion of *path category* in [[model category theory]] and [[homotopy theory]]. For the notion of path category in ordinary category theory, see [[path category]].

----

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

\tableofcontents

## Definition

A **category with path objects** or a **path category** is a [[category]] $\mathcal{C}$ with two sets of morphisms called [[weak equivalences]] and [[fibrations]] in which

1. Fibrations are closed under composition
1. The pullback of a fibration along any other map exists and is again a fibration.
1. The pullback of an [[acylic fibration]] along any other map is again an acyclic fibration.
1. Weak equivalences satisfy the 2-out-of-6 property: if $f:A \to B$, $g:B \to C$, $h:C \to D$ are
three composable maps and both $g \circ f$ and $h \circ g$ are weak equivalences, then so are $f$, $g$, $h$ and $h \circ g \circ f$.
1. Isomorphisms are acyclic fibrations and every acyclic fibration has a section.
1. For any object $B$ there is a path object $P B$ (not necessarily functorial in $B$).
1. $\mathcal{C}$ has a terminal object $1$ and every map $X \to 1$ to the terminal object is a fibration.

## Examples

* The [[syntactic category]] associated to a [[dependent type theory]] with [[identity types]] is a category with path objects. 

* Given a [[Quillen model category]] $\mathcal{C}$ in which every object is cofibrant, the [[full subcategory]] of fibrant objects in $\mathcal{C}$ is a category with path objects. 

* The category of [[topological spaces]] is a category with path objects where the [[homotopy equivalences]] are the weak equivalences and the [[Hurewicz fibrations]] are the the fibrations. 

* A [[finitely complete category]] is a category with path objects in which every morphism is a fibration and only the [[isomorphisms]] are [[weak equivalences]].

## See also

* [[category of fibrant objects]]

* [[homotopy exact completion]]

## References

* {#vdBergMoerdijk18} [[Benno van den Berg]], [[Ieke Moerdijk]], *Exact completion of path categories and algebraic set theory: Part I: Exact completion of path categories*, Journal of Pure and Applied Algebra **222** 10 (2018) 3137-3181 &lbrack;[doi:10.1016/j.jpaa.2017.11.017](https://doi.org/10.1016/j.jpaa.2017.11.017), [arXiv:1603.02456](https://arxiv.org/abs/1603.02456)&rbrack;

* {#vdBergBesten21} [[Benno van den Berg]], [[Martijn den Besten]], *Quadratic type checking for objective type theory* ([arXiv:2102.00905](https://arxiv.org/abs/2102.00905))

[[!redirects category with path objects]]
[[!redirects categories with path objects]]