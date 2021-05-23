
> This entry is about loops in [[topology]]. For loops in the sense of  [[algebra]] see at *[[loop (algebra)]]*, also at *[[quasigroup]]* and *[[Moufang loop]]*.

***


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



# Loops
* table of contents
{: toc}

## Definitions

In [[topology]], a (parametrised, oriented) __loop__ in a [[space]] $X$ is a map (a [[morphism]] in an appropriate [[category]] of spaces, such as a [[continuous function]] between [[topological spaces]]) to $X$ from the [[circle]] $S^1 = \mathbb{R}/\mathbb{Z}$. Hence a continuous [[path]] whose endpoints coincide.

A __loop at $a$__ is a loop $f$ such that $f(k) = a$ for any (hence every) [[integer]] $k$.  An __unparametrised loop__ is an [[equivalence class]] of loops, such that $f$ and $g$ are equivalent if there is an [[monotone function|increasing]] [[automorphism]] $\phi$ of $S^1$ such that $g = f \circ \phi$.  An __unoriented loop__ is an equivalence class of loops such that $f$ is equivalent to $(x \mapsto f(-x))$.  A __Moore loop__ has domain $\mathbb{R}/n \mathbb{Z}$ for some [[natural number]] (or possibly any [[real number]]) $n$.  All of these variations can be combined, of course.  (A Moore loop at $a$ has $f(k n) = a$ instead of $f(k) = a$.  Also, a Moore loop for $n = 0$ is simply a [[point]], so possibly there is a better way to define this to avoid making this exception.  Finally, there is not much difference between unparametrised loops and unparametrised Moore loops, since we may interpret $(t \mapsto n t)$ as a reparametrisation $\phi$.)

In [[graph theory]], a __loop__ is an edge whose endpoints are the same vertex.  Actually, this is a special case of the above, if we interpret $S^1$ as the graph with $1$ vertex and $1$ edge; in this way, the other variations become meaningful.  In this context, a Moore loop is called a __cycle__.  (However, as the only directed graph automorphism of $S^1$ is the [[identity morphism|identity]], parametrisation is trivial for directed graphs and equivalent to orientation for undirected graphs.)

Every loop may be interpreted as a [[path]].  Sometimes a loop, say at $a$, is *defined* to be a path from $a$ to $a$.  However, this is correct only in certain contexts.  In graph theory, it\'s incorrect, but only because of terminological conventions; the idea is sound.  In [[continuous spaces]], it is also correct.  However, in [[smooth spaces]], it is not correct, since the [[derivatives]] at the endpoints should also agree; the same holds in many other more structured contexts.


## Concatenation

Given two Moore loops $f$ and $g$ at $a$, the __concatenation__ of $f$ and $g$ is a Moore loop $f ; g$ or $g \circ f$ at $a$.  If the domain of $f$ is $\mathbb{R}/m \mathbb{Z}$ and the domain of $g$ is $\mathbb{R}/n \mathbb{Z}$, then the domain of $f ; g$ is $\mathbb{R}/(m+n) \mathbb{Z}$, and
$$ (f ; g)(x) \coloneqq \left \{ \array { f(x) & \quad x \leq m \\ g(m+x) & \quad x \geq m .} \right . $$
In this way, we get a [[monoid]] of Moore loops in $X$ at $a$, with concatenation as multiplication.  This monoid may called the __[[Moore loop monoid]]__.

Often we are more interested in a [[quotient]] monoid of the Moore loop monoid.  If we use unparametrised loops (in which case we may use loops with domain $S^1$ if we wish), then we get the __unparametrised [[loop monoid]]__.  If $X$ is a [[smooth space]], then we may additionally identify loops related through a [[thin homotopy]] to get the __[[loop group]]__.  Finally, if $X$ is a [[continuous space]] and we identify loops related through any (basepoint-preserving) [[homotopy]], then we get the __[[fundamental group]]__ of $X$.

See [[looping]] and [[delooping]] for more.


## Related entries

* [[loop]]

* [[path]],

* [[loop space]],

* [[fundamental group]].


[[!redirects Moore loop]]
[[!redirects Moore loops]]
