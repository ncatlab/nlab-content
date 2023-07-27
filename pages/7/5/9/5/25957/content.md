#Contents#
* table of contents
{:toc}

## Idea

Prismatization is a stacky approach to [[prismatic cohomology]] developed independently by Drinfeld in [#Drinfeld20] (#Drinfeld20) and Bhatt-Lurie in [#BhattLurie22](#BhattLurie22) and [#BhattLurie22b](#BhattLurie22b).

## Motivation: Linear algebra via stacks

The reference for this section is Section 2 of [#Bhatt22](#Bhatt22).

## Definitions

\begin{definition}(Definition 3.1.4 of [#BhattLurie22a](#BhattLurie22a), Definition 5.13 of [#Bhatt22](#Bhatt22))
Let $R$ be a p-nilpotent ring and $W(R)$ its ring of Witt vectors. A _Cartier-Witt divisor_ on $R$ is an invertible $W(R)$-module $I$ together with a morphism $\alpha:I\to W(R)$ of $W(R)$-modules such that

* The image of the map $I\to W(R)\twoheadrightarrow R$ is a nilpotent ideal of $R$.
* The image of the map $I\to W(R)\xrightarrow{\delta} W(R)$ generates the unit ideal of $W(R)$.

\end{definition}

\begin{definition}(Definition 5.1.6 of [#Bhatt22](#Bhatt22))
Let $X$ be a bounded $p$-adic formal scheme. The _prismatization_ $X^{\Delta}$ is the presheaf over $\mathrm{Spf}(\mathbb{Z}_{p})$ defined as follows. For a $p$-nilpotent ring $R$, $X^{\Delta}(R)$ is the groupoid of Cartier-Witt divisors on $R$ together with a map $\mathrm{Spec}(\mathrm{Cone}(W(R)/I))\to X$ of derived $\mathrm{Spf}(\mathbb{Z}_{p})$-schemes.
\end{definition}

## Filtered prismatization

The reference for this section is Section 5.3 of [#Bhatt22](#Bhatt22).

## References

* {#Drinfeld20}[[Vladimir Drinfeld]], _Prismatization_ (2020) arXiv:[2005.04746] (https://arxiv.org/abs/2005.04746)

* {#BhattLurie22a}[[Bhargav Bhatt]], [[Jacob Lurie]], _Absolute Prismatic Cohomology_, preprint (2022) arXiv:[2022.06120](https://arxiv.org/abs/2201.06120)

* {#BhattLurie22b}[[Bhargav Bhatt]], [[Jacob Lurie]], _The Prismatization of $p$-adic Formal Schemes_, preprint (2022) arXiv:[2022.06124](https://arxiv.org/abs/2201.06124)

* {#Bhatt22} [[Bhargav Bhatt]], _Prismatic F-gauges_, ([Lecture notes](https://www.math.ias.edu/~bhatt/teaching/mat549f22/lectures.pdf))
