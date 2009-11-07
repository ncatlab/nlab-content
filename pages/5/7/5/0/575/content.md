# Definition #

A **Galois connection** is a [[dual adjunction]] between [[partial order|poset]]s.

More explicitly, given posets $A$ and $B$, a Galois connection between $A$ and $B$ is a pair of order-reversing maps $f:A\to B$ and $g:B\to A$ such that $a\le g(f(a))$ and $b\le f(g(b))$ for all $a\in A$, $b\in B$.

A **Galois correspondence** is a Galois connection which is an adjoint equivalence (so $a = g(f(a))$ and $b = f(g(b))$ for all $a \in A$, $b \in B$). 

# Examples #

* Frequently Galois connections between collections of [[subset]]s arise where $f(a)$ is "the set of all $y$ standing in some relation to every $x\in a$" and dually $g(b)$ is "the set of all $x$ standing in some relation to every $y\in b$."  See [[orthogonality]] for one example. 

In fact, every Galois connection between full power sets, 

$$(f: P(X) \to P(Y)^{op}) \dashv (g: P(Y)^{op} \to P(X))$$

is of just such a form: there is some relation $r$ from $X$ to $Y$ such that 

$$f(S) = \{y: \forall_{x \in X} x \in S \Rightarrow r(x, y)\}, \qquad g(T) = \{x: \forall_{y \in Y} y \in T \Rightarrow r(x, y)\}$$ 

Indeed, define $r: X \times Y \to \mathbf{2}$ by stipulating that $r(x, y)$ is true if and only if $y \in f(\{x\})$. Because $f$ is a left adjoint, it takes colimits in $P(X)$ (in this case, unions) to colimits in $P(Y)^{op}$, which are intersections in $P(Y)$. Since every $S$ in $P(X)$ is a union of singletons $\{x\}$, this gives 

$$f(S) = \bigcap_{x \in S} f(\{x\}) = \{y: \forall_{x \in S} r(x, y)\}$$ 

which is another way of writing the formula for $f$ given above. We observe that 

$$T \subseteq f(S) = \{y: \forall_{x \in S} r(x, y)\}$$ 

if and only if 

$$S \times T \subseteq r$$ 

(now viewing $r$ extensionally in terms of subsets). This last symmetrical expression in $S$ and $T$ means 

$$S \subseteq g(T) := \{x: \forall_{y \in T} r(x, y)\}$$ 

which means we have a Galois connection between $f$ and $g$ under this definition; since $g$ is uniquely determined by the presence of a Galois connection with $f$, we conclude that all Galois connections between power sets arise in this way, via a relation $r$ between $X$ and $Y$. 

* The Galois theory normally taught in graduate-level algebra courses (and based on the work of &#201;variste Galois) involves a Galois connection between the intermediate [[field]]s of a [[Galois extension]] and the subgroups of the corresponding [[Galois group]].