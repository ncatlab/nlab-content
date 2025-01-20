
\tableofcontents

## Definitions

A **strict preorder** or **strict quasiorder** on a set $S$ is a (binary) [[relation]] $\lt$ on $S$ that is both [[irreflexive relation|irreflexive]] and [[transitive relation|transitive]].  That is:

* $x \nless x$ always;
* If $x \lt y \lt z$, then $x \lt z$.

A **strictly preordered set**, or **strict proset**, is a [[set]] equipped with a strict preorder.

## Properties

\begin{theorem}
Strict preorders orders are asymmetric.
\end{theorem}

\begin{proof}
Transitivity of $\lt$ says that for all $x \in S$ and $y \in S$, $x \lt y$ and $y \lt x$ implies $x \lt x$. However, irreflexivity says that for all $x$, $x \leq x$ is always false. This implies that for all $x$ and $y$, $x \lt y$ and $y \lt x$ is always false, which is precisely the condition of asymmetry. 
\end{proof}

As a result, sometimes the term *[[strict partial order]]* is used for strict preorders, since they are always asymmetric. However, the term "strict partial order" is also used for other order relations. 

## In constructive mathematics

Unlike with other notions of [[order]], a set equipped with a strict preorder cannot be [[constructive mathematics|constructively]] understood as a kind of [[enriched category]] (at least, not as far as I know ...).  Using [[excluded middle]], however, a strict preorder is the same as a [[partial order]]; interpret $x \leq y$ literally to mean that $x \lt y$ or $x = y$, while $x \lt y$ conversely means that $x \leq y$ but $x \ne y$.

Instead, the relation $\lt$ should be defined as an [[irreflexive comparison]] when generalising mathematics to other categories and to constructive mathematics. 

If a strict preorder satisfies comparison (if $x \lt z$, then $x \lt y$ or $y \lt z$), then it is a [[strict weak order]], and additionally, if it is a [[connected relation]], it is a [[pseudo-order]], and if it satisfies [[trichotomy]], it is a [[strict total order]].

There are also certainly examples of strictly preordered sets that are also partially ordered, where $\lt$ and $\leq$ (while related and so denoted with similar symbols) don\'t correspond as above. For example, if $A$ is any [[inhabited set]] and $B$ is any [[linearly ordered set]], then the [[function set]] $B^A$ is partially ordered with $f \leq g$ meaning that $f(x) \leq g(x)$ always and strictly preordered with $f \lt g$ meaning that $f(x) \lt g(x)$ always. Except in degenerate cases, it\'s quite possible to have $f \ne g$, $f \nless g$, and $f \leq g$ simultaneously.

## Related concepts

* [[preorder]]
* [[strict total order]]

## References

* Wikipedia, *[Strict preorder](https://en.wikipedia.org/wiki/Strict_preorder)*

* Wikipedia, *[Strict partial order](https://en.wikipedia.org/wiki/Strict_partial_order)*

[[!redirects strict preorder]]
[[!redirects strict preorders]]
[[!redirects strict preordering]]
[[!redirects strict preorderings]]
[[!redirects strictly preordered]]
[[!redirects strictly preordered set]]
[[!redirects strictly preordered sets]]
