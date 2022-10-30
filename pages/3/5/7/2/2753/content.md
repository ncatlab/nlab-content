

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


# Contents #
* table of contents
{:toc}


## Idea

The notion of _Lie--Rinehart pair_ is an algebraic encoding of the notion of _[[Lie algebroid]]_.  It is the pair consisting of the [[associative algebra]] of [[functions]] on the base space of the Lie algebroid and of the [[Lie algebra]] of its global [[sections]]. The [[anchor map]] of the Lie algebroid is encoded in the [[action]] of the Lie algebra on the associative algebra by [[derivations]] and the local structure is encoded in the Lie algebra being a [[module]] over the associative algebra.

Since in this formulation the base manifold of the Lie algebroid is entirely described [[Isbell duality|dually]] in terms of its [[algebra of functions]], and since the definition does not refer to this being a _commutative_ algebra, the notion of Lie-Rinehart pair in fact generalizes the notion of Lie algebroid from ordinary [[differential geometry]] to [[noncommutative geometry]].

## Definition

A _Lie--Rinehart-pair_ $(A,\mathfrak{g})$ is a pair consisting of 

1. an [[associative algebra]] $A$ 

1. a [[Lie algebra]] $\mathfrak{g}$ 

such that 

1. $A$ is a $\mathfrak{g}$-[[module]] 

1. $\mathfrak{g}$ is an $A$-[[module]]

with both module structures being compatible in the obvious way:

1. $\mathfrak{g}$ acts as [[derivations]] of $A$: that is, we have a Lie algebra [[homomorphism]] $\mathfrak{g} \to Der(A)$. 

1. $A$ acts as linear transformations of $\mathfrak{g}$ in a way obeying the [[Leibniz rule]]: that is, we have an associative algebra homomorphism from $A \to End(\mathfrak{g})$, where $End(\mathfrak{g})$ is the algebra of all linear transformations of $\mathfrak{g}$, such that
$$  [v, a w] = v(a) w + a [v,w]. $$ 


## Examples

In the case that $A = C^\infty(X)$ is the algebra of smooth functions on a smooth [[manifold]] $X$, Lie--Rinehart pairs $(C^\infty(X), \mathfrak{g})$ are naturally identified with [[Lie algebroid]]s over $X$: given the [[Lie algebroid]] in its incarnation as a [[vector bundle]] morphism

$$
  \array{
     E &&\stackrel{\rho}{\to}&& T X
     \\
     & \searrow && \swarrow
     \\
     && X 
  }
$$

equipped with a bracket 

$$
  [-,-] : \Gamma(E) \otimes\Gamma(E) \to \Gamma(E)
$$

we obtain a Lie--Rinehart pair by setting

* $\mathfrak{g} = \Gamma(E)$ is the [[Lie algebra]] of [[sections]] of $E$ using the above bracket

* the action of $A$ on $\mathfrak{g}$ is the obvious multiplication of sections of vector bundles over $X$ by functions on $X$

* the action of $\mathfrak{g}$ on $C^\infty(X)$ is given by first applying the anchor map $\rho$ and then using the canonical action of vector fields on functions.

So for all the examples listed at [[Lie algebroid]] we obtain an example for Lie--Rinehart pairs.

In particular

* the Lie--Rinehart pair coresponding to the [[tangent Lie algebroid]] of a [[manifold]] $X$ is $(C^\infty(X), \Gamma(T X))$ with the obvious action on each other.

* the Lie--Rinehart pair corresponding to an ordinary [[Lie algebra]] $\mathfrak{g}$ is $(\mathbb{R}, \mathfrak{g})$ with $\mathfrak{g}$ acting trivially on $\mathbb{R}$.

* the Lie--Rinehart pair corresponding to a [[Poisson Lie algebroid]] on a [[Poisson manifold]] $X$ is $(C^\infty(X), MultVect(X))$, where the [[Lie algebra]] is the the space of [[multivector fields]] on $X$ equipped with the [[Schouten bracket]]. 

In [open-closed string field theory](string%20field%20theory#OpenClosedStringFieldTheory) one finds at least one half of the axioms of homotopy Lie-Rinehart pairs.


## Generalizations 

A little bit is known in the literature to generalizations of the notion of Lie--Rinehart algebras that are to [[Lie ∞-algebroids]] as the latter are to [[Lie algebroids]].

In 

* [[Dmitry Roytenberg]], _Courant--Dorfman algebras and their cohomology_ ([arXiv](http://arxiv.org/abs/0902.4862))

the analogous algebraic structure for [[Courant algebroid]]s is discussed. These "2-Lie--Rinehart algebras" are called [[Courant?Dorfman algebra]]s there.


## Related concepts

* [[bisections of a Lie groupoid]]

## References

The original reference is

* G. Rinehart, _Differential forms for general commutative algebras_, Trans. Amer. Math. Soc. __108__ (1963), 195-222

A brief review in section 1 of

* [[Johannes Huebschmann]], _Lie--Rinehart algebras, descent, and quantization_ ([arXiv](http://arxiv.org/abs/math/0303016))

* [[Mikhail Kapranov|M. Kapranov]], _Free Lie algebroids and the space of paths_,	Sel. Math. (N.S.) __13__, n. 2 277--319 (2007), [arXiv:math.AG/0702584](http://arxiv.org/abs/math.AG/0702584), [doi](http://dx.doi.org/10.1007/s00029-007-0041-9)

* V. Nistor, A. Weinstein, P. Xu, _Pseudodifferential operators on differential groupoids_, Pacific J. Math. __189__, 117&#8211;152 (1999)

A notion of universal enveloping algebra of a Lie--Rinehart algebra is discussed in

* [[Ieke Moerdijk]], [[Janez Mr?un]], _On the universal enveloping algebra of a Lie--Rinehart algebra_, Proc. Amer. Math. Soc. in press, ([pdf](http://www.ams.org/proc/0000-000-00/S0002-9939-10-10347-5/S0002-9939-10-10347-5.pdf), [arXiv/0801.3929](http://arxiv.org/abs/0801.3929))

A connection with [[BV-theory]] is made in

* [[Johannes Huebschmann]], _Lie--Rinehart algebras, Gerstenhaber algebras and Batalin-Vilkovisky algebras_ ([journal](http://aif.cedram.org/item?id=AIF_1998__48_2_425_0))


[[!redirects Lie-Rinehart algebra]]
[[!redirects Lie?Rinehart pair]]
[[!redirects Lie?Rinehart algebra]]
[[!redirects Lie--Rinehart pair]]
[[!redirects Lie--Rinehart algebra]]

[[!redirects homotopy Lie-Rinehart pair]]
[[!redirects homotopy Lie-Rinehart pairs]]

