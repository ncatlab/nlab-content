
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

Recall that a [[Henselian ring]] is a [[local ring]] $R$ with [[maximal ideal]] $\mathfrak{m}$ satisfying the conclusion of [[Hensel's lemma]]. A **Henselian pair** is a generalisation of this concept to the case where the ring doesn't have to be a local ring, and the maximal ideal is replaced by a more general ideal $I$.

## Definition

A *pair* consists of a ring $R$ and an [[ideal]] $I\subset R$.

+-- {: .num_defn}
###### Definition 

A **henselian pair** is a pair $(R, I)$ satisfying

1. $I$ is contained in the [[Jacobson radical]] of $R$, and
1. for any [[monic polynomial]] $f \in R[T]$ and factorization
$\overline{f} = g_0h_0$ with $g_0, h_0 \in R/I[T]$ monic
generating the unit ideal in $R/I[T]$, there
exists a factorization $f = gh$ in $R[T]$ with $g, h$ monic
and $g_0 = \overline{g}$ and $h_0 = \overline{h}$.

There are several equivalent characterizations, see 
[the Stacks Project](#Stacks-henselian-pair). Another characterization is the following (see [Gabber](#Gabber)):

+-- {: .num_prop}
###### Proposition 

A pair $(R,I)$ is a henselian pair if and only if

1. $I$ is contained in the [[Jacobson radical]] of $R$, and
1. Let $f(t) = (t-1)t^N + g(t)$ where $g(t) \in IR[t]$ has degree $\leq N-1$, with $N \geq 1$. Then $f(t)$ has a (necessarily unique) root in $I+1$.
=--

This characterization shows that the property of $(R,I)$ being a henselian pair essentially depends only on the ideal $I$, regarded as a non-unital ring, and not on $R$. Thus the property of $I$ being henselian may be axiomatized in terms of an additional set of algbraic operations on $I$, sending $(g_0,\dots, g_{N-1})$ to the root of $(t-1)t^N + g_{N-1}t^{N-1} + \dots + g_0$, and the resulting algebraic category is equivalent to a full subcategory of the category of nonunital rings.

=--

## Properties

The category of pairs has as morphisms $(R,I) \to (S,J)$ those ring maps $\phi\colon R\to S$ such that $\phi(I) \subset J$. The category of Henselian pairs is the obvious full subcategory.

+-- {: .num_prop}
###### Proposition 

The inclusion map $HenselianPairs \to Pairs$ has a left adjoint
=--

For a proof, see ([Tag 0A02](https://stacks.math.columbia.edu/tag/0A02)) in the Stacks Project. This Henselization functor restricts to the usual one on the subcategory of local rings and local homomorphisms.



## References

* {Stacks-henselian-pair} Stacks Project [Tag 09XD](https://stacks.math.columbia.edu/tag/09XD)
* Eberhard Scherzler, _On henselian pairs_,  Communications in Algebra
Volume 3 (1975) pp 391-404,  doi:[10.1080/00927877508822052](https://doi.org/10.1080/00927877508822052)
* Michel Raynaud, _Anneaux locaux hens&#233;liens_, Lecture Notes in Mathematics Volume **169** 1970 doi:[10.1007/BFb0069571](https://dx.doi.org/10.1007/BFb0069571)
* {Gabber} Gabber, Ofer, _$K$-Theory of Henselian Local Rings and Henselian Pairs_, Algebraic $K$-Theory, Commutative Algebra, and Algebraic Geometry (Santa Margherita Ligure, 1989), 126:59–70. Contemp. Math. Amer. Math. Soc., Providence, RI, 1992. [mathscinet](https://mathscinet.ams.org/mathscinet-getitem?mr=1156502)

