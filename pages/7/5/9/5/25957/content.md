#Contents#
* table of contents
{:toc}

## Idea

Prismatization is a stacky approach to [[prismatic cohomology]] developed independently by Drinfeld in [#Drinfeld20] (#Drinfeld20) and Bhatt-Lurie in [#BhattLurie22](#BhattLurie22) and [#BhattLurie22b](#BhattLurie22b).

## Motivation: Linear algebra via stacks

The reference for this section is Section 2 of [#BhattNotes](#BhattNotes).

## Definitions

\begin{definition}(Definition 3.1.4 of [#BhattLurie22a](#BhattLurie22a), Definition 5.13 of [#BhattNotes](#BhattNotes))
Let $R$ be a p-nilpotent ring and $W(R)$ its ring of Witt vectors. A _Cartier-Witt divisor_ on $R$ is an invertible $W(R)$-module $I$ together with a morphism $\alpha:I\to W(R)$ of $W(R)$-modules such that

* The image of the map $I\to W(R)\twoheadrightarrow R$ is a nilpotent ideal of $R$.
* The image of the map $I\to W(R)\xrightarrow{\delta} W(R)$ generates the unit ideal of $W(R)$.

\end{definition}

\begin{definition}(Definition 5.1.6 of [#BhattNotes](#BhattNotes))
Let $X$ be a bounded $p$-adic formal scheme. The _prismatization_ $X^{\Delta}$ is the presheaf over $\mathrm{Spf}(\mathbb{Z}_{p})$ defined as follows. For a $p$-nilpotent ring $R$, $X^{\Delta}(R)$ is the groupoid of Cartier-Witt divisors on $R$ together with a map $\mathrm{Spec}(\mathrm{Cone}(W(R)/I))\to X$ of derived $\mathrm{Spf}(\mathbb{Z}_{p})$-schemes.
\end{definition}


## The Cartier-Witt stack

The prismatization $\mathrm{Spf}(\mathbb{Z}_{p})^{\Delta}$ of $\mathrm{Spf}(\mathbb{Z}_{p})$ is also called the _Cartier-Witt stack_, and denoted $\mathrm{WCart}$ or $\mathbb{Z}_{p}^{\Delta}$.


## Filtered prismatization

The reference for this section is Section 5.3 of [#BhattNotes](#BhattNotes).

\begin{definition}(Definition 5.2.4 of [#BhattNotes](#BhattNotes))
Let $R$ be a $p$-nilpotent ring. Let $W$ be the ring scheme of Witt vectors over $\mathrm{Spf}(\mathbb{Z}_{p})$. Let $F:W\to F_{*}W$ be the Frobenius. An _admissible $W$-module_ over $R$ is an affine $W$-module scheme $M$ which can be realized as an extension of a twisted form of $F_{*}M$ by a twisted form of the $\mathbb{G}_{a}^{#}$, where $\mathbb{G}_{a}^{#}$ is the PD-hull of the origin in $\mathbb{G}_{a}$ over $\mathbb{Z}$.
\end{definition}

\begin{definition} (Definition 5.3.1 of [#BhattNotes](#BhattNotes)) 
Let $R$ be a $p$-nilpotent ring. Let $W$ be the ring scheme of Witt vectors over $\mathrm{Spf}(\mathbb{Z}_{p})$. Let $F:W\to F_{*}W$ be the Frobenius. A _filtered Cartier-Witt divisor over $R$ is an admissible $W$-module $M$ over $R$ and a map $M\to W$ such that the induced map $F_{\ast}M'\to F_{\ast}W$ of twisted forms of $F_{\ast}W $ comes from a Cartier-Witt divisor.

\end{definition}

\begin{definition} (Definition 5.3.10 of [#BhattNotes](#BhattNotes))

Let $X$ be a bounded $p$-adic formal scheme. Define $\mathrm{Spf}(\mathbb{Z}_{p})^{\mathcal{N}}$ to be the stack which takes a $p$-nilpotent ring $R$ to the groupoid $\mathrm{Spf}(\mathbb{Z}_{p})^{\mathcal{N}}(R)$ of filtered Cartier-Witt divisors over $R$. The _filtered prismatization_ of $X$ is the stack $X^{\mathcal{N}}$ over $\mathbb{Z}_{p}^{\mathcal{N}}$ obtained via transmutation from $\mathbb{G}_{a}^{\mathcal{N}}\to\mathbb{Z}_{p}^{\mathcal{N}}$, where $\mathbb{G}_{a}^{\mathcal{N}}$ is the stack over $\mathbb{Z}_{p}^{\mathcal{N}}$ taking a filtered Cartier-Witt divisor $d:M\to W$ to $R\Gamma(\mathrm{Spec}(R),W/M)$.

\end{definition}

## References

* {#Drinfeld20}[[Vladimir Drinfeld]], _Prismatization_ (2020) arXiv:[2005.04746] (https://arxiv.org/abs/2005.04746)

* {#BhattLurie22a}[[Bhargav Bhatt]], [[Jacob Lurie]], _Absolute Prismatic Cohomology_, preprint (2022) arXiv:[2022.06120](https://arxiv.org/abs/2201.06120)

* {#BhattLurie22b}[[Bhargav Bhatt]], [[Jacob Lurie]], _The Prismatization of $p$-adic Formal Schemes_, preprint (2022) arXiv:[2022.06124](https://arxiv.org/abs/2201.06124)

* {#BhattNotes} [[Bhargav Bhatt]], _Prismatic F-gauges_, ([Lecture notes](https://www.math.ias.edu/~bhatt/teaching/mat549f22/lectures.pdf))
