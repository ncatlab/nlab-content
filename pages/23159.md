# Timed set
* this block creates the table of contents, leave as is
{: toc}

## Idea

Some [[function|functions]] are more expensive to calculate than others. Additionally, calculation with large values is more expensive than with small values. A [[category]] of timed sets has additional [[structure]] which measures the cost of computation for each function.

When properly qualified and constructed, categories of timed sets can provide categorical descriptions of [[complexity class|complexity classes]].


## Definition

\begin{defn}
\label{size monoids}
A size monoid is a [[commutative monoid]] with a partial order $\leq$ such that
$$
\underset{m \in M}{\forall} \;\; 0 \leq m
$$
and if $a \leq b$ and $c \leq d$ then $a + c \leq b + d$.
\end{defn}

\begin{defn}
\label{timed maps}
For a size monoid $M$, a timed map $f$ is a [[partial function]] $X \to Y$ and a partial cost function called the timing, $|-|_f : X \to M$ which are defined on the same [[element|elements]] of $X$.
\end{defn}

Given a size monoid $M$, there is a category $\mathtt{TSet}(M)$ of sets and $M$-timed maps. The identity morphism has the [[zero function]] for timing. The composition of the cost of two morphisms $f : X \to Y$ and $g : Y \to Z$ is given by

$$
|x|_{g \circ f} = |x|_f + |f(x)|_g
$$

## Properties

As categories of sets and partial functions, categories of timed sets are [[restriction category|restriction categories]].


## Examples

The complexity classes [[PTIME]] and [[LOGSPACE]] can be described by categories of timed sets.


## Related articles

* [[complexity theory]]
* [[Turing category]]


## References

Timed sets were introduced in:

* [[Robin Cockett]], [[Joaquín Díaz-Boils]], [[Jonathan Gallagher]], [[Pavel Hrubeŝ]], _Timed Sets, Functional Complexity, and Computability_, Electronic Notes in Theoretical Computer Science, volume 286, 2012 ([doi:10.1016/j.entcs.2012.08.009](https://doi.org/10.1016/j.entcs.2012.08.009))