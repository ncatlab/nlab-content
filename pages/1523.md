
# Extended natural numbers
* table of contents
{: toc}

## Idea

The __extended natural number system__, denoted $\bar{\mathbb{N}}$, consists of all of the [[natural numbers]] together with an extra number representing [[infinity]].


## Definition

Classically, $\bar{\mathbb{N}}$ is the [[disjoint union]] of the set $\mathbb{N}$ of natural numbers and a [[point]] $\{\infty\}$.  That is,
$$ \bar{\mathbb{N}} = \{0,1,2,\ldots,\infty\} .$$

In [[constructive mathematics]], a more careful definition is required: an __extended natural number__ is an [[infinite sequence]] $x$ of [[binary digits]] (each $0$ or $1$) with the property that $x_i = 1$ if $x_j = 1$ for any $j \leq i$; that is, the sequence is [[monotone function|monotone]].  Then the natural number $n$ is identified with a sequence of $n$ copies of $0$ followed by $1$s, while infinity is identified with a sequence of all $0$s.  It is *not* constructively valid that every natural number is either finite or infinite, but it is valid that any that is not finite is infinite, while [[Markov's principle]] is the converse.


## Universal property

$\bar{\mathbb{N}}$ comes naturally equipped with a map $pred\colon \bar{\mathbb{N}} \to 1 + \bar{\mathbb{N}}$ as defined below:
$$
pred(x) = \begin{cases}
*      & if\; x = 0 ,\\
n      & if\; x = n + 1 ,\\
\infty & if\; x = \infty .\end{cases}
$$

Thus, it is a [[coalgebra]] for the endofunctor $H(X) = 1 + X$ on [[Set]], and indeed is the [[terminal coalgebra]] for $H$.  That is, given any set $S$ and map $p\colon S \to 1 + S$, there is a unique map $corec_S p\colon S \to \bar{\mathbb{N}}$ such that
$$ \array {
S                      & \stackrel{p}\to    & 1 + S \\
\downarrow_{corec_S p} &                    & \downarrow_{\id_1 + corec_S p} \\
\bar{\mathbb{N}}       & \stackrel{pred}\to & 1 + \bar{\mathbb{N}}
} $$
commutes.  Indeed, $corec_S p$ is defined corecursively by $corec_S p(a) = 0$ if $p(a) = *$ and $\pred(\corec_S p(a)) = \corec_S p(a^\prime)$ if $p(a) = a^\prime \in S$.  In this way, $\bar{\mathbb{N}}$ is [[duality|dual]] to the [[natural number | natural number system]] $\mathbb{N}$ in its guise as a [[natural numbers object]].

You can think of $corec_S p$ as mapping an element $a$ of $S$ to the maximum number of times that $p$ can be applied in succession, starting from $a$, before being taken out of $S$.  Since this may never occur, we need $\infty$ as a possible value.  At the other extreme, if $p(a) = *$ then $p$ cannot be applied at all to $a$ before leaving $S$, so $corec_S p(a) = 0$.

Note that this universal property also holds constructively (which is why we can be sure that the constructive definition above is correct).  We define $pred$ constructively as follows:
$$
pred(x) = \begin{cases}
*                & if\; x_0 = 1 ,\\
(x_1,x_2,\ldots) & if\; x_0 = 0 .\end{cases}
$$


## Topology

We may naturally give $\bar{\mathbb{N}}$ a [[topological structure|topology]] giving it the structure of a [[compact Hausdorff space]]; unusually, this works even in weak constructive foundations (without having to use the [[fan theorem]] or pass to a [[locale]]).

We may define the topology simply (and constructively) as follows: a [[subset]] $G$ of $\bar{\mathbb{N}}$ is _[[open subset|open]]_ if, whenever $\infty \in G$, there is a finite $n$ such that $m \in G$ whenever $m \geq n$.  In other words, $G$ is a [[neighbourhood]] of $\infty$ just when almost every finite number also belongs to $G$.

In this way, $\bar{\mathbb{N}}$ is the [[Alexandroff compactification]] of the [[discrete space]] $\mathbb{N}$.  The space is obviously compact because, given an [[open cover]] $\mathcal{U}$, we have $\infty \in G \in \mathcal{U}$ for some $G$, so $G$ alone contains almost every point, and only finitely many more open sets are needed.

It is sometimes convenient to represent $\bar{\mathbb{N}}$ as a [[subspace]] of the [[real line]] $\mathbb{R}$, which we can do by interpreting the natural number $n$ as $2^{-n}$ and $\infty$ as $0$.  Constructively, the monotone bit sequence $x$ becomes the real number
$$ 
\frac{1}{2} {\sum_{i=0}^\infty x_i 2^{-i}}
,$$
which always converges.  Another common representation uses $1/(n+1)$ instead of $1/2^n$.

Given any topological space $X$, an [[infinite sequence]] in $X$ may be thought of as a [[continuous map]] to $X$ from the discrete space $\mathbb{N}$.  Then this sequence [[convergent sequence|converges]] iff this map can be extended to a continuous map on $\bar{\mathbb{N}}$.  For this reason, $\bar{\mathbb{N}}$ is sometimes called the __universal convergent sequence__.  (Strictly speaking, unless $X$ is at least [[sequentially Hausdorff space|sequentially Hausdorff]], a map to $X$ from $\bar{\mathbb{N}}$ contains more information than a sequence in $X$ with the property of convergence.)

This may all be generalised from sequences to other [[nets]]; given a [[directed set]] $D$, we form $\bar{D}$ by adjoining $\infty$ and taking $G \subseteq D$ as a neighbourhood of $\infty$ iff $G$ owns almost all of $D$.  (Constructively, this may require using locales for the general case.)


## In higher category theory

Concepts in [[higher category theory]] often come in $n$-versions where $n$ is an extended natural number.  (Sometimes it's also possible to give $n$ a few negative values as well; see [[negative thinking]].)  Typically, the $\infty$-version is all-encompassing, with the $n$-versions as special cases.  On the other hand, the $1$-version is usually more familiar outside of category theory.

See also [[categorification]].


## In constructive mathematics

The claim that every extended natural number is either finite or infinite is equivalent to the [[limited principle of omniscience]] ($LPO$) for natural numbers.  On the other hand, the $LPO$ for extended natural numbers is simply true; given any function from $\bar{\mathbb{N}}$ to $\{0,1\}$, it is either all $0$s or has a $1$.  See [Escard&#243; (2011)](#Escardo).


## References

*  [[Martín Escardó]] (2011) via constructivenews, [Infinite sets that satisfy the principle of omniscience in all varieties of constructive mathematics](http://www.cs.bham.ac.uk/~mhe/papers/omniscient-2011-07-06.pdf) (pdf)
{#Escardo}


[[!redirects extended natural number]]
[[!redirects extended natural numbers]]
[[!redirects extended natural number system]]
