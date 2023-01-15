## Idea

The T-Grothendieck construction generalizes the [[displayed category]] construction to models of an [[algebraic theory]] T. The ordinary displayed category construction is the instance when T is the [[theory of categories]]. This construction forms an equivalence between models of T in the category of [[indexed sets]], and models of T in the [[arrow category]] of [[Set]]. The T-Grothendieck construction answers the following question: which objects classify morphisms of the models of an algebraic theory T?

## Definition

The T-Grothendieck construction relies on internalizing models of $T$ in the category of indexed sets and the arrow category of $Set$.
\begin{defn}
An indexed set is a function $f: X \to Set$. The set $X$ is called the indexing set, and the set $f(x)$ for $x \in X$ is called the fiber over $x$.
\end{defn}
\begin{defn}
Let $IndSet$ be the category whose objects are functions $a: X \to Set$ and a morphism from $a$ to $b: Y \to Set$ is a function $f: X \to Y$ and an $X$-indexed family of functions $\alpha_x: a(x) \to b(f(x))$. Let $Set^{\to}$ be the arrow category of Set.
\end{defn}

The T-Grothendieck construction is the forward direction of the following equivalence:

\begin{theorem}
There is an equivalence of categories
\[ \int_T : [T,IndSet] \cong [T,Set^{\to}]\]
\end{theorem}

\begin{proof}
There is an equivalence of categories
\[ IndSet \cong Set^{\to}\]
An indexed set $f : X \to Set$ is sent to the function $p: \int f \to X$ where 
$\int f = \{ (x,a) | a \in f(x) \}$ and $p$ is the projection onto the first coordinate. The inverse mapping of this equivalence sends a function $f: Y \to X$ to its preimage mapping $f^{-1}: X \to Set$. The functor category is a [[2-functor]]
\[ [T,-] : Cat \to Cat \]
sending a category $C$ to the functor category $[T,C]$, sending a functor $F: C \to D$ to the functor from $[T,F]:[T,C]\to [T,D]$ given by composition with $F$, and sending a natural transformation $\alpha : F \Rightarrow G$ to the natural transformation $[T,\alpha]: [T,F] \Rightarrow [T,G]$ given by [[whiskering]] the functors in the image of $[T,F]$ by $\alpha$. Because every 2-functor preserves equivalences, the equivalence $IndSet \cong Set^{\to}$ is sent to the desired one.
\end{proof}

## Examples

* When T is the [[theory of categories]] we recover the [[displayed category]] construction. This relies on an equivalence
\[ [Th(Cat),IndSet] \cong Cat/Span_{lax} \]
where the latter category is the category of displayed categories i.e.\ lax functors into the [[bicategory of spans]] and functional natural transformations between them. 
* When T is the theory of graphs, we get an equivalence
\[ Grph/USpan \cong Grph^{\to}\]
between the category of graph morphisms with codomain $USpan$, the graph whose vertices are sets and whose edges are spans and the arrow category of $Grph$. This example is like the previous example but with less structure.
* When T is the theory of monoids we get an equivalence
\[ [Th(Mon),IndSet] \cong Mon^{\to} \]
which unpacks morphisms of monoids into "indexed monoids" i.e.\ indexing monoids $M$ equipped with fiberwise monoids whose operations are coherent with the operations of $M$.