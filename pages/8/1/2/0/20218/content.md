
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

A Baire lattice is a [[lattice|lattice theoretic]] abstraction of the [[Baire space|Baire property]] of a topological space. In parallel to the fact that every [[complete space|complete metric space]] is a Baire space every [[continuous poset|continuous lattice]] is a Baire lattice.

## Definitions

Recall that a [[complete lattice]] is a [[partial order|poset]] which has all small [[join|joins]] and [[meet|meets]]. For $a, b \in L$, we say that $a$ is __way below__ $b$ and write $a \ll b$ if whenever $S \subseteq L$ is a [[directed subset]] and $b \leq \bigvee S$ (where $\bigvee S$ denotes the [[join]] of $S$), then there exists $s \in S$ with $a \leq s$. Further we say that $L$ is __[[continuous lattice|continuous]]__ if for every $a\in L$, the subset
$$ \Downarrow (a) \coloneqq \{ b \in L | b \ll a \} $$
is directed and has join $a$.

For example the [[category of open subsets|lattice of open subsets]] of a topological space is a continuous lattice if and only if the [[sobrification]] of the topological space is [[locally compact]] (i.e. the topology has a basis of compact neighborhoods).


\begin{defn}
An element $p \in L$ is called __irreducible__ if $a \vee b = p$ implies $p = a$ or $p = b$.
\end{defn}

To illustrate this definition think of an [[irreducible topological space|irreducible subset]] of a topological space.

\begin{defn}
An element $d\in L$ is __dense__ if for all $a\in L$ the relation $ a \neq \bot $ implies that $ d \wedge a \neq \bot $.
\end{defn}

\begin{defn}
A [[complete lattice]] $L$ is called a __Baire lattice__ if for any countable family of dense elements $N \subset L$ and each nonzero element $u \in L$ there is an irreducible element $p \in L$ such that $ d \wedge u \nleq p $ for all $d \in N$.
\end{defn}

## Theorem

\begin{theorem}
Every continuous lattice is a Baire lattice.
\end{theorem}


## Example

Let $X$ be a [[sober space|sober]] [[topological space]]. Then the lattice of opens of $X$ is Baire if and only if the topological space $X$ has the [[Baire space|Baire property]].

## Related pages

 * [[complete lattice]]
 * [[Baire category theorem]]
 * [[Baire space]]

## References

The concept appeared in:

 * [[Karl Heinrich Hofmann]], _A note on Baire spaces and continuous lattices_ 1980. Bulletin of the Australian Mathematical Society, 21(2), pp. 265-279. ([doi:10.1017/S0004972700006080]( https://doi.org/10.1017/S0004972700006080))

Textbook accounts:

 * G. Gierz, [[Karl Heinrich Hofmann]], K. Keimel, J. D. Lawson, M. Mislove, [[Dana Scott]], _Continuous Lattices and Domains_ 2003, Vol. 93 of _Encyclopedia of Mathematics and its Applications_ ([doi:10.1017/CBO9780511542725](https://doi.org/10.1017/CBO9780511542725))


[[!redirects Baire lattices]]
