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
there is a map $\hat{g}:Y\times I \to E$ such that $f\circ \hat{g} = g$ and there is a vertical homotopy between $\hat{g}(-,0):Y\to E$ and $g_0$.

A map is a **Dold fibration** if it has the WCHP for all spaces.


## Examples and counter-examples

Any [[Hurewicz fibration]] is a Dold fibration

[[Serre fibration]]s are _not_ Dold fibrations, and there is a very simple counter-example. Consider the union of line segments
$$
E:= [-1,0]\times\{2\} \cup \{0\}\times [1,2] \cup [0,1]\times\{1\}
$$
in $\mathbf{R}^2$, and the map projecting on to the first coordinate, $pr_1:E \to [-1,1]$. Then this map is a Dold fibration but not a Serre fibration.

One could consider maps that have the WCHP for just cubes -- these are a sort of hybrid Dold--Serre fibration (warning! nonstandard terminology. I just made it up, suggestions appreciated). For these maps there exists a [[long exact sequence]] in homotopy once basepoints are chosen. For classes of maps determined by (homotopy) lifting properties, this is about the minimum one needs to define such a long exact sequence. On the other hand, [[quasifibration|quasifibrations]] give rise to a long exact sequence in homotopy, but are defined by homotopy properties of the fibres.
