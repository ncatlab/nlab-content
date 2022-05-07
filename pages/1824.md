
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A microbundle is something like an approximation to the notion of [[vector bundle]]: a locally trivial [[bundle]] $E \to X$ of topological spaces that has a [[section]]. Indeed, as observed by Milnor,  every vector bundle gives an example of a microbundle (for a modern treatment see [Kupers18, Example 27.2.3](#Kupers18) or Lurie's course, [Topics in Geometric Topology, Lecture 10](http://www.math.harvard.edu/~lurie/937notes/937Lecture10.pdf)).

## Definition

### Microbundles

A real __microbundle of dimension $n$__ is a 4-tuple $\xi = (E,p,B,i)$ where 

* $E$ is a [[topological space]] (the _total space_ of $\xi$),

* $B$ is a topological space (the _base space_ of $\xi$, 

* and $p:E\to B$ a continuous map (projection), 

* $i:B\hookrightarrow E$ another continuous map (inclusion of base space) 

such that

* $i$ is a [[section]] of $p$, i.e. $p\circ i = id_B$ 

* the _local triviality_ condition holds: 

  for all $b\in B$, there are neighborhoods $U\ni b$ and $V\ni i(b)$ and a homeomorphism $h:U\times R^n\to V\cap p^{-1}(U)$ such that $p(h(u,v))=u$ and $h(u,0)=i(u)$ for all $u\in U$. The open subspace $i(B)$ is called the _zero section_ of $\xi$. 

### Morphisms of microbundles

A __[[morphism]] of microbundles__ $\phi:\xi\to\xi'$ is a [[germ]] of maps from neighborhoods of the zero section of $\xi$ to $\xi'$, which commutes with projections and inclusions, with composition defined for representatives as composition of functions on smaller neighborhoods. 

In particular, an __[[isomorphism]] of microbundles__ can be represented by a [[homeomorphism]] from a neighborhood $V$ of the zero section in $\xi$ to a neighborhood $V'$ of the zero section in $\xi'$ commuting with projections and inclusions of the zero sections. 


## Examples

### Tangent microbundle

The main example is the __tangent microbundle__ $(M\times M,p_1,M,i)$ of a topological [[manifold]] $M$ where $p_1:M\times M\to M$ is the projection onto the first factor. If $(U,f)$ is a chart of the manifold $M$ around point $x\in M$ (where $x\in U\subset M$ and $f:U\to R^n$ is a homeomorphism with $h(x)=0$) then define $h:U\times R^n\to U\times U$ by $h(u,v)=(u,f^{-1}(f(v)-u))$. 

If $M$ is a smooth manifold, then the tangent microbundle is equivalent to the tangent bundle ([Kupers18, Example 27.2.3](#Kupers18)). 

## References

The original reference is

* [[John Milnor]], _Microbundles.  Part I_, Topology 3 (1964), Supplement 1, 53–80. doi: https://doi.org/10.1016/0040-9383(64)90005-9, [PDF](http://www.maths.ed.ac.uk/~aar/papers/micro001.pdf).

Classic treatments of their elementary theory include:

* [[N. H. Kuiper]] and [[Richard Lashof|R. K. Lashof]], _Microbundles and Bundles I. Elementary Theory_, Invent. Math., 1, (1966), 1 – 17. 

* [[N. H. Kuiper]] and [[Richard Lashof|R. K. Lashof]], _Microbundles and Bundles II. Semisimplicial Theory_, Invent. Math., 1, (1966), 243 – 259.

Useful references are for instance

* [[Jacob Lurie]], Spring 2009, [Topics in Geometric Topology](http://www.math.harvard.edu/~lurie/937.html)

* S. Buoncristiano, 2003, [Fragments of geometric topology from the sixties](http://www.emis.de/journals/GT/gtmcontents6.html).

* {#Kupers18} [[Alexander Kupers]], _Lectures on diffeomorphisms groups of manifolds_, ([pdf](http://www.math.harvard.edu/~kupers/teaching/272x/book.pdf))


[[!redirects tangent microbundle]]
[[!redirects tangent microbundles]]
[[!redirects microbundles]]