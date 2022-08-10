My super small edit.

Let $X$ be a set. The usual operations intersection, union, symmetric difference, complementary... on the subsets of $X$ can be presented in an homogeneous way using an operation $\multiscripts{_^n}{\Delta}{_i^j}:\mathcal{P}(X)^{\times n} \rightarrow \mathcal{P}(X)$ for every $n \ge 1$ and $0 \le i \le j \le n$. The operad thus generated gives much more operations.

For every $n \ge 1$, $A_{1},...,A_{n}$ subsets of $X$, and $0 \le i \le j \le j$, define the set:
$
\multiscripts{_^n}{\Delta}{_i^j}(A_{1},...,A_{n}) = \{x \in A_{1} \cup ... \cup A_{n}, i \le |k \in [1,n], x \in A_{k}| \le j\}
$

We then have:

* $A_{1} \cap ... \cap A_{n} = \multiscripts{_^n}{\Delta}{_n^n}(A_{1},...,A_{n})$
* $A_{1} \cup ... \cup A_{n} = \multiscripts{_^n}{\Delta}{_1^n}(A_{1},...,A_{n})$
* $A_{1} \Delta A_{2} = \multiscripts{_^n}{\Delta}{_1^1}(A_{1}, A_{2})$ 
* $\emptyset = \multiscripts{_^n}{\Delta}{_1^1}(A_{1},A_{1})$
* $X = \multiscripts{_^n}{\Delta}{_0^n}(A_{1},...,A_{n})$
* $X - A_{1} = \multiscripts{_^n}{\Delta}{_0^0}(A_{1})$
* $A_{1} = \multiscripts{_^n}{\Delta}{_1^1}(A_{1})$

\linebreak

Knots for quantum computation from defect branes

Already 25 years ago, Kitaev famously proposed that intrinsically fault-tolerant quantum computation should be possible by knotting the worldlines of defect points in effectively 2-dimensional quantum materials akin to graphene. Meanwhile, there have been striking advances (a) in the theoretical understanding of such quantum materials, in terms of topological K-theory and (b) in the practical construction of toy quantum computers -- but the "topological quantum gates" proposed by Kitaev have remained somewhat elusive, both practically but also theoretically. Recently we have shown that a previously neglected sector of topological K-theory in its fully-fledged "twisted & equivariant & differential" refinement does reflect exactly those topological quantum gates that are thought to be practically realizable -- namely the "su(2)-anyon braid gates". This insight was drawn from the study of "defect branes" in string theory and points to a fully non-perturbative enhancement of what is known as "holographic" condensed matter theory. I will give a gentle exposition and motivation of these results, which are joint work with Hisham Sati at CQTS. Talk slides and further pointers may be found at: https://ncatlab.org/schreiber/show/Erice+2022


\linebreak

## The logic at work

### Differentiating a proof

We start from a proof of $!A \vdash B$ and by using as only exponential rules cocontraction and codereliction, we obtain a proof of $!A \vdash A \multimap B$. In the co-Kleisli category we thus go from a morphism $f:A \rightarrow B$, which must be interpreted as a smooth function, to a morphism $df: A \rightarrow (A \multimap B)$. It is the differential of $f$ which associate to every point of $A$ the linear approximation of $f$ around this point.

$$
\frac{\frac{\frac{\frac{\frac{}{!A \vdash !A}^{ax} \frac{\frac{}{A \vdash A}^{ax}}{A \vdash !A}}{!A,A \vdash !A} !A \vdash B}{!A,A \vdash B}}{!A \vdash A^{\perp},B}}{!A \vdash A \multimap B}
$$