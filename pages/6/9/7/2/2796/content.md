### Idea ###

A _thin homotopy_ between paths $f,g:I \to X$ in a topological space $X$ is a map $I\times I \to I$ which, roughly speaking, has zero area. 

### Thin homotopies in smooth spaces ###  

A (smooth) homotopy $F:I\times I \to X$ between smooth paths in a smooth space $X$  is called **thin** if the rank of $dF(s,t)$ is always less than 2.

(More here...)

### Thin homotopies in topological spaces ###

The following is taken from

* K.A. Hardie, K.H. Kamps, R.W. Kieboom _A homotopy 2-groupoid of a Hausdorff space_, Appl. Cat. Str.**8** (2000).

We define a _finite tree_ to be a one-dimensional finite polyhedron.

A homotopy $F:I\times I \to X$ between paths $F(-,0)$ and $F(-,1)$ in the topological space $X$ is called **thin** if $F$ factors through a finite tree,
$$
  I\times I \stackrel{F_0}{\to} T \stackrel{F_1}{\to} X
$$
such that the paths $F_0(-,0):I\to T$, $F_0(-,1):I\to T$ are piecewise-linear.

When $X$ is Hausdorff, points, paths and thin homotopies in $X$ form a bigroupoid.