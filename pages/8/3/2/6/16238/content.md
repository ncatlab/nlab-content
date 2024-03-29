## Idea

This entry is about the notion of [[module]] or [[quasi-coherent sheaf|quasi-coherent]] [[chain complex|complexes]] in the setting of [[higher geometry]] and more specifically, [[E-infinity geometry]] and [[derived algebraic geometry]].

In this setting, modules are already derived, in the sense that modules over an ordinary [[scheme]] or [[stack]], viewed as a discrete [[derived scheme]] or [[derived stack]], are [[complexes]] of [[quasi-coherent sheaves]].

## Definition

Let $Sch^{aff}$ and $Stk$ denote the [[(infinity,1)-categories]] of affine [[derived schemes]] and [[derived stacks]], respectively.
Consider the [[(infinity,1)-prestack]] of [[stable (infinity,1)-categories]]
  $$ Mod : (Sch^{aff})^{op} \to Cat^{stab}_\infty $$
which associates to a [[commutative ring spectrum]] $A$ the [[stable (infinity,1)-category]] $Mod(A)$.

By taking the [[right Kan extension]] of this prestack along the ([[opposite (infinity,1)-category|opposite]] of the) [[Yoneda embedding]]
  $$ (Sch^{aff})^{op} \hookrightarrow Stk^{op}, $$
one gets an [[(infinity,1)-prestack]]
  $$ Mod : Stk^{op} \to Cat^{stab}_\infty. $$
In other words, for a derived stack $X$, $Mod(X)$ is given by the [[limit in an (infinity,1)-category|limit]]
  $$ Mod(X) = lim_{Spec(A) \to X} Mod(A). $$

## In ordinary algebraic geometry

In the case of ordinary [[affine schemes]], [[modules]] in this sense, i.e. [[modules]] over [[Eilenberg-Mac Lane spectra]], correspond by the [[stable Dold-Kan correspondence]] to [[chain complexes]].  The corresponding notion of module over an ordinary [[scheme]] or [[stack]] is then a _quasi-coherent complex_.
That is, for a [[commutative ring]] $A$,
  $$ Mod(H A) = D(Mod(A)) $$
(the [[derived category]] of [[chain complexes]] of $A$-[[modules]]), and for a classical [[scheme]] $X$,
  $$ Mod(X) = D(QCoh(A)) $$
(the [[derived category]] of [[chain complexes]] of [[quasi-coherent sheaves]]).

## Properties

The [[(infinity,1)-prestack]] $Mod$ satisfies [[Zariski descent]] and even [[Nisnevich descent]]; this is due to [[Jacob Lurie]] and [[Vladimir Drinfeld]].

$Mod$ lifts to a prestack of [[symmetric monoidal (infinity,1)-categories]].  The [[dualizable objects]] are precisely the [[perfect modules]].
In good cases, the [[stable (infinity,1)-category]] $Mod(X)$ is [[compactly generated (infinity,1)-category|compactly generated]] and the [[compact objects]] are precisely the [[perfect modules]].

## Related concepts

* [[perfect module]]
* [[triangulated categories of sheaves]]

## References

* [[Dennis Gaitsgory]], _[[Notes on geometric Langlands]]: quasi-coherent sheaves_.

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical algebraic geometry II: geometric stacks and applications_, 2004, [arXiv:math/0404373](http://arxiv.org/abs/math/0404373).

* [[Jacob Lurie]], [[Derived Algebraic Geometry]], thesis, [pdf](http://www.math.harvard.edu/~lurie/papers/DAG.pdf).

* {#BFN08} [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], section 3.1 of _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry_, J. Amer. Math. Soc. 23 (2010), no. 4, 909-966 ([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))

* [[B. Toen]], _Derived Azumaya algebras and generators for twisted derived categories_, [arXiv:1002.2599](http://arxiv.org/abs/1002.2599).

[[!redirects module over a derived stack]]
[[!redirects modules over a derived stack]]
[[!redirects modules over derived stacks]]
[[!redirects module over a derived scheme]]
[[!redirects modules over a derived scheme]]
[[!redirects modules over derived schemes]]

[[!redirects module over a stack]]
[[!redirects modules over a stack]]
[[!redirects modules over stacks]]
[[!redirects module over a scheme]]
[[!redirects modules over a scheme]]
[[!redirects modules over schemes]]

[[!redirects quasi-coherent complex over a stack]]
[[!redirects quasi-coherent complexes over a stack]]
[[!redirects quasi-coherent complexes over stacks]]
[[!redirects quasi-coherent complex over a scheme]]
[[!redirects quasi-coherent complexes over a scheme]]
[[!redirects quasi-coherent complexes over schemes]]
