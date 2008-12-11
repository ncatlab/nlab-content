A graph $G = (G_0,G_1)$ is a collection of nodes $G_0$ and edges $G_1$.

A directed graph $DG = (G,s,t)$ is a graph $G$ together with source maps

$$s:G_1\to G_0$$

and target maps

$$t:G_1\to G_0.$$

Note that this definition includes multigraphs, i.e. graphs with distinct edges $e,e'\in G_1$ such that $s(e) = s(e')$ and $t(e) = t(e')$, as well as loops, i.e. edges with $s(e) = t(e)$.