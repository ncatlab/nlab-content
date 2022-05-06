

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[compactification]] of [[configuration spaces of points]] was introduced in [Axelrod-Singer 93, p. 5-6](#AxelrodSinger93), [Fulton-MacPherson 94](#FultonMacPherson94) and an [[operad]]-[[structure]] defined on it by [Getzler-Jones 94](#GetzlerJones94) [Kontsevich 97](#Kontsevich97), now called the _Fulton-MacPherson operad_, [[weak equivalence|weakly equivalent]] to the [[little n-disk operad]] ([Salvatore 01, Prop. 4.9](#Salvatore01)), hence a model for an [[En-operad]]. 

The [[de Rham cohomology]] as well as the [[de Rham complex]] itself of the Fulton-MacPherson operad it [[quasi-isomorphism|quasi-isomorphic]] to [[graph complexes]] via [[TQFT|topological]] [[Feynman amplitudes]] (see [below](#RelationToGraphComplexes)), in fact it is the [[perturbative quantum field theory|perturbative]] computation of [[Feynman amplitudes]] in [[Chern-Simons theory]] that motivated the compactified configuration space, this way, in [Axelrod-Singer 91](#AxelrodSinger91), [Axelrod-Singer 93](#AxelrodSinger93). These two [[quasi-isomorphism]] serve to exhibit [[formal dg-algebra|formality]] of the Fulton-MacPherson operad, and hence also [[formality of the little n-disk operad]].

To see the nature of the Axelrod-Singer-Fulton-MacPherson compactification of [[configuration spaces of points]], observe that the [[configuration space of points|configuration space]] of exactly 2 points in a [[Cartesian space]]/[[Euclidean space]] $\mathbb{R}^d$ is [[homotopy equivalence]] to the [[quotient]] by [[group of order two|Z/2]] of a [[n-sphere|(d-1)-sphere]]

$$
  Conf_2( \mathbb{R}^d )
  \;\simeq\;
  S^{d-1}/(\mathbb{Z}/2)
$$

this being the sphere of [[direction of a vector|directions]] of the [[vector]] pointing from one of the two points to the other. This means that the configuration space $Conf_n( \mathbb{R} )$ of $n$ points is [[homotopy equivalent]] to a [[quotient]] by the [[symmetric group]] $\Sigma(n)$ of the [[Cartesian product]] of one such [[n-sphere|(d-1)-sphere]] of [[direction of a vector|directions]] for each [[pair]] of points and various [[open intervals]] encoding the relative [[distance]] between the points.

The _Fulton-MacPherson compactification_ is the evident [[compactification]] of this [[quotient space|quotient]] of [[Cartesian products]] of [[n-sphere|(d-1)-spheres]] with [[open intervals]], replacing the latter by their corresponding [[closed intervals]]. 

This means that a point on the [[boundary]] of the Fulton-MacPherson compactification corresponds to a would-be [[configuration space of points|configuration]] of points where some of the points have formally vanishing [[distance]] to each other, while still remembering a relative [[direction of a vector|direction]] to each other.

More abstractly one may sum this up succinctly by saying that the ASFM-compactification is the  [[blowup]] of the [[fat diagonal]] inside the [[Cartesian products]] of the base space with itself. 

In the literature these [[boundary]] configurations are often referred to in terms of "infinitesimally close points". While there may be some formal relation to actual [[infinitesimal neighbourhoods]] in (for example) [[synthetic differential geometry]], we point out the Axelrod-Singer-Fulton-MacPherson compactifications as defined below are plain [[topological spaces]] or manifolds with corners (in some suitable sense), not [[objects]] in a [[smooth topos]] in any of the usual senses. 

## Definition

For $n, d \in \mathbb{N}$, consider first the [[topological space]] of configurations of _ordered_ [[n-tuples]] of points in the [[Cartesian space]]/[[Euclidean space]] $\mathbb{R}^d$, hence the [[mapping space]] of [[injections]]/[[embeddings of topological spaces]]

$$
  Emb( \{1, \cdots, n\}, \mathbb{R}^d )
  \;\subset\;
  \left( 
    \mathbb{R}^d
  \right)^n
  \,.
$$

The [[group]] of [[translation group|translations]] and of [[scale transformations]] [[action|acts]] canonically on $\mathbb{R}^d$ and hence [[diagonal action|diagonally]] on $Emb( \{1, \cdots, n\}, \mathbb{R}^d )$. The resulting [[quotient topological space]]

$$
  Emb( \{1, \cdots, n\}, \mathbb{R}^d )
  \longrightarrow
  Emb( \{1, \cdots, n\}, \mathbb{R}^d )/ \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}
$$

is clearly [[homotopy equivalence|homotopy equivalent]] to the original space.

But now for $n \geq 2$ this quotient space canonically carries the structure of a [[topological manifold]] (in fact of a [[smooth manifold]]) of [[dimension of a manifold|dimension]]

$$
  dim
  \left(
    Emb\left( \{1, \cdots, n\}, \mathbb{R}^d \right)/\left( \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}\right)
  \right)
  \;=\;
  n \cdot d - d - 1
$$

while for $n \leq 1$ the quotient is the [[point space]] (of [[dimension of a manifold|dimension]] 0).

Now for a [[pair]] $i \neq j \in \{1, \cdots, n\}$ of distinct indices, consider the [[continuous function]]

\[
  \label{ProjectionsToBoundarySpheres}
  \array{
    Emb\left( \{1, \cdots, n\}, \mathbb{R}^d \right)/\left( \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}right)
  \right)
    &\overset{\theta_{i j}}{\longrightarrow}&
    S^{d-1} \subset \mathbb{R}^d
    \\
    (x_1, \cdots, x_n)
    &\mapsto&
    \frac{
      x_j - x_i
    }{
      {\vert x_j - x_i\vert}
    }
  }
