The __extended natural number system__, denoted $\bar{\mathbb{N}}$, consists of all of the [[natural number]]s together with an extra number representing [[infinity]].

## Definition

Classically, $\bar{\mathbb{N}}$ is the [[disjoint union]] of the set $\mathbb{N}$ of natural numbers and a [[point]] $\{\infty\}$.  That is,
$$ \bar{\mathbb{N}} = \{0,1,2,\ldots,\infty\} .$$

In [[constructive mathematics]], a more careful definition is required; it is *not* constructively valid that every natural number is either finite or infinite (although it is valid that any that is not finite is infinite), and [[Markov's principle]] is the converse.)  Instead, we define $\bar{\mathbb{N}}$ as the set of infinite [[sequence]]s $x$ of $0$ or $1$ with the property that $x_i = 0$ if $x_j = 0$ for any $j \leq i$.  Then the natural number $n$ is identified with a sequence of $n$ copies of $1$ followed by $0$s, while infinity is identified with a sequence of all $1$s.

## Universal property

$\bar{\mathbb{N}}$ comes naturally equipped with a map $pred: \bar{\mathbb{N}} \to 1 + \bar{\mathbb{N}}$ as defined below:
$$
pred(x) = \begin{cases}
*      & if\; x = 0 ,\\
n      & if\; x = n + 1 ,\\
\infty & if\; x = \infty .\end{cases}
$$

Thus, it is a [[coalgebra]] for the endofunctor $H(X) = 1 + X$ on [[Set]], and indeed is the [[terminal coalgebra]] for $H$.  That is, given any set $S$ and map $p: S \to 1 + S$, there is a unique map $corec_S p: S \to \mathbb{N}$ such that
$$ \array {
S                      & \stackrel{p}\to    & 1 + S \\
\downarrow_{corec_S p} &                    & \downarrow_{\id_1 + corec_S p} \\
\bar{\mathbb{N}}       & \stackrel{pred}\to & 1 + \bar{\mathbb{N}}
} $$
commutes.  In this way, $\bar{\mathbb{N}}$ is [[duality|dual]] to the natural number system $\mathbb{N}$ in its guise as a [[natural numbers object]].

You can think of $corec_S p$ as mapping an element $a$ of $S$ to the number of times that $p$ must be applied in succession, starting from $a$, before being taken out of $S$.  Since this may never occur, we need $\infty$ as a possible value.

Note that this universal property also holds constructively (which is why we can be sure that the constructive definition above is correct).  We define $pred$ as follows:
$$
pred(x) = \begin{cases}
*                & if\; x_0 = 0 ,\\
(x_1,x_2,\ldots) & if\; x_0 = 1 .\end{cases}
$$