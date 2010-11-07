[[!redirects Pi-algebras]]
[[!redirects Pi-algebras]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}
 
##Idea

A _$\Pi$-algebra_ is an algebraic model for the [[homotopy group]]s $\pi_*X$ of a pointed [[topological space]], $X$, together with the [[action]] of the [[primary homotopy operation]]s on them, in the same sense that algebras over the [[Steenrod algebra]] are models for the [[cohomology]] of a space.


## The category $\Pi$ of homotopy operations

The [[category]] $\Pi$ of homotopy operations has

* as [[object]]s - pointed [[CW-complex]]es with the [[homotopy type]] of a finite [[wedge product]] of [[sphere]]s of [[dimension]]s $\geq 1$;


* as [[morphism]]s - homotopy classes of (pointed) [[continuous function]]s between them.

### Properties

*  $\Pi$ is a pointed category and has finite coproducts (given by the finite wedges), but not products.

 *  There is a [[functor]], _smash product_ $i : \Pi\times \Pi \to \Pi$, which sends an object $(U,V)$ to $U\wedge V = (U\times V)/((U\times *)\vee(*\times V))$, which preserves [[coproduct]]s in each variable.


##$\Pi$-algebras

Let $Set_*$ denote the category of [[pointed sets]].

+--
{: . un_defn}
######Definition

A _$\Pi$-algebra_ is a [[functor]] $A: \Pi^{op}\to Set_*$, which sends [[coproduct]]s to [[products]].

A morphism of $\Pi$-algebras is a natural transformation between the corresponding functors.

=--

### Properties

* A $\Pi$-algebra $A$ satisfies $A* = *$.

* The values of a $\Pi$-algebra $A$ are determined by the values $A_n = A(S^n)$, that it takes on the spheres, $S^n$, $n\geq 1$.

*  A $\Pi$-algebra can be considered to be a graded [[group]] $\{A_n\}_{n=1}^\infty$ with $A_n$ abelian for $n\gt 1$, together with  
   
   * [[Whitehead product]] homomorphisms : 

$$[-,-] : A_p\otimes A_q \to A_{p+q-1}$$

for $p,q \geq 1$ (the case where they are equal to 1 needs special mention, see below.)
     
   * [[composition operation]]s, $-\cdot \alpha : A_p\to A_r$ for $\alpha \in \pi_r(S^p)$, $1\lt p\lt r$,

which satisfy the identities that hold for the Whitehead products and composition operations on the higher homotopy groups os a pointed space, and

   * a left action of $A_1$ on the $A_n$, $n\gt 1$, which commutes with these operations.

The [[Whitehead products]] include

   * $[\xi,a] = {}^\xi a - a$, where ${}^\xi a$ is the result of the $A_1$-action of $\xi \in A_1$ on $a\in A_r$, $r\gt 1$; similarly for a right action;

   * the commutators $[a,b] = aba^{-1]b^{-1}$, for $a,b \in A_1$.

## The homotopy $\Pi$-algebra of a pointed topological space.

For a pointed space $X$, and $U \in \Pi$, define $\pi_* X = [U,X]_*$, the set of pointed homotopy classes of pointed maps from $U$ to $X$.

This is a $\Pi$-algebra called the **homotopy $\Pi$-algebra** of $X$.


##The realisability problem

Suppose $A: \Pi \to sets_*$ is an abstract $\Pi$-algebra, the **realisability problem** for $A$ is to construct, if possible, a pointed space $X$, such that $A\simeq \pi_* X$.  The space $X$ is called a _realisation_ of $A$.

Things can be complicated!

1.  The homotopy type of $X$ is not be determined by $A$ (hence 'a' rather than 'the" realisation) , so that raises the additional problem of classifying the realisations.

1. Not all $\Pi$-algebras can be reaised, in fact

####Theorem (Blanc 1995)

Given a $\Pi$-algebra, $A$, there is a sequence of [[higher homotopy operation]]s depending only on maps between wedges of spheres, such that $A$ is realisable if and only if the operations vanish coherently.

####Example (Blanc 1995)

For $p\neq 2$, a prime and $r\geq 4(p-1)$, $\pi_*S^r \otimes \mathbb{Z}/p$ cannot be realised (and if $p = 2$, one uses $r\geq 6).

(There is a problem, discussed in Blanc's 1995 paper, that the composition operations need not be 
homomorphisms, so tensoring with $\mathbb{Z}/p$ has to be interpreted carefully.)




## References

* C.R. Stover, _A Van Kampen spectral sequence for higher homotopy groups_, Topology 29 (1990) 9 - 26.

[[David Blanc]] has written a lot on these objects. An example is

* [[David Blanc]], _Loop spaces and homotopy operations_, Fund. Math. 154 (1974) 75 - 95.

The realisability problem is discussed in 

* [[David Blanc]], _Higher homotopy operations and the realizability of homotopy groups_, Proc.  London Math. Soc. (3) 70 (19950 214 -240,

and further in 

*  [[David Blanc]], _Algebraic invariants for homotopy types_, Math. Proc. Camb. Phil. Soc. 127 (3)(1999) 497 - 523. (preprint version on the [ArXiv](http://arxiv.org/abs/math/9812035).)

There are more recent results on the realisability problem in Martin Frankland's [thesis](http://www.math.uiuc.edu/~franklan/Frankland_Thesis_20100513.pdf).  