\]

which takes each configuration to the [[direction]] of the [[vector]] between the $i$th and the $j$th point in the configuration.

Moreover, for each [[triple]] $i,j,k$ of mutually distinct indices, consider the [[continuous function]]

$$
  \array{
    Emb\left( \{1, \cdots, n\}, \mathbb{R}^d \right)/\left( \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}\right)
    &\overset{\delta_{i j k}}{\longrightarrow}&
    (0,\infty) \subset [0,\infty]
    \\
    (x_1, \cdots, x_n)
    &\mapsto&
    \frac{ {\vert x_i - x_j\vert} }{ {\vert  x_j - x_k \vert} }
  }
$$

which takes each configuration to the [[ratio]] of the [[distance]] between the $i$th and the $j$th point over that of the $j$th to the $k$th point.

Together these functions induce one total [[continuous function]]

\[
  \label{EmbeddingOfTheOrderedConfigurationSpace}
  \iota
  \;\colon\;
  Emb\left( \{1, \cdots, n\}, \mathbb{R}^d \right)/\left( \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}\right)
  \overset{ (\theta_{i j}, \delta_{i j k}) }{\hookrightarrow}
  \left( S^{d-1} \right)^{ n(n-1) }
  \times [0,\infty]^{ \left(  n(n-1)(n-2) \right) }
\]

from the ordered configuration space into the [[Cartesian product]] of all these [[n-sphere|(d-1)-spheres]] and [[intervals]]. 

