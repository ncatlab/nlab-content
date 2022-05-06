+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Homotopical algebraic geometry_ is a [[homotopy theory|homotopical]] generalization of [[algebraic geometry]], where the [[affine schemes]] are not necessarily [[commutative algebras]] in the usual sense, but rather [[commutative algebra in an (∞,1)-category|commutative algebra objects]] in an arbitrary [[symmetric monoidal (infinity,1)-category]].
In other words, it is the specialization of [[higher geometry]] where the local models are [[commutative algebra in an (∞,1)-category|commutative algebras]] in a [[symmetric monoidal (infinity,1)-category]].

Interesting examples can be obtained by starting with

* the ordinary category of [[sets]] (yielding ordinary [[algebraic geometry]])
* the [[(infinity,1)-category]] of [[simplicial commutative rings]] (yielding [[derived algebraic geometry]]),
* the [[(infinity,1)-category of spectra]] (yielding [[spectral algebraic geometry]]).

As in ordinary [[algebraic geometry]], there are two equivalent definitions of [[scheme]]: the so-called [[functor of points]] approach, or the approach via [[locally ringed toposes]]; we consider the former approach below.

## Definition

Given a [[symmetric monoidal (infinity,1)-category]] $C$, let $CAlg(C)$ denote the [[(infinity,1)-category]] of [[commutative algebra in an (∞,1)-category|commutative algebra objects]] in $C$.

+-- {: .num_defn}
###### Definition
A **$C$-prestack** is an [[infinity-prestack]] on the [[opposite (infinity,1)-category]] of $CAlg(C)$.
In other words it is a functor $CAlg(C) \to Spc$ to the [[(infinity,1)-category of spaces]].
=--

Let $\tau$ be a subcanonical [[Grothendieck topology]] on $CAlg(C)^{op}$.

+-- {: .num_defn}
###### Definition
A **$(C,\tau)$-stack** is an [[infinity-stack]] on the [[opposite (infinity,1)-category]] of $CAlg(C)$, with respect to the topology $\tau$.
Let $Stk(C, \tau)$ denote the [[(infinity,1)-category]] of $(C,\tau)$-stacks.
The [[Yoneda embedding]] is denoted
  $$ Spec : CAlg(C) \hookrightarrow Stk(C,\tau) $$
and a stack is called **affine** if it is in the [[essential image]].
=--

Let $P$ be a class of morphisms in $Stk(C, \tau)$ which is stable by [[base change]].
The triple $(C, \tau, P)$ is a called a **homotopical algebraic geometry context** (*HAG context*).

+-- {: .num_defn}
###### Definition
A **$(C,\tau, P)$-scheme** is a $(C,\tau)$-stack $X$ such that there exists a family of morphisms $(X_\alpha \to X)_\alpha$, each in $P$, such that $X_\alpha$ are affine and the induced morphism
  $$ \coprod_\alpha X_\alpha \longrightarrow X $$
is an [[epimorphism]].
Let $Sch(C, \tau, P)$ denote the [[(infinity,1)-category]] of $(C,\tau,P)$-schemes.
=--

## Related concepts

* [[derived algebraic geometry]]
* [[spectral algebraic geometry]]

## References

* [[Jacob Lurie]], [[Derived Algebraic Geometry]], thesis, [pdf](http://www.math.harvard.edu/~lurie/papers/DAG.pdf).

* [[Jacob Lurie]], [[Structured Spaces]].

An alternate exposition of the theory, using the presentations by [[model categories]] (hence the various [[model structures on simplicial presheaves]]), is given in

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical algebraic geometry I: topos theory_, 2002, [arXiv:math/0207028](http://arxiv.org/abs/math/0207028).

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical algebraic geometry II: geometric stacks and applications_, 2004, [arXiv:math/0404373](http://arxiv.org/abs/math/0404373).

An exposition in the style of To&#235;n-Vezzosi but in the language of [[(infinity,1)-categories]] can be found in

* [[Mauro Porta]], Tony Yue Yu, _Higher analytic stacks and GAGA theorems_, [arXiv:1412.5166](http://arxiv.org/abs/1412.5166).

For an extension of homotopical algebraic geometry from $\infty$-stacks valued in $Spc$ to those valued in augmentation categories, a special class of [[generalized Reedy categories]], see.

* Scott Balchin, _Augmented Homotopical Algebraic Geometry_, ([arXiv:1711.02640](https://arxiv.org/abs/1711.02640))
