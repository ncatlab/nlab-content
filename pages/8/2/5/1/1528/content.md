#Idea#

The _Moore path category_ of a [[topological space]] $X$ is a kind of [[path category]] whose collection of objects is $X$, and whose morphisms are _parameterized_ paths in $X$, i.e. continuous images of the interval $[0,t] \subset \mathbb{R}$ of length $t$, for all $0 \leq t \lt \infty$.

#Definition#

Let $X$ be a [[topological space]]. It **Moore path category** $P(X)$ has

* $Obj(P(X)) = X$

* $Mor(P(X)) = \sqcup_{t \in [0,\infty)} Top([0,t],X)$ .

Composition is the obvious concatenation of paths obtaibed by pullback along the injection maps

$$
  [0,t_1] \stackrel{1}{\hookrightarrow} [0, t_1 + t_2]
  \stackrel{(-)+t_1}{\leftarrow}
  [0,t_2]
  \,.
$$

The identity morphism at $x \in X$ is the unique path of length 0 at $x$, i.e the map ${*} = [0,0] \stackrel{x}{\to} X$ .