A moment of reflection shows that every ordered configuration modulo translation and rescaling, hence every point on the left, may be uniquely reconstructed from its direction vectors and distance ratios, hence from a point on the right, hence that this function is a [[homeomorphism]] onto its [[image]] ([Sinha 03, lemma 3.18](#Sinha03)).

+-- {: .num_defn #FultonMacPhersonCompactification}
###### Definition
**(Fulton-MacPherson compactification)**

The _Fultan-MacPherson compactification_ of the [[configuration space of points|configuration space]] of ordered [[n-tuples]] of points in the [[Cartesian space]]/[[Euclidean space]] $\mathbb{R}^d$ is the [[topological closure]] of the [[image]] of (eq:EmbeddingOfTheOrderedConfigurationSpace):

$$
  FM_n(\mathbb{R}^d)
  \;\coloneqq\;
  \overline{ \iota\left( 
      Emb\left( \{1, \cdots, n\}, \mathbb{R}^d \right)/\left( \mathbb{R}^d \rtimes \mathbb{R}_{\gt 0}\right)
  \right) }
$$

=--

(e.g. [Lambrechts-Volic 14, Def. 5.1](#LambrechtsVolic14))

The [[symmetric group]] $\Sigma(n)$ still canonically [[action|acts]] on $FM_n(\mathbb{R}^d)$ and hence the FM-compactification of the actual [[configuration space of points]] $Conf_n(\mathbb{R}^d)$ is the [[quotient space]] 

$$
  \overline{Conf_n(\mathbb{R}^d)} 
  \;=\; 
  FM_n(\mathbb{R}^d)/\Sigma(n)
  \,.
$$

## Pictorial notation
 {#Pictorial}

By the above, the points on the [[boundary]] of a Fulton-MacPherson compactification of [[configuration spaces of points]] (Def. \ref{FultonMacPhersonCompactification}) correspond to configurations that involve [[triples]] of points in space $x,y,z$, such that the [[distance]] between two of them is "vanishing in ratio to the distance of both to the third".

Hence where a configuration of two points in space looks like

<center>
<img src="https://ncatlab.org/nlab/files/FultonMacPherson1.jpg" width="300"/>
</center>

a configuration of such a boundary case of three points may be visualized as

<center>
<img src="https://ncatlab.org/nlab/files/FultonMacPherson2.jpg" width="400"/>
</center>

where the "funnel" might be thought of as an infinite magnifying glass held to the location of the second point and revealing that it really consists of two points of vanishing distance to each other, relative to their joint distance to the remaining point.

In this fashion, for instance a boundary point in the Fulton-MacPherson compactification depicted as follows 

<center>
<img src="https://ncatlab.org/nlab/files/FultonMacPherson3.jpg" width="400"/>
</center>

would consist of 

* points 3, 4 and 5  being arbitrarily close to each other with respect to their distance to points 1, 2 and 6

* points 3 and 5 also being arbitrarily close to each other with respect to their joint distance to 4

* points 1, 2 and 6 being arbitrarily close to each other in comparison to their joint distances to 3, 4 and 5

* points 1 and 2 also being arbitrarily close to each other with respect to their joint distance to 6.

> graphics grabbed from [Lambrechts-Volic 14, Figures 3 and 4](#LambrechtsVolic14)

This pictorial notation was introduced in [Sinha 03](#Sinha03). It immediately suggests the correct [[operad]]-[[structure]] on the Fulton-MacPherson compactifications.

## Properties

### Relation to the little $n$-disk operad

+-- {: .num_prop #WeakEquivalenceToLittleNDiskOperad}
###### Proposition

The Fulton-MacPherson operad $FM_\bullet\left( \mathbb{R}^d\right)$ is [[weak equivalence|weakly equivalent]] in the [[model structure on operads]] with respect to the [[classical model structure on topological spaces]], to the [[little n-disk operad|little d-disk operad]].

=--

([Salvatore 01, Prop. 4.9](#Salvatore01), summarized as [Lambrechts-Volic 14, Prop. 5.6](#LambrechtsVolic14))

### de Rham cohomology
  {#deRhamCohomology}

We discuss the [[de Rham complex]] $\Omega^\bullet(FM_n(\mathbb{R}^d))$ and the [[de Rham cohomology]] $H^\bullet_{dR}( FM_n(\mathbb{R}^d) )$ of Fulton-MacPherson compactifications.

+-- {: .num_defn #SphereClassGeneratorsOfDeRhamCohomology}
###### Definition

Let $d \in \mathbb{N}$ ([[dimension of a manifold|dimension]] of [[Euclidean space]]),  and $n \in \mathbb{N}$ (number of points) and consider the Fulton-MacPherson compactification $FM_n(\mathbb{R}^d)$ from Def. \ref{FultonMacPhersonCompactification}.

Let

$$
  dvol_{\left(S^{d-1}\right)}
  \;\in\;
  \Omega^\bullet\left( S^{d-1} \right)
$$

be the standard [[volume form]] on the standard [[n-sphere|d-sphere]].

For $i \neq j \in \{1, \cdots, n\} $ two distinct point labels, write

$$
  g_{i j}
  \;\coloneqq\;
  \left(\theta_{i j}\right)^\ast\left( dvol_{\left( S^{d-1}\right)}\right)
  \;\in\;
  \Omega^\bullet\left( FM_n\left(\mathbb{R}^d\right) \right)
$$

be the [[pullback of differential forms]] of this standard volume form along the [[projection]] $\theta_{i j} \;\colon\; FM_n\left( \mathbb{R}^{d}\right) \longrightarrow S^{d-1}$ from (eq:ProjectionsToBoundarySpheres).

=--

+-- {: .num_prop #DeRhamCohomologyOfFMCompactification}
###### Proposition

Let $d \in \mathbb{N}$ ([[dimension of a manifold|dimension]] of [[Euclidean space]]),  and $n \in \mathbb{N}$ (number of points) and consider the Fulton-MacPherson compactification $FM_n(\mathbb{R}^d)$ from Def. \ref{FultonMacPhersonCompactification}.


The [[de Rham cohomology]] of $FM_n\left( \mathbb{R}^d\right)$ is, as a [[graded-commutative algebras]], [[isomorphism|isomorphic]] to the [[quotient algebra]] of the [[free construction|free]] [[graded commutative algebra]] [[generators and relations|generated]] by the classes of the forms $g_{i j}$ from Def. \ref{SphereClassGeneratorsOfDeRhamCohomology} 

$$
  H^\bullet_{dR}\left(
    FM_n\left( \mathbb{R}^d \right)
  \right)
  \;\simeq\;
  \wedge_{\mathbb{R}}^\bullet
  \left\langle
    \left[g_{i j}\right] \;\vert\; i \neq j \in \{1, \cdots, n\}
  \right\rangle / \sim
$$

by the following three relations (for all distinct $i,j,k \in \{1,\cdots, n\}$):

1. $\left[g_{i j}\right] \wedge \left[g_{i j}\right] \;\sim\; 0$;

1. $\left[g_{i j}\right] \;\sim\; (-1)^d \left[g_{j i}\right]$;

1.  $
     \left[g_{i j}\right] \wedge \left[ g_{j k} \right]
     +
     \left[g_{j k}\right] \wedge \left[ g_{k i} \right]
     +
     \left[g_{k i}\right] \wedge \left[ g_{i j} \right]
     \;\sim\;
     0
   $ $\;\;\;\;$("3-term relation")

=--

This is due to ([Cohen 73](#Cohen73)). 


### Relation to Graph complexes and Formality theorem
 {#RelationToGraphComplexes}

We have that [[the Fulton-MacPherson operad is formal]] in the sense that for each of its component [[manifolds]] $FM_n\left( \mathbb{R}^d\right)$ (Def. \ref{FultonMacPhersonCompactification}) there is a [[zig-zag]] of [[quasi-isomorphisms]] between their [[de Rham cohomology]] and their [[de Rham complex]], and such that these morphisms are compatible with the induced [[cooperad]]-[[structure]] on both sides.

Concretely, the [[zig-zags]] may be taken to consist of one [[span]] of [[quasi-isomorphisms]] out of a suitable [[graph complex]] to the [[de Rham cohomology]]/[[de Rham complex]] of the [[Fulton-MacPherson operad]].

Here the morphism from the [[graph complex]] to the [[de Rham complex]] of the [[Fulton-MacPherson operad]] regards the latter as the [[compactification]] of a [[configuration space of points]], regards [[functions]]/[[differential forms]] on [[configuration spaces of points]] as [[n-point functions]] of a [[topological quantum field theory|topological]] [[quantum field theory]], regards suitable [[graphs]] as [[Feynman diagrams]] and proceeds by sending each such graph/Feynman diagram to a corresponding [[Feynman amplitude]].

This idea of a proof was sketched in [Kontsevich 99](#Kontsevich99), a full account is due to [Lambrechts-Volic 14](#LambrechtsVolic14).

+-- {: .num_defn #TheGraphComplexdgcAlgebra}
###### Definition
**(the [[graph complex]])**

For $n\in \mathbb{N}$, write 

$$
  Graphs_n\left( \mathbb{R}^d \right)
  \;\in\;
  dgcAlg_{\mathbb{R}}
$$ 

for the [[graph complex]] of "[[Feynman graphs]]" with $n$ external [[vertices]], regarded with its [[structure]] of a [[differential graded-commutative algebra]] over the [[real numbers]].

=--

([Lambrechts-Volic 14, Def. 6.19](#LambrechtsVolic14))

+-- {: .num_prop  #QuasiIsoFromGraphComplexToDeRhamCohomology}
###### Proposition

The [[linear function]]

$$
  \overline{I}
  \;\colon\;
  Graphs_n\left( \mathbb{R}^d\right)
  \overset{ \phantom{AA}\simeq \phantom{AA} }{\longrightarrow}
  H^\bullet_{dR}\left(  FM_n\left( \mathbb{R}^d \right) \right)
$$

from the [[graph complex]] [[dgc-algebra]] (Def. \ref{TheGraphComplexdgcAlgebra}) to the [[de Rham cohomology]] (Prop. \ref{DeRhamCohomologyOfFMCompactification}) of the Fulton-MacPherson compactification (Def. \ref{FultonMacPhersonCompactification}) given on generators by

$$
  \overline{I}\left( \Gamma \right)
  \;=\;
  \left\{
    \array{
      \left[g_{i j}\right] &\vert& \Gamma \, {\text{is diagram without internal vertices} \atop \text{and single edge between external vertices}\, i \, \text{and}\, j}
      \\
      0 &\vert& \Gamma \, \text{has internal vertices}
    }
  \right.
$$

(where $g_{i j} \in \Omega^\bullet\left(  FM_n\left( \mathbb{R}^d\right) \right)$ are the [[differential forms]] from Def. \ref{SphereClassGeneratorsOfDeRhamCohomology})

extends to a [[homomorphism]] of [[dgc-algebras]] which is a [[quasi-isomorphism]].

=--

([Lambrechts-Volic 14, Theorem 8.1](#LambrechtsVolic14))

+-- {: .num_example #ThreeTermRelation}
###### Example
**(the "3-term relation")**

In the [[graph complex]] the [[differential]] of the [[graph]] as shown on the left below (the vertices on the horizontal line are the external vertices, that above the line is internal) is a linear combination as shown on the right:

$\phantom{AAA}\array{ \partial \\ \phantom{A} \\ \phantom{a}}$
<img src="https://ncatlab.org/nlab/files/TrivializationOfThreeTermIdentity.jpg" width="100">
$\phantom{A}\array{ = \\ \phantom{A} \\ \phantom{a} }\phantom{A}$
<img src="https://ncatlab.org/nlab/files/ThreeTermIdentity.jpg" width="300">

> graphics grabbed from [Lambrechts-Volic 14, Figure 1 & Figure 2](#LambrechtsVolic14)

Under the above [[quasi-isomorphism]] (Prop. \ref{QuasiIsoFromGraphComplexToDeRhamCohomology}) from the [[graph complex]] to the [[de Rham complex]] on the [[Fulton-MacPherson compactification]] of a [[configuration space of points]] given by sending each [[graph]] to its [[Chern-Simons propagator|Chern-Simons]] [[Feynman amplitude on compactified configuration spaces of points]] (Remark \ref{AsPerturbativeChernSimonsTheory}) this relation becomes the "3-term relation" from Prop. \ref{DeRhamCohomologyOfFMCompactification}

$$
     \left[g_{i j}\right] \wedge \left[ g_{j k} \right]
     +
     \left[g_{j k}\right] \wedge \left[ g_{k i} \right]
     +
     \left[g_{k i}\right] \wedge \left[ g_{i j} \right]
     \;\sim\;
     0
$$

satisfied by the [[Chern-Simons propagator]] form

$$
  \left(
    g_{i j}
    \;\in\;
    \Omega^2\left( FM_n(\mathbb{R}^d)  \right)
  \right)
  \,.
$$


=--


Now we consider the analogous but richer quasi-isomorphism from the [[graph complex]] not just to the [[de Rham cohomology]] of the compactified configuration space, but its full [[de Rham complex]].

+-- {: .num_defn #FiberIntegrationOverInternalVertices}
###### Definition
**([[fiber integration]] over internal [[vertices]])**

For $\Gamma \in Graphs_n\left( \mathbb{R}^d \right)$ an element in the [[graph complex]] (Def. \ref{TheGraphComplexdgcAlgebra}) with $k$ internal vertices, write

$$
  \array{
    FM_{n + k}\left( \mathbb{R}^d \right)
    \\
    \Big\downarrow {}^{\mathrlap{\pi_n^{n + k}}}
    \\
    FM_{n}\left( \mathbb{R}^d\right)
  }
$$

for the evident [[continuous function]] between the Fulton-MacPherson compactifications of ordered [[configuration spaces of points]] (Def. \ref{FultonMacPhersonCompactification}) obtained by forgetting the $k$ "internal" of the total of $n + k$ points in a configuration.

This canonically carries the [[structure]] of a [[fiber bundle]] of [[semi-algebraic manifolds]] and hence induces a [[fiber integration|fiber-]] [[integration of differential forms]] from minimal to partially algebraic differential forms:

$$
  \underset{ 
    \pi_n^{n + k}
  }{\int}
  \;\colon\;
  \Omega^\bullet_{min}
  \left(
    FM_{n + k}\left( \mathbb{R}^d \right)
  \right)
  \longrightarrow
  \Omega^{\bullet - d \cdot k}_{PA}
  \left(
    FM_n\left( \mathbb{R}^d \right)
  \right)
$$

=--

([Lambrechts-Volic 14, Theorem 5.8 and equation (111)](#LambrechtsVolic14))



+-- {: .num_prop #QuasiIsomorphismBetweenGraphComplexAndDeRhamComplexOfFM}
###### Proposition
**([[quasi-isomorphism]] between [[graph complex]] and [[de Rham complex]] of Fulton-MacPherson compactification)**

Consider the [[linear function]]

$$
  \overline{I}
  \;\colon\;
  Graphs_n\left( \mathbb{R}^d\right)
  \overset{ \phantom{AA}\simeq \phantom{AA} }{\longrightarrow}
  \Omega^\bullet_{PA}\left(  FM_n\left( \mathbb{R}^d \right) \right)
$$

from the [[graph complex]] [[dgc-algebra]] (Def. \ref{TheGraphComplexdgcAlgebra}) to the [[semialgebraic de Rham complex]] (Def. \ref{FiberIntegrationOverInternalVertices}) of the Fulton-MacPherson compactification (Def. \ref{FultonMacPhersonCompactification}) given on [[graphs]] 

$$
  \Gamma \;\in\; Graphs_{n}\left( \mathbb{R}^d\right)
$$

with 

$$
  k \coloneqq int(\Gamma)
$$

internal vertices by the [[integral transform]] of the canonical [[volume form]] through the [[span]]

$$
  \array{
    && 
    FM_{n + k}\left( \mathbb{R}^d\right)
    \\
    & 
    {}^{ \mathllap{ \left( \theta_{a b} \vert a \neq b\in \{1, \cdots, n + k\} \right) } }\swarrow 
    && 
    \searrow^{ \mathrlap{ \pi_n^{n + k}  } }
    \\
    \left(
      S^{d-1}
    \right)^{n + k}
    && &&
    FM_n\left( \mathbb{R}^d \right)
  }
$$

where 

1. the [[function]] on the left, to the [[Cartesian product]] of one [[n-sphere|(d-1)-spheres]] for each pair of distinct vertices, is given by the functions $\theta_{a b}$ from (eq:ProjectionsToBoundarySpheres)

1. the function on the right is the canonical forgetful projection from Def. \ref{FiberIntegrationOverInternalVertices}, 

hence which sends

$$
  \Gamma 
  \;\mapsto\;
  \underset{ \pi_{n}^{n + int(\Gamma)} }{\int}
  \underset{
    (a \to b) \in \Gamma
  }{\wedge}
  g_{a b}
$$

to the [[fiber integration]] over internal vertices (Def. \ref{FiberIntegrationOverInternalVertices}) of the [[wedge product]] of the [[differential forms]] 

$$
  g_{a b} \coloneqq \theta_{a b}^\ast dvol_{\left(S^{d-1}\right)}
$$ 

(Def. \ref{SphereClassGeneratorsOfDeRhamCohomology}), one for each [[edge]] in the graph from vertex $a$ to vertex $b$.

This function constitutes a [[homomorphism]] of [[dgc-algebras]] which is a [[quasi-isomorphism]].

=--

That this is a dgc-algebra-homomorphism compatible with the [[cooperad]]-[[structure]] is proven in [Lambrechts-Volic 14](#LambrechtsVolic14), that it is a [[quasi-isomorphism]] is proven in [Lambrechts-Volic 14, section 10](#LambrechtsVolic14).


+-- {: .num_remark #AsPerturbativeChernSimonsTheory}
###### Remark
**([[perturbative quantum field theory|perturbative]] [[Chern-Simons theory]] )**

The [[differential forms]] $g_{i j}$ from Def. \ref{SphereClassGeneratorsOfDeRhamCohomology} may be understood as being the [[Feynman propagator]] of [[perturbative quantum field theory|perturbative]] [[higher Chern-Simons theory]] regarded equivalently in its incarnation as a  [[Feynman amplitude on compactified configuration spaces of points]]. See at _[[Chern-Simons propagator]]_ for more on this.

From this perspective, the [[quasi-isomorphism]] in Prop. \ref{QuasiIsomorphismBetweenGraphComplexAndDeRhamComplexOfFM} sends each [[graph]], regarded as a [[Feynman diagram]] for [[higher Chern-Simons theory]], to its correspomnding [[Feynman amplitude]], regarded in its incarnation as a  [[Feynman amplitude on compactified configuration spaces of points]]. 

That this should be the case was originally suggested in [Kontsevich 94](#Kontsevich94).

=--


## Related concepts

* [[little n-disk operad]]

* [[Feynman amplitude on compactified configuration space of points]]

## References

The [[compactification]] of [[configuration spaces of points]] was first considered for two points in 

* {#AxelrodSinger91} [[Scott Axelrod]], [[Isadore Singer]],  _Chern-Simons Perturbation Theory_, in S. Catto, A. Rocha (eds.) Proc. XXthe DGM Conf. World Scientific Singapore, 1992, 3-45; ([arXiv:hep-th/9110056](http://arxiv.org/abs/hep-th/9110056))

* {#AxelrodSinger93} [[Scott Axelrod]], [[Isadore Singer]],  _Chern--Simons Perturbation Theory II_, J. Diff. Geom. 39 (1994) 173-213 ([arXiv:hep-th/9304087](http://arxiv.org/abs/hep-th/9304087)) 

and then more generally in

* {#FultonMacPherson94} William Fulton, Robert MacPherson, _A compactification of configuration spaces_, Ann. of Math. (2), 139(1):183–225, 1994 ([jstor:2946631](https://www.jstor.org/stable/2946631))

based on the general method of [[resolution of singularities]] due to 

* {#Hironaka64} [[Heisuke Hironaka]], _Resolution of Singularities of an Algebraic Variety Over a Field of Characteristic Zero: I_, Annals of Mathematics Second Series, Vol. 79, No. 1 (Jan., 1964), pp. 109-203 (95 pages) ([jstor:1970486](https://www.jstor.org/stable/1970486))

More general compactifications of spaces of _subspace arrangements_ are due to

* {#deConciniProcesi95} [[Corrado de Concini]], [[Claudio Procesi]], _Wonderful models of subspace arrangements_, Selecta Mathematica, New Series Vol. 1, No. 3, 1995 ([pdf](https://link.springer.com/content/pdf/10.1007/BF01589496.pdf))

see also

* {#Feichtner05} Eva Maria Feichner, _De Concini–Procesi Wonderful Arrangement Models:  A Discrete Geometer’s Point of View_, Math. Sci. Res. Inst. Publ 52, 2005 ([pdf](http://library.msri.org/books/Book52/files/17feich.pdf))


The [[operad]]-[[structure]] on Axelrod-Singer Fulton-MacPherson compactifications of [[configuration spaces of points]] was considered in

* {#GetzlerJones94} [[Ezra Getzler]], [[John Jones]], _Operads, homotopy algebra and iterated integrals for double loop spaces_ ([arXiv:hep-th/9403055](https://arxiv.org/abs/hep-th/9403055))

and alternatively in 
 
* {#Kontsevich99} [[Maxim Kontsevich]], around Def. 12 of _Operads and Motives in Deformation Quantization_, Lett.Math.Phys.48:35-72,1999 ([arXiv:math/9904055](https://arxiv.org/abs/math/9904055))

* {#Kontsevich97} [[Maxim Kontsevich]], section 5.1 of _Deformation quantization of Poisson manifolds, I_, Lett.Math.Phys.66:157-216,2003 ([arXiv:q-alg/9709040](https://arxiv.org/abs/q-alg/9709040))

which was corrected in 

* Giovanni Gaiffi, _Models for real subspace arrangements and stratified manifolds_, Int. Math. Res. Not. 12:627-656, 2003 ([pdf](http://www.dm.unipi.it/~gaiffi/papers/models.pdf))

and developed in detail in 

* {#Sinha03} Dev Sinha, _Manifold theoretic compactifications of configuration spaces_, Selecta Math. (N.S.) 10(3):391-428, 2004 ([arXiv:math/0306385](https://arxiv.org/abs/math/0306385))

which also shows the equivalence to [Fulton-MacPherson 94](#FultonMacPherson94).


Review includes

* {#LambrechtsVolic14} [[Pascal Lambrechts]], [[Ismar Volić]], section 5 of _Formality of the little N-disks operad_, Memoirs of the American Mathematical Society; no. 1079, 2014  ([arXiv:0808.0457](https://arxiv.org/abs/0808.0457), [doi:10.1090/memo/1079](http://dx.doi.org/10.1090/memo/1079))


The [[de Rham cohomology]] was determined in 

* {#Cohen73} Fred Cohen, _Cohomology of braid spaces_, Bull. Amer. Math. Soc. Volume 79, Number 4 (1973), 763-766 ([euclid:1183534761](https://projecteuclid.org/euclid.bams/1183534761))

The equivalence to the [[little n-disk operad]] was established in 

* {#Salvatore01} Paolo Salvatore, _Configuration spaces with summable labels_, Cohomological methods in homotopy theory. Birkhäuser, Basel, 2001. 375-395.



{#ReferencesPropagator} The interpretation of the quasi-isomorphism establishing [[formality of the little n-disk operad]] as sending edges to [[Feynman propagators]] of some [[topological quantum field theory]] such as [[Chern-Simons theory]] is due to

* {#AxelrodSinger93} [[Scott Axelrod]], [[Isadore Singer]], Section 2 of _Chern--Simons Perturbation Theory II_, J. Diff. Geom. 39 (1994) 173-213 ([arXiv:hep-th/9304087](http://arxiv.org/abs/hep-th/9304087)) 

which is recalled and recast in somewhat more generality in 

* {#BottCattaneo97} [[Raoul Bott]], [[Alberto Cattaneo]], Remark 3.6 in _Integral invariants of 3-manifolds_, J. Diff. Geom., 48 (1998) 91-133 ([arXiv:dg-ga/9710001](https://arxiv.org/abs/dg-ga/9710001))

* {#CattaneoMnev10} [[Alberto Cattaneo]], [[Pavel Mnev]], Remark 11 in _Remarks on Chern-Simons invariants_, Commun.Math.Phys.293:803-836,2010 ([arXiv:0811.2045](https://arxiv.org/abs/0811.2045))

That this should exhibit a graph complex model for the cohomology of compactified configuration spaces was suggested in 

* {#Kontsevich94} [[Maxim Kontsevich]], pages 11-12 of _Feynman diagrams and low-dimensional topology_, First European Congress of Mathematics, 1992, Paris, vol. II, Progress in Mathematics __120__, Birkh&#228;user (1994), 97&#8211;121 ([pdf](http://www.ihes.fr/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf))

and spelled out in more detail in 

* [Kontsevich 99, section 3](#Kontsevich99)

with a careful proof being layed out in 

* [Lambrechts-Volic 14](#LambrechtsVolic14)


[[!redirects Fulton-MacPherson operads]]

[[!redirects Fulton-MacPherson compactification]]
[[!redirects Fulton-MacPherson compactifications]]
