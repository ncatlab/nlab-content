
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _cellular simplex_ is one of the basic [[geometric shapes for higher structures]]. Variants of the same "shape archetype" exist in several settings, e.g., that of a [[simplicial set]], the topological /cellular one, and categorical contexts, plus others.

## Definitions
 {#Definition}

### Simplicial simplices
 {#SimplicialSimplex}

For $n \in \mathbb{N}$, the standard _simplicial $n$-simplex_ $\Delta[n]$ is the [[simplicial set]] which is represented (as a [[presheaf]]) by the object $[n]$ in the [[simplex category]], so $\Delta[n]= \Delta(-,[n])$.


### Cellular (simplicial) simplex
 {#CellularSimplex}

Likewise, there is a standard topological $n$-simplex, which is (more or less by definition) the [[geometric realization]] of the standard simplicial $n$-simplex.

### Topological simplex
 {#TopologicalSimplex}

The _topological $n$-simplex_ $\Delta^n$ is a generalization of the standard filled _[[triangle]]_ in the plane, from [[dimension]] 2 to arbitrary dimensions. Each $\Delta^n$ is [[homeomorphism|homeomorphic]] to the closed $n$-[[ball]] $D^n$, but its defining [[embedding]] into a [[Cartesian space]] equips its [[boundary]] with its cellular decomposition into _[[faces]]_, generalizing the way that the triangle has three [[edges]] (which are 1-simplices) as [[faces]], and three points (which are [[vertices]] or 0-simplices) as corners.

The topological $n$-simplex is naturally defined as a [[subspace]] of a
[[Cartesian space]] given by some relation on its canonical 
[[coordinates]]. There are two standard choices for such coordinate
presentation, which of course define [[homeomorphism|homeomorphic]]
$n$-simplices:

* [Barycentric coordinates](#BarycentricCoordinates)

* [Cartesian coordinates](#CartesianCoordinates)

Each of these has its advantages and disadvantages, depending on application, but of course there is a simple coordinate transformation that exhibits an explicit [[homeomorphism]] between the two:

* [Transformation between Barycentric and Cartesian coordinates](#CoordinateTransformation).


#### Barycentric coordinates
 {#BarycentricCoordinates}


In the following, for $n \in \mathbb{N}$ we regard the [[Cartesian space]] $\mathbb{R}^n$ as equipped with the canonical [[coordinates]] labeled $x_0, x_1, \cdots, x_{n-1}$.

+-- {: .num_defn #TopologicalInBarycentricCoords}
###### Definition

For $n \in \mathbb{N}$, the **topological $n$-simplex** is, 
up to [[homeomorphism]], the [[topological space]] whose underlying set is
the [[subset]]

$$
  \Delta^n 
    \;\coloneqq\; 
  \Big\{
    \vec x \in (\mathbb{R}_{\geq 0})^{n+1}
    \,\big|\,
    \textstyle{\sum}_{i = 0 }^n x^i = 1 
  \Big\}
  \;\subset\; 
  \mathbb{R}^{n+1}
$$

of the [[Cartesian space]] $\mathbb{R}^{n+1}$, and whose [[topological space|topology]] is the  [[subspace topology]] inherited from the [[Euclidean topology]] on $\mathbb{R}^{n+1}$.

=--

\linebreak
\linebreak

\[\label{IllustrationOfBarycentricTopologicalSimplices}\]
\begin{imagefromfile}
    "file_name": "TopologicalSimplices.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -100,
        "bottom": 20,
        "right": 0, 
        "left": 0
    }
\end{imagefromfile}





+-- {: .num_defn #FaceInclusionInBarycentricCoords}
###### Definition

For $n \in \mathbb{N}$, $\n \geq 1$ and $0 \leq k \leq n$, the 
**$k$th $(n-1)$-face (inclusion)**  of the topological $n$-simplex is the subspace inclusion

$$
  \delta_k : \Delta^{n-1} \hookrightarrow \Delta^n
$$

induced under the barycentric coordinates of def. \ref{TopologicalInBarycentricCoords},
by the inclusion 

$$
  \mathbb{R}^n \hookrightarrow \mathbb{R}^{n+1}
$$

which omits the $k$th coordinate

$$
  (x_0, \cdots , x_{n-1}) \mapsto (x_0, \cdots, x_{k-1} , 0 , x_{k}, \cdots, x_{n-1})
  \,.
$$

=--

+-- {: .num_example}
###### Example

The inclusion 

$$
  \delta_0 : \Delta^0 \to \Delta^1
$$ 

is the inclusion

$$
  \{1\} \hookrightarrow [0,1]
$$ 

of the "right" end of the standard interval. The other inclusion 

$$
  \delta_1 : \Delta^0 \to \Delta^1
$$ 

is that of the "left" end $\{0\} \hookrightarrow [0,1]$.

=--

+-- {: .num_defn #DegeneracyProjectionsInBarycentricCoords}
###### Definition

For $n \in \mathbb{N}$ and $0 \leq k \lt n$ the **$k$th degenerate $n$-simplex (projection)** is the surjective map

$$
  \sigma_k : \Delta^{n} \to \Delta^{n-1}
$$

induced under the barycentric coordinates of def. \ref{TopologicalInBarycentricCoords} under the surjection

$$
  \mathbb{R}^{n+1} \to \mathbb{R}^n
$$

which sends

$$
  (x_0, \cdots, x_n) \mapsto (x_0, \cdots, x_{k} + x_{k+1}, \cdots, x_n)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The collection of face inclusions, def. \ref{FaceInclusionInBarycentricCoords}
and degeneracy projections, def. \ref{DegeneracyProjectionsInBarycentricCoords}
satisfy the (dual) [[simplicial identities]]. Equivalently, they constitute the components of a [[functor]]

$$
  \Delta^\bullet : \Delta \to Top
$$

from the [[simplex category]] $\Delta$ to the category [[Top]] of [[topological spaces]]. This is, up to [[isomorphism]], the standard [[cosimplicial object]] in $Top$.

=--

#### Cartesian coordinates
 {#CartesianCoordinates}

+-- {: .num_defn #TopologicalInCartesianCoordinates}
###### Definition

The standard **topological $n$-simplex** is, up to [[homeomorphism]], 
the [[subset]]

$$
  \Delta^n 
  \coloneqq
  \{
     \vec x \in \mathbb{R}^n | 0 \leq x_1 \leq \cdots \leq x_n \leq 1
  \}
  \hookrightarrow \mathbb{R}^n 
$$

equipped with the [[subspace topology]] of the standard topology on the [[Cartesian space]] $\mathbb{R}^n$.

=--

+-- {: .num_remark }
###### Remark

This definition identifies the topological $n$-simplex with the space of [[interval]] maps (preserving top and bottom) $\{0 \lt 1 \lt \ldots \lt n+1\} \to I$ into the topological interval. This point of view takes advantage of the [duality](http://ncatlab.org/nlab/show/simplex+category#duality_with_intervals_23) between the [[simplex category]] $\Delta$ and the category $\nabla$ of finite [[intervals]] with distinct top and bottom. Indeed, it follows from the duality that we obtain a functor 

$$\Delta \simeq \nabla^{op} \stackrel{Int(-, I)}{\to} Top.$$ 

=--


+-- {: .num_example}
###### Example

* For $n = 0$ this is the [[point]], $\Delta^0 = *$.

* For $n = 1$ this is the standard [[interval object]] $\Delta^1 = [0,1]$.

* For $n = 2$ this is a triangle sitting in the plane like this:

  $$
    \left\{
      (x_0,x_1) | 0 \leq x_0 \leq x_1 \leq 1
    \right\}
    = 
    \left\{
    \array{
       && && (1,1)
       \\
       && & \nearrow & \downarrow
       \\
       && (\tfrac{1}{2}, \tfrac{1}{2}) && (\tfrac{1}{2},1)
       \\
       & \nearrow & && \downarrow
       \\
       (0,0) &\stackrel{}{\to}& (0,\tfrac{1}{2}) & \to & (0,1)
    }
    \right\}
  $$


=--


#### Transformation between Barycentric and Cartesian coordinates
 {#CoordinateTransformation}

For $n \in \mathbb{N}$,  write now explicitly 

$$
 \Delta^n_{bar} \hookrightarrow \mathbb{R}^{n+1}
$$

for the topological $n$-simplex in barycentric coordinate presentation, def. \ref{TopologicalInBarycentricCoords}, and 

$$
 \Delta^n_{cart} \hookrightarrow \mathbb{R}^{n}
$$

for the topological $n$-simplex in Cartesian coordinate presentation, def. \ref{TopologicalInCartesianCoordinates}.  

Write

$$
  S_n : \mathbb{R}^{n+1} \to \mathbb{R}^n
$$

for the [[continuous function]] given in the standard coordinates by

$$
  (x_0, \cdots, x_{n})
  \mapsto
  (x_0, x_0 + x_1, \cdots, \sum_{i = 0}^k x_i, \cdots, \sum_{i = 0}^{n-1} x_i)
  \,.
$$

By restriction, this induces a continuous function on the topological $n$-simplices

$$
  \array{
     \Delta^n_{bar} &\hookrightarrow& \mathbb{R}^{n+1}
     \\
     \downarrow^{\mathrlap{S_n|_{\Delta^n_{bar}}}} && \downarrow^{p_n}
     \\
     \Delta^n_{cart} &\hookrightarrow& \mathbb{R}^n
  }
  \,.
$$

+-- {: .num_prop}
###### Proposition

For every $n \in \mathbb{N}$ the function $S_n$ is a [[homeomorphism]]
and respects the face and degeneracy maps.

Equivalently, $S_\bullet$ is a [[natural isomorphism]] of [[functors]] 
$\Delta^n \to Top$, hence an [[isomorphism]] of [[cosimplicial objects]]

$$
  S_\bullet : \Delta^\bullet_{bar} \stackrel{\simeq}{\to} \Delta^\bullet_{cart}
  \,.
$$

=--

### Singular simplex
 {#SingularSimplex}

+-- {: .num_defn}
###### Definition

For $X \in $ [[nLab:Top]]  and $n \in \mathbb{N}$, a **singular $n$-simplex** in $X$ is a [[nLab:continuous map]]

$$
  \sigma : \Delta^n \to X
  \,.
$$

Write 

$$
  (Sing X)_n \coloneqq Hom_{Top}(\Delta^n , X)
$$ 

for the set of singular $n$-simplices of $X$.

=--

As $n$ varies, this forms the [[singular simplicial complex]] of $X$.

## Properties

### Relation to globes

The [[orientals]] relate simplices to [[globes]].

## Related concepts


* [[vertex]], [[edge]]

* [[triangle]], [[tetrahedron]]

* [[horn]], [[boundary of a simplex]], [[spine]]

* [[differential forms on simplices]]

* [[simplicial set]]

  * [[simplicial complex]]

  * [[Kan complex]]
 
  * [[weak Kan complex]]

* [[simplicial category]]

* [[globe]], 

* [[tree]], [[dendrex]]

* [[Bloch region]]

* [[Delta-generated space]]

## References

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Exp. 1.7 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) &lbrack;[doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/)&rbrack;




[[!redirects simplices]]

[[!redirects simplicial simplex]]
[[!redirects cellular simplex]]
[[!redirects topological simplex]]

[[!redirects simplicial simplices]]
[[!redirects cellular simplices]]
[[!redirects topological simplices]]

[[!redirects singular simplex]]
[[!redirects singular simplices]]

[[!redirects k-simplex]]
[[!redirects k-simplices]]

[[!redirects 0-simplex]]
[[!redirects 0-simplices]]

[[!redirects 1-simplex]]
[[!redirects 1-simplices]]

[[!redirects 2-simplex]]
[[!redirects 2-simplices]]

[[!redirects 3-simplex]]
[[!redirects 3-simplices]]

[[!redirects n-simplex]]
[[!redirects n-simplices]]

[[!redirects topological n-simplex]]
[[!redirects topological n-simplices]]

[[!redirects topological k-simplex]]
[[!redirects topological k-simplices]]


[[!redirects geometric n-simplex]]
[[!redirects geometric n-simplices]]



