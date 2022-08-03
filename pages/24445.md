Let $X$ be a [[set]]. The usual operations [[intersection]], [[union]], [[symmetric difference]], [[complement]]... on the [[subsets]] of $X$ can be presented in an homogeneous way using an operation $\multiscripts{_^n}{\Delta}{_i^j}:\mathcal{P}(X)^{\times n} \rightarrow \mathcal{P}(X)$ for every $n \ge 1$ and $0 \le i \le j \le n$. The [[operad]] thus generated gives much more operations.

For every $n \ge 1$, $A_{1},...,A_{n}$ subsets of $X$, and $0 \le i \le j \le n$, define the set:
$
\multiscripts{_^n}{\Delta}{_i^j}(A_{1},...,A_{n}) = \{x \in A_{1} \cup ... \cup A_{n}, i \le |k \in [1,n], x \in A_{k}| \le j\}
$

We then have:

* $A_{1} \cap ... \cap A_{n} = \multiscripts{_^n}{\Delta}{_n^n}(A_{1},...,A_{n})$
* $A_{1} \cup ... \cup A_{n} = \multiscripts{_^n}{\Delta}{_1^n}(A_{1},...,A_{n})$
* $A_{1} \Delta A_{2} = \multiscripts{_^2}{\Delta}{_1^1}(A_{1}, A_{2})$ 
* $\emptyset = \multiscripts{_^2}{\Delta}{_1^1}(A_{1},A_{1})$
* $X = \multiscripts{_^n}{\Delta}{_0^n}(A_{1},...,A_{n})$
* $X - A_{1} = \multiscripts{_^1}{\Delta}{_0^0}(A_{1})$
* $A_{1} = \multiscripts{_^1}{\Delta}{_1^1}(A_{1})$

We also have:

* $X - (A_{1} \cup ... \cup A_{n}) = \multiscripts{_^n}{\Delta}{_0^0}(A_{1},...,A_{n})$
* $X - (A_{1} \cap ... \cap A_{n}) = \multiscripts{_^n}{\Delta}{_0^{n-1}}(A_{1},...,A_{n})$
* $\multiscripts{_^n}{\Delta}{_1^1}(A_{1},...,A_{n})$ is the set of elements which are in exactly one $A_{i}$.

We get an operad by starting with the operations $\multiscripts{_^n}{\Delta}{_i^j}$ and composing them together.
