## Idea ##

Given a finite [[n-poset]] $C$, its _Hasse n-graph_ encodes the minimal amount of information necessary to reproduce the ordering relation.

## Definition ##

Given an [[n-poset]] $C$, a **Hasse $n$-graph** $H$ is a [[directed n-graph]] whose $n$-[[n-quiver|quiver]] $F(H)$ is [[equivalence|equivalent]] to $C$.

+-- {: .query}
As with [[Hasse diagram]], I *think* that declaring it to be smallest in unnecessary; the fact that it is merely an $n$-graph and not a $n$-category will do this.  But this should be an $n$-quiver, yes?  ---Toby

[[Eric]]: What should be an n-quiver? I thought I'd stick the "smallest" in there because if $x\lt y$, $y\lt z$ then the morphisms $x\to y$, $y\to z$, and $x\to z$ are in the quiver, but only $x\to y$ and $y\to z$ need to be in the Hasse diagram. However, we could have a graph including $x\to z$, but this would not be a Hasse diagram. Maybe I'm confused.

=--