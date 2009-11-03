# Contents #
* automatic table of contents goes here
{:toc}


#Idea#

A Lie--Rinehart pair is an algebraic structure that generalizes the notion of [[Lie algebroid]] from the case where the base is a [[manifold]] to that where it is an arbitrary [[noncommutative geometry|noncommutative space]].


#Definition#

A _Lie--Rinehart-pair_ $(A,\mathfrak{g})$ is a pair consisting of an associative [[algebra]] $A$ and a [[Lie algebra]] $\mathfrak{g}$ such that $A$ is a $\mathfrak{g}$-module and $\mathfrak{g}$ is an $A$-module with both module structures being compatible in the obvious way:

* $\mathfrak{g}$ acts as derivations of $A$: that is, we have a Lie algebra homomorphism $\mathfrak{g} \to Der(A)$. 

* $A$ acts as linear transformations of $\mathfrak{g}$ in a way obeying the Leibniz law: that is, we have an associative algebra homomorphism from $A$ to the algebra of linear transformations of $\mathfrak{g}$ such that
$$  [v, a w] = v(a) w + a [v,w]. $$ 


#Examples#

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

* $\mathfrak{g} = \Gamma(E)$ is the [[Lie algebra]] of [[section]]s of $E$ using the above bracket

* the action of $A$ on $\mathfrak{g}$ is the obvious multiplication of sections of vector bundles over $X$ by functions on $X$

* the action of $\mathfrak{g}$ on $C^\infty(X)$ is given by first applying the anchor map $\rho$ and then using the canonical action of vector fields on functions.

So for all the examples listed at [[Lie algebroid]] we obtain an example for Lie--Rinehart pairs.

In particular

* the Lie--Rinehart pair coresponding to the [[tangent Lie algebroid]] of a [[manifold]] $X$ is $(C^\infty(X), \Gamma(T X))$ with the obvious action on each other.

* the Lie--Rinehart pair corresponding to an ordinary [[Lie algebra]] $\mathfrak{g}$ is $(\mathbb{R}, \mathfrak{g})$ with $\mathfrak{g}$ acting trivially on $\mathbb{R}$.

* the Lie--Rinehart pair corresponding to a [[Poisson Lie algebroid]] on a [[Poisson manifold]] $X$ is $(C^\infty(X), MultVect(X))$, where the [[Lie algebra]] is the the space of multi vector fields on $X$ equipped with the bracket ... (exercise for the reader) ...


# Generalizations #

A little bit is known in the literature to generalizations of the notion of Lie--Rinehart algebras that are to [[Lie ∞-algebroids]] as the latter are to [[Lie algebroids]].

In 

* [[Dmitry Roytenberg]], _Courant--Dorfman algebras and their cohomology_ ([arXiv](http://arxiv.org/abs/0902.4862))

the analogous algebraic structure for [[Courant algebroid]]s is discussed. These "2-Lie--Rinehart algebras" are ccalled [[Courant?Dorfman algebra]]s there.


#References#

The original reference is

* G. Rinehart _Differential forms for general commutative algebras_ Trans. Amer. Math. Soc. 108 (1963), 195-222

A brief review in section 1 of

* [[Johannes Huebschmann]], _Lie--Rinehart algebras, descent, and quantization_ ([arXiv](http://arxiv.org/abs/math/0303016))

A notion of universal enveloping algebra of a Lie--Rinehart algebra is discussed in

* [[Ieke Moerdijk]], J. Mrcun, _On the universal enveloping algebra of a Lie--Rinehart algebra_ ([arXiv](http://arxiv.org/abs/0801.3929))

A connection with [[BV-theory]] is made in

* [[Johannes Huebschmann]], _Lie--Rinehart algebras, Gerstenhaber algebras and Batalin-Vilkovisky algebras_ ([journal](http://aif.cedram.org/item?id=AIF_1998__48_2_425_0))


[[!redirects Lie-Rinehart algebra]]
[[!redirects Lie?Rinehart pair]]
[[!redirects Lie?Rinehart algebra]]
[[!redirects Lie--Rinehart pair]]
[[!redirects Lie--Rinehart algebra]]