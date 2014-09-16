
#Contents#
* table of contents
{:toc}

## Idea

The _absolute Galois group_ of a [[field]] $k$ is that of the [[field extension]] $k \hookrightarrow k_s$ which is the [[separable closure]] of $k$. When $k$ is a [[perfect field]] this is equivalently the Galois group of the [[algebraic closure]] $k \hookrightarrow \overline{k}$.

## Definition

+-- {: .num_defn}
###### Definition

Let $k$ be a [[field]]. Let $k_s$ denote the [[separable closure]] of $k$. Then the [[Galois group]] $Gal(k\hookrightarrow k_s)$ of the [[field extension]] $k\hookrightarrow k_s$ is called *absolute Galois group of $k$*.

=--

## Properties

+-- {: .num_remark}
###### Remark

By general [[Galois theory]]
we have $Gal(K\hookrightarrow K_s)\simeq \pi_1(Spec\; K)$ is equivalent to the [[fundamental group]] of the [[spectrum of a commutative ring|spectrum]] [[scheme]] $Spec K$ 

=--


An instance of [[Grothendieck's Galois theory]] is the following:

+-- {: .num_prop}
###### Proposition
The functor

$$\begin{cases}
Sch_{et}\to Gal(k\hookrightarrow k_s)-Set
\\
X\mapsto X(k_s)
\end{cases}$$

from the category of [[étale scheme|étale schemes]] to the category of sets equipped with an [[action]] of the absolute Galois group is an equivalence of categories.
=--

+-- {: .num_prop}
###### Proposition
Recall the every [[profinite group]] appears as the [[Galois group]] of some [[Galois extension]]. Moreover we have:

Every [[projective object|projective]] [[profinite group]] appears as an absolute [[Galois group]] of a [[pseudo algebraically closed field]].
=--

## Examples

### Of the rational numbers

+-- {: .num_remark}
###### Remark
There is no direct description (for example in terms of [[generators and relations]]) known for the absolute Galois group $G_\mathbb{Q}:=Gal(\mathbb{Q}\hookrightarrow \overline \mathbb{Q})$ of the [[rational numbers]].

However [[Belyi's theorem]] implies that there is a faithful [[action]] of $G_\mathbb{Q}$ on the [[children's drawing|children's drawings]].
=--

+-- {: .num_theorem}
###### Theorem 
**(Drinfeld, Ihara, Deligne)**

There is an inclusion of the absolute Galois group of the rational numbers into the [[Grothendieck-Teichmüller group]] (recalled e.g. as [Stix 04, theorem 6](#Stix04)).

=--

## References

* {#Stix04} [[Jakob Stix]], _The Grothendieck-Teichm&#252;ller group and Galois theory of the rational numbers_, 2004 ([[StiXGaloisAndGT.pdf:file]])

category: Galois theory

[[!redirects absolute Galois groups]]

[[!redirects absolute Galois theory]]


