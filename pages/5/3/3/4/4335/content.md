A __pseudonatural transformation__ is a [[lax natural transformation]] whose $2$-cell components are all [[invertible 2-morphism|invertible]].  More precisely:

+-- {: .un_def} 
######Definition 
Given two 2-functors $U, V: S \stackrel{\to}{\to} C$ between 2-categories, a **pseudonatural transformation** $\phi: U \to V$ is a rule that assigns to each 0-cell $s$ of $S$ a 1-cell $\phi(s): U(s) \to V(s)$ of $C$, and to each 1-cell $f: r \to s$ of $S$ an invertible 2-cell $\phi(f)$ of $C$:  
$$\array{
U(r) & \stackrel{U(f)}{\to} & U(s) \\
\phi(r) \downarrow & \phi(f) \swArrow & \downarrow \phi(s) \\
V(r) & \underset{V(f)}{\to} & V(s)
}$$ 
such that the following pasting diagram equalities hold: 
$$\array{
U(r) & \stackrel{U(f)}{\to} & U(s) & \stackrel{U(g)}{\to} & U(t) & & U(r) & \stackrel{U(g f)}{\to} & U(t) & & \\
\phi(r) \downarrow & \phi(f) \swArrow & \downarrow \phi(s) & \phi(g) \swArrow & \downarrow \phi(t) & = & \phi(r) \downarrow & \phi(g f) \swArrow & \downarrow \phi(t) & & & \\
V(r) & \underset{V(f)}{\to} & V(s) & \underset{V(g)}{\to} & V(t) & & V(r) & \underset{V(g f)}{\to} & V(t) & & & 
}$$
and
$$\array{
 U(r) & \stackrel{U(1_r)}{\to} & U(r) & & \\
\phi(r) \downarrow & \phi(1_r) \swArrow & \downarrow \phi(r) & = & 1_{\phi(r)} \\
V(r) & \underset{V(1_r)}{\to} & V(r) & & 
}$$
=-- 


[[!redirects pseudonatural transformation]]
[[!redirects pseudonatural transformations]]
[[!redirects pseudo-natural transformation]]
[[!redirects pseudo-natural transformations]]
[[!redirects pseudo natural transformation]]
[[!redirects pseudo natural transformations]]
