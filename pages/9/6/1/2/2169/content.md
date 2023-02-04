
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Normed division algebras
* table of contents
{: toc}

## Idea

A normed division algebra is a [[not-necessarily associative algebra]] over the real numbers that is: 

1. [[unital]] (there is an element $1$ such that $1a = a = a1$ for all $a$),

1. a [[division algebra]] $\big( \text{i.e.}\, (a \cdot b = 0) \Rightarrow (a = 0 \,\text{or}\, b = 0) \big)$, and  

1. a [[normed algebra]] such that $\|a b\| = \|a\| \|b\|$ for all $a,b$.

It turns out (by [[Hurwitz' theorem]]) that over the [[real numbers]] there are precisely only four finite-dimensional normed division algebras up to [[isomorphism]]: the algebras of 

1. [[real numbers]], 

1. [[complex numbers]], 

1. [[quaternions]], 

1. [[octonions]].

In this sense real normed division algebras may be thought of as a natural generalization of the [[real numbers]] and the [[complex numbers]]. 

Moreover, if one regards the [[real numbers]] as a [[star-algebra]] with trivial [[anti-involution]], then each step in the above sequence is given by applying the [[Cayley-Dickson construction]]. (While the process of applying the [[Cayley-Dickson construction]] continues, next with the[[sedenions]], these and the following are no longer [[division algebras]].)

This classification of real normed division algebras is closely related to various other systems of [[universal exceptionalism|exceptional]] structures in [[mathematics]] and [[physics]]: 

* The _[[Hopf invariant one theorem]]_ says that the only [[continuous functions]] between [[spheres]] of the form $S^{2n-1}\to S^n$ whose [[Hopf invariant]] is equal to 1 are the [[Hopf constructions]] on the four real normed division algebras, namely 

   1. the [[real Hopf fibration]];

   1. the [[complex Hopf fibration]];

   1. the [[quaternionic Hopf fibration]];

   1. the [[octonionic Hopf fibration]].

* Patterns related to [[Majorana spinors]] in [[spin geometry]] are intimately related to the four normed division algebras, and, induced by this, so is the classification of _[[supersymmetry]]_ in the form of [[super Poincaré Lie algebras]] and [[super Minkowski spacetimes]] (which are built from these real spin representations). For more on this see at _[[supersymmetry and division algebras]]_.

(Moreover, apparently these two items are not unrelated, see [[schreiber:Equivariant cohomology of M2/M5-branes|here]].)


## Definition

A __normed division algebra__ is 

* a [[division algebra]]

* that is also a [[Banach algebra]]

* such that ${\|x y\|} = {\|x\|} {\|y\|}$

While the [[norm]] in a [[Banach algebra]] is in general only submultiplicative (${\|x y\|} \leq {\|x\|} {\|y\|}$), the norm in a normed division algebra must obey the stronger condition ${\|x y\|} = {\|x\|} {\|y\|}$.  Accordingly, this norm is considered to be an [[absolute value]] 
and often written ${|{-}|}$ instead of ${\|{-}\|}$.  There is also a converse: if the norm on a Banach algebra is multiplicative (including ${\|1\|} = 1$), then it must be a division algebra.  While the usual definition of a 'normed division algebra' does not include the [[complete space|completeness]] condition of a Banach algebra, in fact 
([UrbanikWright60](#UrbanikWright60)) the only examples have finite [[dimension]] and are therefore complete, hence Banach algebras.

Any normed division algebras is in particular a [[composition algebra]].

## Properties

### Classification
 {#Classification}

Over the [[complex numbers]],  [[generalized the|the]] only normed division algebra is the algebra of complex numbers themselves.  

The [[Hurwitz theorem]] says that over the [[real numbers]] there are, up to [[isomorphism]], exactly four finite-dimensonal normed division algebras :

*  $\mathbb{R}$, the algebra of [[real numbers]],
*  $\mathbb{C}$, the algebra of [[complex numbers]],
*  $\mathbb{H}$, the algebra of [[quaternions]],
*  $\mathbb{O}$, the algebra of [[octonions]].

In fact these are also exactly the real [[alternative algebra|alternative]] division algebras:

+-- {: .num_prop #ZornTheorem}
###### Proposition

The only [[division algebras]] over the [[real numbers]] which are also [[alternative algebras]] are the [[real numbers]] themselves, the [[complex numbers]], the [[quaternions]] and the [[octonions]].

=--

([Zorn 30](#Zorn30)).

Each of these is produced from the previous one by the [[Cayley–Dickson construction]]; when applied to $\mathbb{O}$, this construction produces the algebra of [[sedenions]], which do *not* form a division algebra.

The Cayley--Dickson construction applies to an algebra with [[involution]]; by the abstract nonsense of that construction, we can see that the four normed division algebras above have these properties:

*  $\mathbb{R}$ is [[associative algebra|associative]], [[commutative algebra|commutative]], and with trivial involution,
*  $\mathbb{C}$ is associative and commutative but has nontrivial involution,
*  $\mathbb{H}$ is associative but noncommutative and with nontrivial involution,
*  $\mathbb{O}$ is neither associative, commutative, nor with trivial involution.

However, these algebras do all have some useful algebraic properties; in particular, they are all [[alternative algebra|alternative]] (a weak version of associativity).  They are also all [[composition algebra]]s.

A __[[normed field]]__ is a commutative normed division algebra; it follows from the preceding that the only normed fields over $\mathbb{R}$ are $\mathbb{R}$ and $\mathbb{C}$ (e.g. [Tornheim 52](#Tornheim52)).

It is in fact true that all _unital_ normed division algebras over $\mathbb{R}$ are already finite dimensional, by ([Urbanik-Wright 1960](#UrbanikWright60)) (the authors give a reference on a non-unital infinite-dimensional normed division algebra). Hence the [[Hurwitz theorem]] together with [Urbanik-Wright 1960](#UrbanikWright60) says that the above four exhaust all real normed division algebras.

### Automorphisms
 {#Automorphisms}

The [[automorphism groups]] of the real normed division algebras, as [[normed algebras]], are

* $Aut(\mathbb{R}) = 1$, the [[trivial group]]

* $Aut(\mathbb{C}) = \mathbb{Z}/2$ the [[group of order 2]], acting by [[complex conjugation]];

* $Aut(\mathbb{H}) = SO(3)$, the [[special orthogonal group]] acting via its canonical representation  on the 3-dimensional space of imaginary quaternions;

* $Aut(\mathbb{O}) = G_2$, the [[exceptional Lie group]] [[G2]].

Incidentally, there is a sense in which this sequence of groups continues, with the [[infinity-group]] [[G3]] (the [[Dwyer-Wilkerson H-space]]):

| $n=$ | 0 | 1 | 2 | 3 | 4 | 
|--|--|--|--|--|--|
| $DI(n)=$ | [[trivial group|1]] |  [[Z/2]] | [[SO(3)]] | [[G2]] | [[G3]] |
|          | = Aut(R) | [= Aut(C)](complex+number#AutomorphismsOfComplexNumbersIsZ2)        | [= Aut(H)](quaternion#AutomorphismsOfQUatrnionsAlgebraIsSO3)       |  [= Aut(O)](octonion#AutomorphismsOfOctonionAlgebraIsG2)  |  


### Relation to H-space structures on sphere (Hopf invariant one)

The [[Hopf invariant one theorem]] says that the [[spheres]] carrying [[H-space]] structure are precisely the unit spheres in one of the normed division algebras

<img src="http://ncatlab.org/nlab/files/AdamsHopfInvariantProofFlow.jpg" width="700">

([Adams 60](Hopf+invariant+one#Adams60))

### Magic square 

The [[Freudenthal magic square]] is a special square array of [[Lie algebras]]/[[Lie groups]] labeled by pairs of real normed division algebras and including all the [[exceptional Lie groups]] except [[G2]].
 
## Related concepts

* [[Hopf invariant one]]

* [[Cayley–Dickson construction]]

[[!include exceptional spinors and division algebras -- table]]

see [[division algebra and supersymmetry]]

[[!include normed division algebra Riemannian geometry -- table]]

## References


The classification of real divsion composition algebras is originally due ([[Hurwitz theorem]]) to 

* {#Hurwitz1898} [[Adolf Hurwitz]], _&#220;ber die Composition der quadratischen Formen von beliebig vielen Variabeln_, Nachr. Ges. Wiss. G&#246;ttingen (1898) 309&#8211;316

The alternative classification as real [[alternative algebra|alternative]] division algebras is due to

* {#Zorn30} [[Max Zorn]], _Theorie der alternativen Ringe_, Abhandlungen des Mathematischen Seminars der Universit&#228;t Hamburg 8 (1930), 123-147

General discussion includes includes

* {#Tornheim52} Leonard Tornheim, _Normed fields over the real and complex fields_, Michigan Math. J. Volume 1, Issue 1 (1952), 61-68. ([Euclid](http://projecteuclid.org/euclid.mmj/1028989727))

* Silvio Aurora, _On normed rings with monotone multiplication_, Pacific J. Math.
Volume 33, Number 1 (1970), 15-20 ([JSTOR](http://projecteuclid.org/euclid.pjm/1102977236))

The result about removing the assumption of finite-dimensionality from unital normed division algebras appears in:

* {#UrbanikWright60} Kazimierz Urbanik and Fred B. Wright, _Absolute-valued algebras_, Proc. Amer. Math. Soc. **11** (1960), 861-866, doi:[10.1090/S0002-9939-1960-0120264-6](https://doi.org/10.1090/S0002-9939-1960-0120264-6)


Exposition with emphasis on the [[octonions]] is in

* [[John Baez]], _[Normed Division Algebras](http://math.ucr.edu/home/baez/octonions/node2.html)_

* [[John Baez]], [This Week's Finds --- Week 59](http://math.ucr.edu/home/baez/week59.html)

Discussion of [[Riemannian geometry]] and [[special holonomy]] modeled on the different normed division algebras is in

* {#Leung02} [[Naichung Conan Leung]], _Riemannian Geometry Over Different Normed Division Algebras_, J. Differential Geom. Volume 61, Number 2 (2002), 289-333. ([euclid](http://projecteuclid.org/euclid.jdg/1090351387))



[[!redirects normed division algebra]]
[[!redirects normed division algebras]]

[[!redirects real normed division algebra]]
[[!redirects real normed division algebras]]

