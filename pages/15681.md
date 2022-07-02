
#Contents#
* table of contents
{:toc}

## Idea

The _Birch and Swinnerton-Dyer conjecture_ is a [[conjecture]] about the form of the first non-vanishing [[derivative]] of the [[Hasse-Weil L-function]] of an [[elliptic curve]] at $s= 1$, expressed in terms of a [[higher regulator]], analogous to the [[class number formula]] for a [[Dedekind zeta function]].

This is hence a conjecture about [[special values of L-functions]]. It influenced the more far-reaching [[Beilinson conjectures]].

## Statement

Let $E$ be an elliptic curve over $\mathbb{Q}$. The Mordell-Weil theorem states that the Mordell-Weil group $E(\mathbb{Q})$ (defined to be the group of rational points of $E$) is a finitely generated abelian group, i.e. it is isomorphic to the product of $r$ copies of $\mathbb{Z}$ with some torsion subgroup. This $r$ is called the algebraic rank.

The rank part of the Birch and Swinnerton-Dyer conjecture states that the algebraic rank $r$ is given by the order of vanishing of the [[Hasse-Weil L-function]] $L(E,s)$ of $E$ at $s=1$. For instance, if $L(E,s)$ does not vanish at $s=1$, then the conjecture states that $E$ has no rational points of infinite order. 

Note that more generally it is not known if the Hasse-Weil L-function of an elliptic curve (over a more general field) is even defined at $s=1$. However the [[modularity theorem]] states that every elliptic curve over $\mathbb{Q}$ is modular, so this Hasse-Weil L-function is equal to the L-function of some [[modular form]], which is known to have analytic continuation to all of $\mathbb{C}$, by the work of [[Erich Hecke]].

There is an even stronger statement of the Birch and Swinnerton-Dyer conjecture that gives the first non-vanishing Taylor coefficient of the Hasse-Weil L-function of $E$:

$$\frac{L^{(r)}(E,1)}{r!}=\frac{\#Sha(E) \Omega_{E} R_{E}\prod_{p\vert N}c_{p}}{(#E(\mathbb{Q})_{Tor})^{2}}.$$

Here

* $\#Sha(E)$ is the order of the [[Tate-Shafarevich group]] of $E$

* $\Omega_{E}$ is the real period of $E$

* $R_{E}$ is the regulator of $E$

* $c_{p}$ is the Tamagawa number of $E$ at a prime $p$ dividing the conductor $N$ of $E$

* $\#E(\mathbb{Q})_{Tor}$ is the order of the torsion subgroup of the Mordell-Weil group $E(\mathbb{Q})$ of $E$.

## Progress

## Related concepts

* [[Picard group]], [[Tate-Shafarevich group]]

* [[Tamagawa number]]

## References

* Wikipedia, _[Birch and Swinnerton-Dyer conjecture](http://en.wikipedia.org/wiki/Birch_and_Swinnerton-Dyer_conjecture)_

* Frank Gounelas, _The BSD cconjecture, regulators and special values of L-functions_ ([[GounelasBSD.pdf:file]])

* {#Bloch80} [[Spencer Bloch]], _A note on height pairings, Tamagwawa numbers, and the Birch and Swinnerton-Dyer conjecture_, Inventiones math. 58, 65-76 (1980) ([[BlochTamagawa.pdf:file]])

* Conrad, Venkatesh, et al., _BSD Seminar_ _[Introduction to the BSD conjecture](http://math.stanford.edu/~conrad/BSDseminar/Notes/L1.pdf)_, _[All lecture notes](http://math.stanford.edu/~conrad/BSDseminar/Notes/)_
[[!redirects BSD conjecture]]
[[!redirects BSD-conjecture]]
