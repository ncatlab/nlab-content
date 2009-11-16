## Idea ##

A **Dold fibration** is a map that allows [[lifting]] of [[homotopies]], with initial condition agreeing with a given map up to a [[vertical homotopy]].


## Definition ##

The map $f:E \to B$ is said to have the **weak covering homotopy property** (WCHP) for the space $Y$ if for all squares

$$
\begin{matrix}
  Y\times\{0\}& \stackrel{g_0}{\to} & E \\
  \downarrow&&\, \downarrow f\\
  Y\times I &\underset{g}{\to} & B
\end{matrix}
$$
there is a map $\hat{g}:Y\times I \to E$ such that $f\circ \hat{g} = g$ and there is a vertical homotopy between $\hat{g}(-,0):Y\to E$ and $g_0$. The synonym expression _weak homotopy lifting property_ (WHLP) is also used. 

A continuous map is a **Dold fibration** if it has the WCHP for all spaces. Somewhat surprisingly, there is an equivalent condition in terms of delayed homotopies. A __delayed homotopy__ is a homotopy $H:Y\times I\to Z$ such that $H(y,t)=H(y,0)$ for $0\leq t\leq t_0$ for some $t_0\gt 0$.
A continuous map is a Dold fibration iff in the diagram above in which $g$ is a delayed homotopy, can be filled with a diagonal map $\hat{g}:Y\times I \to E$ such that the diagram is strictly commutative. It is of course not required that $\hat{g}$ be delayed (one can require, but then one allows $t_0$ for $\hat{g}$ to be possibly smaller than $t_0$ for $g$). This is sometimes called __delayed homotopy lifting property__. 

## Examples and counter-examples

Any [[Hurewicz fibration]] is a Dold fibration

[[Serre fibration]]s are _not_ Dold fibrations, and there is a very simple counter-example. Consider the union of line segments
$$
E:= [-1,0]\times\{2\} \cup \{0\}\times [1,2] \cup [0,1]\times\{1\}
$$
in $\mathbf{R}^2$, and the map projecting on to the first coordinate, $pr_1:E \to [-1,1]$. Then this map is a Dold fibration but not a Serre fibration.

One could consider maps that have the WCHP for just cubes -- these are a sort of hybrid Dold--Serre fibration (warning! nonstandard terminology. I just made it up, suggestions appreciated). For these maps there exists a [[long exact sequence]] in homotopy once basepoints are chosen. For classes of maps determined by (homotopy) lifting properties, this is about the minimum one needs to define such a long exact sequence. On the other hand, [[quasifibration|quasifibrations]] give rise to a long exact sequence in homotopy, but are defined by homotopy properties of the fibres.
