
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Paths
* table of contents
{: toc}

## Definitions

In [[topology]], a (parametrised, oriented) __path__ in a [[space]] $X$ is a map (a [[morphism]] in an appropriate [[category]] of [[spaces]], such as a [[continuous function]] between [[topological space]]) to $X$ from the [[topological interval]] $\mathbb{I} = [0,1]$.  

A __path from $a$ to $b$__ is a path $f$ such that $f(0) = a$ and $f(1) = b$.  
An __unparametrised path__ is an [[equivalence class]] of paths, such that $f$ and $g$ are equivalent if there is an [[monotone function|increasing]] [[automorphism]] $\phi$ of $\mathbb{I}$ such that $g = f \circ \phi$.  An __unoriented path__ is an equivalence class of paths such that $f$ is equivalent to $(x \mapsto f(1 - x))$.  

If $P$ is a path, then its __reverse path__[^1], denoted $\overline{P}$, is defined to be the composite $P \circ ( t\mapsto 1-t )$. 
The operation $P\mapsto\overline{P}$ is called _path reversal_.

[^1]: Cf. e.g. [[Introduction to Topology -- 2]], or also [Section 2.1](#tomDieck2008); beware that that reference, (0) like many others, uses the term "inverse path", even though the operation of concatenation of paths does not *in and of itself* yield a [[strict category|strict groupoid]], in which $\overline{P}$ would be an inverse, and (1) that it uses $a$ and $b$ for the endpoints of the _interval_, not the endpoints of the paths in the space $X$, and (2) that it uses $P^-$ instead of $\overline{P}$, which however is less suited for notational iterating (compare $\overline{\overline{P}}=P$ with $(P^-)^-=P$), and that (3)  the 2008 edition has a typo: " $w(1-t)$ " in loc. cit., when   *inverse path* gets defined, should be $u(1-t)$.

A __Moore path__ is defined like a path, except for having another domain: replace $[0,1]$ with the interval $[0,n]$ for some [[natural number]] (or, more commonly, any non-negative [[real number]]) $n$.  All of these variations can be combined, of course.  (For unoriented paths, one usually says 'between $a$ and $b$' instead of 'from $a$ to $b$'.  Also, a Moore path from $a$ to $b$ has $f(n) = b$ instead of $f(1) = b$.  Finally, there is not much difference between unparametrised paths and unparametrised Moore paths, since we may interpret $(t \mapsto n t)$ as a reparametrisation $\phi$.)

In [[graph theory]], a __path__ is a [[list]] of edges, each of which ends where the next begins.  Actually, this is a special case of the above, if we use Moore paths and interpret $[0,n]$ as the linear graph with $n + 1$ vertices and $n$ edges; in this way, the other variations become meaningful.  (However, as the only directed graph automorphism of $[0,n]$ is the [[identity morphism|identity]], parametrisation is trivial for directed graphs and equivalent to orientation for undirected graphs.  Note that a non-Moore path is simply an edge, one of the fundamental ingredients of a graph.)


## Concatenation

Given a Moore path $f$ from $a$ to $b$ and a Moore path $g$ from $b$ to $c$, the __concatenation__ of $f$ and $g$ is a Moore path $f ; g$ or $g \circ f$ from $a$ to $c$.  If the domain of $f$ is $[0,m]$ and the domain of $g$ is $[0,n]$, then the domain of $f ; g$ is $[0,m+n]$, and
$$ (f ; g)(x) \coloneqq \left \{ \array { f(x) & \quad x \leq m \\ g(x-m) & \quad x \geq m .} \right . $$
In this way, we get a ([[strict category|strict]]) [[category]] whose [[objects]] are [[global element|points]] in $X$ and whose [[morphisms]] are Moore paths in $X$, with concatenation as [[composition]].  This category is called the __[[Moore path category]]__.

Often we are more interested in a [[quotient category]] of the Moore path category.  If we use unparametrised paths (in which case we may use paths with domain $\mathbb{I}$ if we wish), then we get the __unparametrised [[path category]]__.  If $X$ is a [[smooth space]], then we may additionally identify paths related through a [[thin homotopy]] to get the __[[path groupoid]]__.  Finally, if $X$ is a [[continuous space]] and we identify paths related through any (endpoint-preserving) [[homotopy]], then we get the __[[fundamental groupoid]]__ of $X$.

In graph theory, the Moore path category is known as the __[[free category]]__ on the graph.

## References

{#tomDieck2008} [[Tammo tom Dieck]], _Algebraic Topology_, European Mathematical Society, 2008


## Related entries

* [[path-connected topological space]]

* [[locally path-connected topological space]]

* [[loop]]

* [[path space]],

* [[fundamental group]], [[fundamental groupoid]]

* [[fundamental theorem of covering spaces]]




[[!redirects path]]
[[!redirects paths]]

[[!redirects Moore path]]
[[!redirects Moore paths]]

[[!redirects path concatenation]]
[[!redirects path concatenations]]

[[!redirects concatenation of paths]]
[[!redirects concatenrations of paths]]


[[!redirects reverse path]]
[[!redirects reverse paths]]

[[!redirects path reversal]]
[[!redirects path reversion]]
[[!redirects path reversals]]
[[!redirects path reversions]]

[[!redirects constant path]]
[[!redirects constant paths]]
