
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
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


The _classical model structure on simplicial sets_ or _Kan-Quillen model structure_ , $sSet_{Quillen}$ ([Quillen 67, II.3](#Quillen67)) is a [[model category]] structure on the [[category]] [[sSet]] of [[simplicial sets]] which represents the standard classical [[homotopy theory]]. 

Its [[weak equivalences]] are the [[simplicial weak equivalences]] ([[isomorphisms]] on [[simplicial homotopy groups]]), its [[fibrations]] are the [[Kan fibrations]] and its [[cofibrations]] are the [[monomorphisms]] (degreewise injections).

The [[singular simplicial complex]]/[[geometric realization]] [[nerve and realization|adjunction]] constitutes a [[Quillen equivalence]] between 
$sSet_{Quillen}$ and $Top_{Quillen}$, the [[classical model structure on topological spaces]]. This is sometimes called part of the statement of the _[[homotopy hypothesis]]_ [for Kan complexes](homotopy+hypothesis#ForKanComplexes). In the language of [[(∞,1)-category theory]] this means that $sSet_{Quillen}$ and $Top_{Quillen}$ both are [[presentable (∞,1)-category|presentations]] of the [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoids]].

There are also other model structures on [[sSet]] itself, see at _[[model structure on simplicial sets]]_ for more. This entry here focuses on just the standard classical model structure.


## Background on combinatorial topology

This section reviews basics of the theory of [[simplicial sets]] (the modern version of the original "combinatorial topology") necessary to define, verify and analyse the classical model category structure on simplicial sets, [below](#TheClassicalModelStructure). See also at _[[simplicial homotopy theory]]_.

### Simplicial sets

The concept of [[simplicial sets]] is secretly well familiar already in basic [[algebraic topology]]: it reflects just the abstract structure carried by the [[singular simplicial complexes]] of [[topological spaces]], as in the definition of [[singular homology]] and [[singular cohomology]]. 

Conversely, every simplicial set may be [[geometric realization|geometrically realized]] as a topological space. These two [[adjoint]] operations turn out to exhibit the homotopy theory of simplicial sets as being equivalent ([[Quillen equivalence|Quillen equivalent]]) to the homotopy theory of topological spaces.  For some purposes, working in [[simplicial homotopy theory]] is preferable over working with topological homotopy theory.

+-- {: .num_defn #TopologicalSimplex}
###### Definition

For $n \in \mathbb{N}$, the **[topological n-simplex](simplex#TopologicalSimplex)** is,  up to [[homeomorphism]], the [[topological space]] whose underlying set is the subset

$$
  \Delta^n \coloneqq 
  \{
    \vec x \in \mathbb{R}^{n+1}
    |
    \sum_{i = 0 }^n x_i = 1 \; and \;
    \forall i . x_i \geq 0 
  \}
  \subset \mathbb{R}^{n+1}
$$

of the [[Cartesian space]] $\mathbb{R}^{n+1}$, and whose topology is the  [[nLab:subspace topology]] induces from the canonical topology in $\mathbb{R}^{n+1}$.

=--

+-- {: .num_example}
###### Example

For $n = 0$ this is the [[point]], $\Delta^0 = *$.

For $n = 1$ this is the standard [[interval object]] $\Delta^1 = [0,1]$.

For $n = 2$ this is the filled triangle.

For $n = 3$ this is the filled tetrahedron.

=--



+-- {: .num_defn #FaceInclusionInBarycentricCoords}
###### Definition

For $n \in \mathbb{N}$, $\n \geq 1$ and $0 \leq k \leq n$, the 
**$k$th $(n-1)$-face (inclusion)**  of the topological $n$-simplex, def. \ref{TopologicalSimplex}, is the subspace inclusion

$$
  \delta_k : \Delta^{n-1} \hookrightarrow \Delta^n
$$

induced under the coordinate presentation of def. \ref{TopologicalSimplex},
by the inclusion 

$$
  \mathbb{R}^n \hookrightarrow \mathbb{R}^{n+1}
$$

which "omits" the $k$th canonical coordinate:

$$
  (x_0, \cdots , x_{n-1}) \mapsto (x_0, \cdots, x_{k-1} , 0 , x_{k}, \cdots, x_n)
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

<img src="http://ncatlab.org/nlab/files/faceanddegeneracymaps.jpg" width="500" >

(graphics taken from [Friedman 08](https://ncatlab.org/nlab/show/simplicial+set#Friedman08))

+-- {: .num_defn #DegeneracyProjectionsInBarycentricCoords}
###### Definition

For $n \in \mathbb{N}$ and $0 \leq k \lt n$ the **$k$th degenerate $(n)$-simplex (projection)** is the surjective map

$$
  \sigma_k : \Delta^{n} \to \Delta^{n-1}
$$

induced under the barycentric coordinates of def. \ref{TopologicalSimplex} under the surjection

$$
  \mathbb{R}^{n+1} \to \mathbb{R}^n
$$

which sends

$$
  (x_0, \cdots, x_n) \mapsto (x_0, \cdots, x_{k} + x_{k+1}, \cdots, x_n)
  \,.
$$

=--

+-- {: .num_defn #SingularSimplex}
###### Definition

For $X \in $ [[Top]]  and $n \in \mathbb{N}$, a **singular $n$-simplex** in $X$ is a [[continuous map]]

$$
  \sigma : \Delta^n \to X
$$

from the topological $n$-simplex, def. \ref{TopologicalSimplex}, to $X$.

Write 

$$
  (Sing X)_n \coloneqq Hom_{Top}(\Delta^n , X)
$$ 

for the set of singular $n$-simplices of $X$.

=--

<img src="http://ncatlab.org/nlab/files/singularsimplices.jpg" width="500" >

(graphics taken from [Friedman 08](https://ncatlab.org/nlab/show/simplicial+set#Friedman08))

The sets $(Sing X)_\bullet$ here are closely related by an interlocking system of maps that make them form what is called a _[[simplicial set]]_, and as such the collection of these sets of singular simplices is called the _[[singular simplicial complex]]_ of $X$. We discuss the definition of simplicial sets now and then come back to this below in def. \ref{SingularSimplicialComplex}.

Since the topological $n$-simplices $\Delta^n$ from def. \ref{TopologicalSimplex} sit inside each other by the face inclusions of def. \ref{FaceInclusionInBarycentricCoords}

$$
  \delta_k : \Delta^{n-1} \to \Delta^{n}
$$

and project onto each other by the degeneracy maps, def. \ref{DegeneracyProjectionsInBarycentricCoords}

$$
  \sigma_k : \Delta^{n+1} \to \Delta^n
$$

we dually have functions

$$
  d_k \coloneqq Hom_{Top}(\delta_k, X) : (Sing X)_n \to (Sing X)_{n-1}
$$

that send each singular $n$-simplex to its $k$-face and functions

$$
  s_k \coloneqq Hom_{Top}(\sigma_k,X) : (Sing X)_{n} \to (Sing X)_{n+1}
$$

that regard an $n$-simplex as beign a degenerate ("thin") $(n+1)$-simplex.
All these sets of simplices and face and degeneracy maps between them form the following structure. 

+-- {: .num_defn #SimplicialSet}
###### Definition

A **[[simplicial set]]** $S \in sSet$ is 

* for each $n \in \mathbb{N}$ a [[set]] $S_n \in Set$ -- the **set of $n$-[[simplices]]**;

* for each [[injective map]] $\delta_i : \overline{n-1} \to \overline{n}$ of [[nLab:totally ordered sets]] $\bar n \coloneqq \{ 0 \lt 1 \lt \cdots \lt n \}$

  a [[function]] $d_i : S_{n} \to S_{n-1}$ -- the $i$th **face map** on $n$-simplices;

* for each [[surjective map]] $\sigma_i : \overline{n+1} \to \bar n$ of [[totally ordered sets]]

  a [[function]] $\sigma_i : S_{n} \to S_{n+1}$ -- the $i$th **degeneracy map** on $n$-simplices;

such that these functions satisfy the _[[simplicial identities]]_.

=--

+-- {: .num_defn #SimplicialIdentities}
###### Definition

The **simplicial identities** satisfied by face and degeneracy maps as above are (whenever these maps are composable as indicated):

1. $ d_i \circ d_j  = d_{j-1} \circ d_i$ if $i \lt j$,

1. $s_i \circ s_j  = s_j \circ s_{i-1}$ if $i \gt j$.

1. $d_i \circ s_j =  \left\{ \array{ s_{j-1} \circ d_i &  if \;  i \lt j \\ id & if  \;  i = j \; or \; i = j+1 \\ s_j \circ d_{i-1} &  if i \gt j+1 } \right. $

=--

It is straightforward to check by explicit inspection that the evident injection and restriction maps between the sets of [[singular simplices]] make $(Sing X)_\bullet$ into a simplicial set. However for working with this, it is good to streamline a little:

+-- {: .num_defn}
###### Definition

The **[[simplex category]]** $\Delta$ is the [[full subcategory]] of [[Cat]] on the free categories of the form

$$
  \begin{aligned}
    [0] & \coloneqq \{0\}
    \\
    [1] & \coloneqq \{0 \to 1\}
    \\
   [2] & \coloneqq \{0 \to 1 \to 2\}
   \\
   \vdots
   \end{aligned}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This is called the "simplex category" because we are to think of the object $[n]$ as being the "[[spine]]" of the $n$-[[simplex]]. For instance for $n = 2$ we think of $0 \to 1 \to 2$ as the "spine" of the triangle. This becomes clear if we don't just draw the morphisms that _generate_ the category $[n]$, but draw also all their composites. For instance for $n = 2$ we have_

$$
  [2]  
  = 
  \left\{
  \array{
     && 1
     \\
     & \nearrow && \searrow
     \\
    0 &&\to&& 2
  }
  \right\}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

A [[functor]] 

$$
  S : \Delta^{op} \to Set
$$

from the [[opposite category]] of the [[nLab:simplex category]] to the category [[Set]] of sets is canonically identified with a [[simplicial set]], def. \ref{SimplicialSet}.

=--

+-- {: .proof}
###### Proof

One checks by inspection that the simplicial identities 
characterize precisely the behaviour of the morphisms in
$\Delta^{op}([n],[n+1])$ and $\Delta^{op}([n],[n-1])$.

=--

This makes the following evident:

+-- {: .num_example #StandardCosimplicialTopologicalSpace}
###### Example

The [[topological simplices]] from def. \ref{TopologicalSimplex} arrange into a _[[cosimplicial object]] in [[Top]]_, namely a [[functor]]

$$
  \Delta^\bullet : \Delta \to Top
  \,.
$$

=--

With this now the structure of a simplicial set on $(Sing X)_\bullet$, def. \ref{SingularSimplex}, is manifest: it is just the _[[nerve]]_ of $X$ with respect to $\Delta^\bullet$, namely:

+-- {: .num_defn #SingularSimplicialComplex}
###### Definition

For $X$ a [[topological space]] its **[[singular simplicial complex|simplicial set of singular simplicies]]**  (often called the **[[singular simplicial complex]]**)

$$
  (Sing X)_\bullet : \Delta^{op} \to Set
$$

is given by composition of the functor from example \ref{StandardCosimplicialTopologicalSpace} with the [[nLab:hom functor]] of [[nLab:Top]]:

$$
  (Sing X) : [n] \mapsto Hom_{Top}( \Delta^n , X )
  \,.
$$

=--

+-- {: .num_remark}
###### Remark 

It turns out -- this is the content of the _[[nLab:homotopy hypothesis]]-theorem_ ([Quillen 67](model+structure+on+simplicial+sets#Quillen67)) -- that [[homotopy type]] of the topological space $X$ is entirely captured by its singular simplicial complex $Sing X$. Moreover, the [[geometric realization]] of $Sing X$ is a model for the same [[homotopy type]] as that of $X$, but with the special property that it is canonically a [[cell complex]] -- a [[CW-complex]]. Better yet, $Sing X$ is itself already good cell complex, namely a [[Kan complex]]. We come to this below.

=--

### Simplicial homotopy

The concept of [[homotopy]] of morphisms between simplicial sets proceeds in direct analogy with that in [[topological spaces]].

+-- {: .num_defn #LeftHomotopyOfSimplicialSets}
###### Definition

For $X$ a [[simplicial set]], def. \ref{SimplicialSet}, its _simplicial [[cylinder object]]_ is the [[Cartesian product]] $X\times \Delta[1]$ (formed in the [[category]] [[sSet]]).

A _[[left homotopy]]_ 

$$
  \eta \;\colon\; f \Rightarrow g
$$

between two morphisms

$$
  f,g\;\colon\; X \longrightarrow Y
$$

of [[simplicial sets]] is a morphism 

$$
  \eta \;\colon\; X \times \Delta[1] \longrightarrow Y
$$

such that the following [[commuting diagram|diagram commutes]]

$$
  \array{
     X 
     \\
     {}^{\mathllap{(id_X,d_1)}}\downarrow & \searrow^{\mathllap{f}}
     \\
     X \times \Delta^1 &\stackrel{\eta}{\longrightarrow}& Y
     \\
     {}^{\mathllap{(id_x, d_0)}}\uparrow & \nearrow_{\mathllap{g}}
     \\
     X
  }
  \,.
$$

For $Y$ a [[Kan complex]], def. \ref{SimplicialSet}, its _simplicial [[path space object]]_ is the [[function complex]] $X^{\Delta[1]}$ (formed in the [[category]] [[sSet]]).

A _[[right homotopy]]_ 

$$
  \eta \;\colon\; f \Rightarrow g
$$

between two morphisms

$$
  f,g\;\colon\; X \longrightarrow Y
$$

of [[simplicial sets]] is a morphism 

$$
  \eta \colon X \longrightarrow Y^{\Delta[1]}
$$

such that the following [[commuting diagram|diagram commutes]]

$$
  \array{
    && Y
    \\
    & {}^{\mathllap{f}}\nearrow & \uparrow^{\mathrlap{Y^{d_1}}}
    \\
    X &\stackrel{\eta}{\longrightarrow}& Y^{\Delta[1]}
    \\
    & {}_{\mathllap{g}}\searrow & \downarrow^{\mathrlap{Y^{d_0}}}
    \\
    && 
    Y
  }
  \,.
$$

=--

+-- {: .num_prop #LeftHomotopyIsEquivalence}
###### Proposition

For $Y$ a [[Kan complex]], def. \ref{KanComplexes}, and $X$ any [[simplicial set]], then left homotopy, def. \ref{LeftHomotopyOfSimplicialSets},
regarded as a [[relation]]

$$
  (f\sim g) \Leftrightarrow (f \stackrel{\exists}{\Rightarrow} g)
$$

on the [[hom set]] $Hom_{sSet}(X,Y)$, is an [[equivalence relation]].

=--

+-- {: .num_defn #HomotopyEquivalence}
###### Definition

A morphism $f \colon X \longrightarrow Y$ of [[simplicial sets]] is a left/right [[homotopy equivalence]] if there exists a morphisms $X \longleftarrow Y \colon g$ and left/right homotopies (def. \ref{LeftHomotopyOfSimplicialSets})

$$
  g \circ f \Rightarrow id_X\,,\;\;\;\; f\circ g \Rightarrow id_Y
$$

=--

The the basic invariants of [[simplicial sets]]/[[Kan complexes]] in [[simplicial homotopy theory]] are their [[simplicial homotopy groups]], to which we turn now.
 
Given that a [[Kan complex]] is a special [[simplicial set]] that [[homotopy hypothesis|behaves like]] a combinatorial model for a [[topological space]], the _simplicial homotopy groups_ of a  Kan complex are accordingly the combinatorial analog of the [[homotopy groups]] of [[topological spaces]]: instead of being maps from topological [[spheres]] modulo maps from topological disks, they are maps from the [[boundary of a simplex]] modulo those from the [[simplex]] itself. 

Accordingly, the definition of the discussion of simplicial homotopy groups is essentially literally the same as that of [[homotopy groups]] of topological spaces.  One technical difference is for instance that the definition of the group structure is slightly more non-immediate for simplicial homotopy groups than for topological homotopy groups (see below).


+-- {: .num_defn #UnderlyingSetsOfSimplicialHomotopyGroups}
###### Definition 

For $X$ a [[Kan complex]], then its **0th [[simplicial homotopy group]]** (or **set of [[connected components]]**) is the set of [[equivalence classes]] of vertices modulo the [[equivalence relation]] $X_1 \stackrel{(d_1,d_0)}{\longrightarrow} X_0 \times X_0$

$$
  \pi_0(X) \colon X_0/X_1
  \,.
$$

For $x \in X_0$ a vertex and for $n \in \mathbb{N}$, $n \geq 1$, then the underlying [[set]]  of the **$n$th [[simplicial homotopy group]]** of $X$ at $x$ -- denoted $\pi_n(X,x)$ -- is, the set of [[equivalence classes]] $[\alpha]$ of morphisms

$$
  \alpha \colon \Delta^n \to X
$$ 
 
from the simplicial $n$-[[simplex]] $\Delta^n$ to $X$, such that these take the [[boundary of a simplex|boundary of the simplex]] to $x$, i.e. such that they fit into a [[commuting diagram]] in [[sSet]] of the form
 
$$
  \array{
     \partial \Delta[n] & \longrightarrow &  \Delta[0]
     \\
     \downarrow && \downarrow^{\mathrlap{x}}
     \\
     \Delta[n] &\stackrel{\alpha}{\longrightarrow}& X
   }
  \,,
$$


where two such maps $\alpha, \alpha'$ are taken to be equivalent is they are related by a [[simplicial homotopy]] $\eta$

$$
  \array{
     \Delta[n]
     \\
     \downarrow^{i_0} & \searrow^{\alpha}
     \\
     \Delta[n] \times \Delta[1]
     &\stackrel{\eta}{\longrightarrow}&
     X
     \\
     \uparrow^{i_1} & \nearrow_{\alpha'}
     \\
     \Delta[n]
  }
$$

that fixes the boundary in that it fits into a [[commuting diagram]] in [[sSet]] of the form

$$
  \array{
     \partial \Delta[n] \times \Delta[1]
     & \longrightarrow &
     \Delta[0]
     \\
     \downarrow && \downarrow^{\mathrlap{x}}
     \\
     \Delta[n]  \times \Delta[1]
     &\stackrel{\eta}{\longrightarrow}&
     X
  }
  \,.
$$

=--

These sets are taken to be equipped with the following group structure.

+-- {: .num_defn #ProductOnSimplicialHomotopyGroups}
###### Definition 
  
For $X$ a [[Kan complex]], for $x\in X_0$, for $n \geq 1$ and for  $f,g \colon \Delta[n] \to X$ two representatives of $\pi_n(X,x)$ as in def. \ref{UnderlyingSetsOfSimplicialHomotopyGroups}, consider the following $n$-simplices in $X_n$:

$$
  v_i 
  \coloneqq
  \left\{
    \array{
      s_0 \circ s_0 \circ \cdots \circ s_0 (x) & for \; 0 \leq i \leq  n-2
      \\
      f & for \; i = n-1
      \\
      g & for \; i = n+1
    }
  \right.
$$

This corresponds to a morphism $\Lambda^{n+1}[n] \to X$ from a [[horn]] of the $(n+1)$-[[simplex]] into $X$. By the [[Kan complex]] property of $X$ this morphism has an [[extension]] $\theta$ through the $(n+1)$-[[simplex]] $\Delta[n]$

$$
  \array{
     \Lambda^{n+1}[n] & \longrightarrow & X
     \\
     \downarrow & \nearrow_{\mathrlap{\theta}}
     \\
     \Delta[n+1]
  }
$$

From the [[simplicial identities]] one finds that the boundary of the $n$-simplex arising as the $n$th boundary piece $d_n \theta$ of $\theta$ is constant on $x$

$$
  d_i d_{n} \theta = d_{n-1} d_i \theta = x
$$

So $d_n \theta$ represents an element in $\pi_n(X,x)$ and we define a product operation on $\pi_n(X,x)$ by

$$
  [f]\cdot [g] \coloneqq [d_n \theta]
  \,.
$$

=--

(e.g. [Goerss-Jardine 99, p. 26](#GoerssJardine99))

+-- {: .num_remark}
###### Remark 

All the degenerate $n$-simplices $v_{0 \leq i \leq n-2}$ in def. \ref{ProductOnSimplicialHomotopyGroups} are just there so that the gluing of the two $n$-cells $f$ and $g$ to each other can be regarded as forming the boundary of an $(n+1)$-simplex except for one face. By the Kan extension property that missing face exists, namely $d_n \theta$.  This is a choice of gluing composite of $f$ with $g$.

=--

+-- {: .num_lemma}
###### Lemma

The product on homotopy group elements in def. \ref{ProductOnSimplicialHomotopyGroups} is
well defined, in that it is independent of the
choice of representatives $f$, $g$ and of the extension $\theta$.

=--

e.g. ([Goerss-Jardine 99, lemma 7.1](#GoerssJardine99))


+-- {: .num_lemma}
###### Lemma

The product operation in def. \ref{ProductOnSimplicialHomotopyGroups} yields a [[group]] structure on $\pi_n(X,x)$, which is [[abelian group|abelian]] for $n \geq 2$.

=--

e.g. ([Goerss-Jardine 99, theorem 7.2](#GoerssJardine99))

+-- {: .num_remark}
###### Remark 

The first homotopy group, $\pi_1(X,x)$, is also called the _[[fundamental group]]_ of $X$. 

=---


+-- {: .num_defn #WeakHomotopyEquivalence}
###### Definition

For $X,Y \in KanCplx \hookrightarrow sSet$ two [[Kan complexes]], then a morphism

$$
  f \colon X \longrightarrow Y
$$

is called a **[[weak homotopy equivalence]]** if it induces [[isomorphisms]] on all [[simplicial homotopy groups]], i.e. if

1. $\pi_0(f) \colon \pi_0(X) \longrightarrow \pi_0(Y)$ is a [[bijection]] of sets;

1. $\pi_n(f,x) \colon \pi_n(X,x) \longrightarrow \pi_n(Y,f(x))$ is an [[isomorphism]] of [[groups]] for all $x\in X_0$ and all $n \in \mathbb{N}$; $n \geq 1$.

=--



### Kan fibrations

+-- {: .num_defn #Horn}
###### Definition

For each $i$, $0 \leq i \leq n$, the **$(n,i)$-horn** 
is the subsimplicial set 

$$
  \Lambda^i[n]
  \hookrightarrow
  \Delta[n] 
$$

of the simplicial $n$-[[simplex]], which is the [[union]] of all faces _except_ the  $i^{th}$ one.

This is called an **outer horn** if $k = 0$ or $k = n$.  Otherwise it is an **inner horn**.


=--

<img src="http://ncatlab.org/nlab/files/2horns.jpg" width="500" >

(graphics taken from [Friedman 08](https://ncatlab.org/nlab/show/simplicial+set#Friedman08))


+-- {: .num_remark }
###### Remark

Since [[sSet]]  is a [[presheaf category]], [[unions]] of [[subobjects]] make sense and they are calculated objectwise, thus in this case dimensionwise.  This way it becomes clear what the structure of a horn as a functor $\Lambda^k[n]: \Delta^{op} \to Set$ must therefore be: it takes $[m]$ to the collection of ordinal maps $f: [m] \to [n]$ which do not have the element $k$ in the image.

=--


+-- {: .num_defn #KanComplexes}
###### Definition

A _[[Kan complex]]_ is a [[simplicial set]] $S$ that satisfies the _Kan condition_, 

* which says that all [[horns]] of the simplicial set have _fillers_/extend to [[simplices]];

* which means equivalently that the unique homomorphism $S \to pt$ from $S$ to the [[point]] (the [[terminal object|terminal]] [[simplicial set]]) is a [[Kan fibration]];

* which means equivalently that for all [[diagrams]] of the form

  $$
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] &\to& pt
  }
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow && 
    \\
    \Delta[n] 
  }
  $$

  there exists a diagonal morphism

  $$
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow &\nearrow& \downarrow
    \\
    \Delta[n] &\to& pt
  }
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow &\nearrow& 
    \\
    \Delta[n] 
  }
  $$

  completing this to a [[commuting diagram]];

* which in turn means equivalently that the map from $n$-simplices to $(n,i)$-horns is an [[epimorphism]]
$$
  [\Delta[n], S]\, \twoheadrightarrow \,[\Lambda^i[n],S]
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For $X$ a [[topological space]], its [[singular simplicial complex]]
$Sing(X)$, def. \ref{SingularSimplicialComplex}, is a Kan complex, def. \ref{KanComplexes}.

=--

+-- {: .proof}
###### Proof

The inclusions ${{\Lambda^n}_{Top}}_k \hookrightarrow \Delta^n_{Top}$ of topological horns into topological simplices are  [[retracts]], in that there are [[continuous maps]] $\Delta^n_{Top} \to {{\Lambda^n}_{Top}}_k$ given by "squashing" a topological $n$-simplex onto parts of its boundary, such that

$$
  ({{\Lambda^n}_{Top}}_k \to \Delta^n_{Top} \to
  {{\Lambda^n}_{Top}}_k)
  =
  Id
  \,.
$$

Therefore the map
$[\Delta^n, \Pi(X)] \to [\Lambda^n_k,\Pi(X)]$ is an epimorphism, since it is equal to  to $Top(\Delta^n, X) \to Top(\Lambda^n_k, X)$ which has a right inverse $Top(\Lambda^n_k, X) \to Top(\Delta^n, X)$.

=--

More generally: 

+-- {: .num_defn #KanFibration}
###### Definition

A morphism $\phi \colon S \longrightarrow T$ in [[sSet]] is called a _[[Kan fibration]]_ if it has the [[right lifting property]] again all [[horn]] inclusions, def. \ref{Horn}, hence if for every [[commuting diagram]] of the form

$$
  \array{
    \Lambda^i[n] &\longrightarrow& S
    \\
    \downarrow && \downarrow^{\mathrlap{\phi}}
    \\
    \Delta[n] &\longrightarrow& T
  }
$$

there exists a lift

$$
  \array{
    \Lambda^i[n] &\longrightarrow& S 
    \\
    \downarrow &\nearrow& \downarrow^{\mathrlap{\phi}}
    \\
    \Delta[n] &\longrightarrow& T
  }
  \,.
$$

=--

This is the simplicial incarnation of the concept of [[Serre fibrations]] of topological spaces:

+-- {: .num_defn #SerreFibration}
###### Definition

A [[continuous function]] $f \colon X \longrightarrow Y$ between [[topological spaces]] is a [[Serre fibration]] if for all [[CW-complexes]] $C$ and for every [[commuting diagram]] in [[Top]] of the form

$$
  \array{
    C &\longrightarrow& X 
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    C \times I &\longrightarrow& Y
  }
$$

there exists a lift

$$
  \array{
    C &\longrightarrow& X 
    \\
    \downarrow &\nearrow& \downarrow^{\mathrlap{f}}
    \\
    C \times I &\longrightarrow& Y
  }
  \,.
$$

=--

+-- {: .num_prop #SingDetextsAndReflectsFibrations}
###### Proposition

A [[continuous function]] $f \colon X \longrightarrow Y$ is a [[Serre fibration]], def. \ref{SerreFibration}, precisely if $Sing(f) \colon Sing(X) \longrightarrow Sing(Y)$ (def. \ref{SingularSimplicialComplex}) is a [[Kan fibration]], def. \ref{KanFibration}.

=--

The proof uses the basic tool of [[nerve and realization]]-[[adjunction]] to which we get to below in prop. \ref{NerveAndRealizationAdjunction}.

+-- {: .proof}
###### Proof

First observe that the left [[lifting property]] against all $C \hookrightarrow C \times I$ for $C$ a [[CW-complex]] is equivalent to left lifting against [[geometric realization]] ${\vert \Lambda^i[n]\vert} \hookrightarrow {\vert \Delta[n]\vert}$ of [[horn]] inclusions.
Then apply the [[natural isomorphism]] $Top({\vert-\vert},-) \simeq sSet(-,Sing(-))$,  given by the [[adjunction]] of prop. \ref{NerveAndRealizationAdjunction} and example \ref{TopologicalRealizationOfSimplicialSets}, to the lifting diagrams.

=--


+-- {: .num_lemma #PullbackOfKanFibrationSendsLeftHomotopyToFiberwiseHomotopyequivalence}
###### Lemma

Let $p \colon X \longrightarrow Y$ be a [[Kan fibration]], def. \ref{KanFibration}, and let $f_1,f_2 \colon A \longrightarrow X$ be two morphisms. If there is a [[left homotopy]] (def. \ref{LeftHomotopyOfSimplicialSets}) $f_1 \Rightarrow f_2$ between these maps, then there is a fiberwise [[homotopy equivalence]], def. \ref{HomotopyEquivalence}, between the [[pullback]] fibrations $f_1^\ast X \simeq f_2^\ast X$.

=--

(e.g. [Goerss-Jardine 99, chapter I, lemma 10.6](#GoerssJardine99))


While [[simplicial sets]] have the advantage of being purely combinatorial structures, the [[singular simplicial complex]] of any given [[topological space]], def. \ref{SingularSimplicialComplex} is in general a huge simplicial set which does not lend itself to detailed inspection. The following is about small models.

+-- {: .num_defn #MinimalKanFibration}
###### Definition

A [[Kan fibration]] $\phi \colon S \longrightarrow T$, def. \ref{KanFibration}, is called a **[[minimal Kan fibration]]** if for any two cells in the same fiber with the same [[boundary]] if they are homotopic relative their boundary, then they are already equal.

More formally, $\phi$ is minimal precisely if for every [[commuting diagram]] of the form

$$
  \array{
    (\partial \Delta[n]) \times \Delta[1]
    &\stackrel{p_1}{\longrightarrow}&
    \partial \Delta[n]
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] \times \Delta[1]
    &\stackrel{h}{\longrightarrow}&
    S
    \\
    \downarrow^{\mathrlap{p_1}} && \downarrow^{\mathrlap{\phi}}
    \\
    \Delta[n] &\longrightarrow& T
  }
$$

then the two composites 

$$
  \Delta[n]
  \stackrel{\overset{d_0}{\longrightarrow}}{\underset{d_1}{\longrightarrow}} 
  \Delta[n] \times \Delta[1]
  \stackrel{h}{\longrightarrow}
  S
$$

are equal.

=--

+-- {: .num_prop #PullbackPreservesMinimalFibration}
###### Proposition

The [[pullback]] (in [[sSet]]) of a [[minimal Kan fibration]], def. \ref{MinimalKanFibration}, along any morphism is again a mimimal Kan fibration. 

=--


... [[anodyne extensions]]...

([Goerss-Jardine 99, chapter I, section 4](#GoerssJardine99), [Joyal-Tierney 05, section 31](#JoyalTierney05))


+-- {: .num_prop #KanFibrationHasMinimalStrongDeformationRetract}
###### Proposition

For every [[Kan fibration]], def. \ref{KanFibration}, there exists a fiberwise [[strong deformation retract]] to a [[minimal Kan fibration]], def. \ref{MinimalKanFibration}.

=--

(e.g. [Goerss-Jardine 99, chapter I, prop. 10.3](#GoerssJardine99), [Joyal-Tierney 05, theorem 3.3.1, theorem 3.3.3](#JoyalTierney05)).

+-- {: .proof}
###### Proof idea

Choose representatives by [[induction]], use that in the induction step one needs lifts of [[anodyne extensions]] against a [[Kan fibration]], which exist.

=--

+-- {: .num_lemma #FiberwiseHomotopyEquivalenceOfMinimalFibrationsIsIso}
###### Lemma

A morphism between [[minimal Kan fibrations]], def. \ref{MinimalKanFibration}, which is fiberwise a [[homotopy equivalence]], def. \ref{HomotopyEquivalence}, is already an [[isomorphism]].

=--

(e.g. [Goerss-Jardine 99, chapter I, lemma 10.4](#GoerssJardine99))

+-- {: .proof}
###### Proof idea

Show the statement degreewise. In the [[induction]] one needs to lift [[anodyne extensions]] agains a [[Kan fibration]].

=--

+-- {: .num_lemma #MinimalKanFibrationAreFiberBundles}
###### Lemma

Every [[minimal Kan fibration]], def. \ref{MinimalKanFibration}, over a [[connected]] base is a simplicial [[fiber bundle]], locally trivial over every simplex of the base.

=--

(e.g. [Goerss-Jardine 99, chapter I, corollary 10.8](#GoerssJardine99))

+-- {: .proof}
###### Proof

By assumption of the base being connected, the classifying maps for the fibers over any two vertices are connected by a [[zig-zag]] of [[homotopies]], hence by lemma \ref{PullbackOfKanFibrationSendsLeftHomotopyToFiberwiseHomotopyequivalence} the fibers are connected by [[homotopy equivalences]] and then by prop. \ref{PullbackPreservesMinimalFibration} and lemma \ref{FiberwiseHomotopyEquivalenceOfMinimalFibrationsIsIso} they are already isomorphic. Write $F$ for this [[typical fiber]].

Moreover, for all $n$ the morphisms $\Delta[n] \to \Delta[0] \to \Delta[n]$ are [[left homotopy|left homotopic]] to $\Delta[n] \stackrel{id}{\to} \Delta[n]$ and so applying lemma \ref{PullbackOfKanFibrationSendsLeftHomotopyToFiberwiseHomotopyequivalence} and prop. \ref{FiberwiseHomotopyEquivalenceOfMinimalFibrationsIsIso} once more yields that the fiber over each $\Delta[n]$ is [[isomorphism|isomorphic]] to $\Delta[n]\times F$.

=--

### Geometric realization

So far we we have considered passing from [[topological spaces]] to [[simplicial sets]] by applying the [[singular simplicial complex]] functor of def. \ref{SingularSimplicialComplex}.
Now we discuss a [[left adjoint]] of this functor, called [[geometric realization]], which turns a simplicial set into a topological space by identifying each of its abstract [[n-simplices]] with the standard topological $n$-simplex. 

This is an example of a general abstract phenomenon:

+-- {: .num_prop #NerveAndRealizationAdjunction}
###### Proposition

Let 

$$
  \delta \;\colon\; D \longrightarrow \mathcal{C}
$$

be a [[functor]] from a [[small category]] $D$ to a [[locally small category]] $\mathcal{C}$ with all [[colimits]].  Then the [[nerve]]-functor

$$
  N \;\colon\; \mathcal{C} \longrightarrow [D^{op}, Set]
$$

$$
  N(X) \coloneqq \mathcal{C}(\delta(-),X)
$$

has a [[left adjoint]] functor ${\vert-\vert}$, called [[geometric realization]],
 
$$
  ({\vert-\vert} \dashv N)
  \;\colon\;
  \mathcal{C}
  \stackrel{\overset{{\vert-\vert}}{\longleftarrow}}{\underset{N}{\longrightarrow}}
  [D^{op}, Set]
$$

given by the [[coend]]

$$
  {\vert S\vert}
  =
  \int^{d \in D} \delta(d) \cdot S(d)
  \,.
$$

=--

([Kan 58](nerve+and+realization#Kan58))


+-- {: .proof}
###### Proof

By basic propeties of [[ends]] and [[coends]]:

$$
  \begin{aligned}
     [D^{op}, Set](S,N(X))
     & =
     \int_{d \in D} Set(S(d), N(X)(d))
     \\
     & = \int_{d\in D} Set(S(d), \mathcal{C}(\delta(d),X))
     \\
     & \simeq \int_{d \in D} \mathcal{C}(\delta(d) \cdot S(d), X)
     \\
     & \simeq \mathcal{C}(\int^{d \in D} \delta(d) \cdot S(d), X)
     \\
     & = \mathcal{C}({\vert S\vert}, X)
     \,.
  \end{aligned}
$$

=--

+-- {: .num_example #TopologicalRealizationOfSimplicialSets}
###### Example

The [[singular simplicial complex]] functor $Sing$ of def. \ref{SingularSimplicialComplex} has a [[left adjoint]] [[geometric realization]] functor

$$
  {\vert-\vert}
  \colon
  sSet \longrightarrow Top
$$

given by the [[coend]]

$$
  {\vert S \vert}
  =
  \int^{[n]\in \Delta}
  \Delta^n \cdot S_n
  \,.
$$


=--

Topological geometric realization takes values in particularly nice topological spaces.

+-- {: .num_defn #TopologicalRealizationOfsSetLandsInCWComplexes}
###### Proposition

The topological [[geometric realization]] of [[simplicial sets]]
in example \ref{TopologicalRealizationOfSimplicialSets} takes values in [[CW-complexes]].

=--

(e.g. [Goerss-Jardine 99, chapter I, prop. 2.3](#GoerssJardine99))

Thus for a topological space $X$ the [[adjunction counit]] $\epsilon_X \colon {\vert Sing X\vert} \longrightarrow X$ of the [[nerve and realization]]-adjunction is a candidate for a replacement of $X$ by a CW-complex. For this, $\epsilon_X$ should be at least a [[weak homotopy equivalence]], i.e. induce [[isomorphisms]] on all [[homotopy groups]]. Since homotopy groups are built from maps into $X$ out of [[compact topological spaces]] it is plausible that this works if the topology of $X$ is entirely detected by maps out of compact topological spaces into $X$. Topological spaces with this property are called [[compactly generated topological spaces|compactly generated]].

We take _[[compact topological space]]_ to imply _[[Hausdorff topological space]]_.

+-- {: .num_defn #kTop}
###### Definition

A [[subspace]] $U \subset X$ of a [[topological space]] $X$ is called **compactly open** or **compactly closed**, respectively, if for every [[continuous function]] $f \colon K \longrightarrow X$ out of a [[compact topological space]] the [[preimage]] $f^{-1}(U) \subset K$ is open or closed, respectively.

A topological space $X$ is a **[[compactly generated topological space]]** if each of its compactly closed subspaces is already closed.

Write

$$
  Top_{cg} \hookrightarrow Top
$$

for the [[full subcategory]] of [[Top]] on the compactly generated topological spaces.

=--

Often the condition is added that a compactly closed topological space be also a [[weakly Hausdorff topological space]].

+-- {: .num_example #ExamplesOfCompactlyGeneratedTopologiclSpaces}
###### Example

Examples of [[compactly generated topological spaces]], def. \ref{kTop}, include

* every [[compact space]];

* every [[locally compact space]];

* every [[topological manifold]];

* every [[CW-complex]]; 

* every [[first countable space]]

=--


+-- {: .num_cor #TopologicalRealizationOfSSetLandsInkTop}
###### Corollary

The topological [[geometric realization]] functor of [[simplicial sets]]
in example \ref{TopologicalRealizationOfSimplicialSets} takes values in [[compactly generated topological spaces]]

$$
  {\vert - \vert}
  \;\colon\;
  sSet
  \longrightarrow Top_{cg}
$$

=--

+-- {: .proof}
###### Proof

By example \ref{ExamplesOfCompactlyGeneratedTopologiclSpaces} and prop. \ref{TopologicalRealizationOfsSetLandsInCWComplexes}.

=--

+-- {: .num_prop #kTopIsCoreflectiveInTop}
###### Proposition

The [[subcategory]] $Top_{cg} \hookrightarrow Top$ of def. \ref{kTop} has the following properties

1. It is a [[coreflective subcategory]]

   $$
     Top_{cg} \stackrel{\hookrightarrow}{\underset{k}{\longleftarrow}} Top
     \,.
   $$

   The coreflection $k(X)$ of a topological space is given by adding to the open subsets of $X$ all compactly open subsets, def. \ref{kTop}.

1. It has all small [[limits]] and [[colimits]].

   The colimits are computed in $Top$, the limits are the image under $k$ of the limits as computed in $Top$.

1. It is a [[cartesian closed category]]. 

   The [[cartesian product]] in $Top_{cg}$ is the image under $k$ of the Cartesian product formed in $Top$.

=--

This is due to ([Steenrod 67](compactly+generated+topological+space#Steenrod67)), expanded on in ([Lewis 78, appendix A](compactly+generated+topological+space#Lewis78)). One says that prop. \ref{kTopIsCoreflectiveInTop} with example \ref{ExamplesOfCompactlyGeneratedTopologiclSpaces} makes $Top_{cg}$ a "[[convenient category of topological spaces]]".


+-- {: .num_prop #Timesk}
###### Proposition

Regarded, via corollary \ref{TopologicalRealizationOfSSetLandsInkTop} as a functor ${\vert - \vert} \colon sSet \to Top_{cg}$, [[geometric realization]] 
preserves [[finite limits]].

=--

See at _[Geometric realization is left exact](geometric+realization#GeometricRealizationIsLeftExact)_.

+-- {: .proof}
###### Proof idea

The key step in the proof is to use the [[cartesian closed category|cartesian closure]] of $Top_{cg}$ (prop. \ref{kTopIsCoreflectiveInTop}). This gives that the [[Cartesian product]] is a [[left adjoint]] and hence preserves colimits in each variable, so that the [[coend]] in the definition of the geometric realization may be taken out of Cartesian products. 

=--



+-- {: .num_lemma}
###### Lemma

The [[geometric realization]], example \ref{TopologicalRealizationOfSimplicialSets}, 
of a [[minimal Kan fibration]], def. \ref{MinimalKanFibration} is a [[Serre fibration]], def. \ref{SerreFibration}.

=--

This is due to ([[Calculus of fractions and homotopy theory|Gabriel-Zisman 67]]). See for instance ([Goerss-Jardine 99, chapter I, corollary 10.8, theorem 10.9](#GoerssJardine99)).

+-- {: .proof}
###### Proof idea

By prop. \ref{MinimalKanFibrationAreFiberBundles} minimal Kan fibrations are simplicial [[fiber bundles]], locally trivial over each simplex in the base. By prop. \ref{Timesk} this property translates to their [[geometric realization]] also being a locally trivial [[fiber bundle]] of [[topological spaces]], hence in particular a [[Serre fibration]].

=--

+-- {: .num_prop #GeometricRealizationOfKanFibrationIsSerreFibration}
###### Proposition

The [[geometric realization]], example \ref{TopologicalRealizationOfSimplicialSets}, of any [[Kan fibration]], def. \ref{KanFibration} is a [[Serre fibration]], def. \ref{SerreFibration}.

=--

This is due to ([Quillen 68](Kan+fibration#Quillen68)). See for instance ([Goerss-Jardine 99, chapter I, theorem 10.10](#GoerssJardine99)).




+-- {: .num_prop #UnitOfSingularNerveAndRealizationIsWEOnKanComplexes}
###### Proposition

For $S$ a [[Kan complex]], then the [[adjunction unit|unit]] of the [[nerve and realization]]-[[adjunction]] (prop. \ref{NerveAndRealizationAdjunction}, example \ref{TopologicalRealizationOfSimplicialSets})

$$
  S \longrightarrow Sing {\vert S \vert}
$$

is a [[weak homotopy equivalence]], def. \ref{WeakHomotopyEquivalence}.

For $X$ any [[topological space]], then the [[adjunction counit]] 

$$
  {\vert Sing X\vert} \longrightarrow X
$$

is a [[weak homotopy equivalence]]

=--

e.g. ([Goerss-Jardine 99, chapter I, prop. 11.1 and p. 63](#GoerssJardine99)).

+-- {: .proof}
###### Proof idea

Use prop. \ref{SingDetextsAndReflectsFibrations} and prop. \ref{GeometricRealizationOfKanFibrationIsSerreFibration} applied to the [[path fibration]] to proceed by [[induction]].

=--


## The classical model structure $sSet_{Quillen}$
 {#TheClassicalModelStructure}


+-- {: .num_defn #ClassesOfMorphismsOnsSetQuillen}
###### Definition

The classical model structure on [[simplicial sets]], $sSet_{Quillen}$, has the following distinguished classes of morphisms:

* The classical **weak equivalences** $W$ are the [[simplicial weak equivalences]]: morphisms whose [[geometric realization]], example \ref{TopologicalRealizationOfSimplicialSets}, is a [[weak homotopy equivalence]] of [[topological spaces]];

* The classical **fibrations** $F$ are the **[[Kan fibrations]]**, def. \ref{KanFibration};

* The classical **cofibrations** $C$ are the [[monomorphisms]] of simplicial sets, i.e. the degreewise [[injections]].


=--

## Properties

### Basic properties

+-- {: .num_prop}
###### Proposition

In model structure $sSet_{Quillen}$, def. \ref{ClassesOfMorphismsOnsSetQuillen}, the following holds.

* The fibrant objects are precisely the [[Kan complexes]].

* A morphism $f : X \to Y$ of fibrant simplicial sets / [[Kan complexes]] is a weak equivalence precisely if it induces an [[isomorphism]] on all [[simplicial homotopy groups]], def. \ref{UnderlyingSetsOfSimplicialHomotopyGroups}.

* All simplicial sets are cofibrant with respect to this model structure. 


=--

+-- {: .num_prop}
###### Proposition

The **acyclic fibrations** in $sSet_{Quillen}$(i.e. the maps that are both fibrations as well as weak equivalences) between [[Kan complexes]] are precisely the morphisms $f : X \to Y$ that have the [[right lifting property]] with respect to all inclusions $\partial \Delta[n] \hookrightarrow \Delta[n]$ of boundaries of $n$-simplices into their $n$-simplices
  $$
    \array{
      \partial \Delta[n] &\to& X
      \\
      \downarrow &{}^\exists\nearrow& \downarrow^f 
      \\
      \Delta[n] &\to& Y
    }
    \,.
  $$

=--

This appears spelled out for instance as ([Goerss-Jardine 99, theorem 11.2](#GoerssJardine99)).


In fact:

+-- {: .num_prop}
###### Proposition

$sSet_{Quillen}$ is a [[cofibrantly generated model category]] with

* generating cofibrations the [[boundary]] inclusions $\partial \Delta[n] \to \Delta[n]$;

* generating acyclic cofibrations the [[horn]] inclusions $\Lambda^i[n] \to \Delta[n]$.

=--



+-- {: .num_theorem}
###### Theorem

Let $W$ be the smallest class of morphisms in $sSet$ satisfying the following conditions:

1. The class of monomorphisms that are in $W$ is closed under [[pushout]], [[transfinite composition]], and [[retracts]].
2. $W$ has the [[two-out-of-three]] property in $sSet$ and contains all the [[isomorphisms]].
3. For all natural numbers $n$, the unique morphism $\Delta [n] \to \Delta [0]$ is in $W$.

Then $W$ is the class of weak homotopy equivalences.
=--

+-- {: .proof}
###### Proof

* First, notice that the horn inclusions $\Lambda^0 [1] \hookrightarrow \Delta [1]$ and $\Lambda^1 [1] \hookrightarrow \Delta [1]$ are in $W$.
* Suppose that the horn inclusion $\Lambda^k [m] \hookrightarrow \Delta [m]$ is in $W$ for all $m \lt n$ and all $0 \le k \le m$. Then for $0 \le l \le n$, the horn inclusion $\Lambda^l [n] \hookrightarrow \Delta [n]$ is also in $W$.
* Quillen's [[small object argument]] then implies all the trivial cofibrations are in $W$.
* If $p : X \to Y$ is a trivial Kan fibration, then its right lifting property implies there is a morphism $s : Y \to X$ such that $p \circ s = id_Y$, and the two-out-of-three property implies $s : Y \to X$ is a trivial cofibration. Thus every trivial Kan fibration is also in $W$.
* Every weak homotopy equivalence factors as $p \circ i$ where $p$ is a trivial Kan fibration and $i$ is a trivial cofibration, so every weak homotopy equivalence is indeed in $W$.
* Finally, noting that the class of weak homotopy equivalences satisfies the conditions in the theorem, we deduce that it is the _smallest_ such class.

=--

As a corollary, we deduce that the classical model structure on $sSet$ is the smallest (in terms of weak equivalences) model structure for which the cofibrations are the monomorphisms and the weak equivalences include the (combinatorial) homotopy equivalences.

+-- {: .num_prop}
###### Proposition

Let $\pi_0 : sSet \to Set$ be the connected components functor, i.e. the left adjoint of the constant functor $cst : Set \to sSet$. A morphism $f : Z \to W$ in $sSet$ is a weak homotopy equivalence if and only if the induced map
$$\pi_0 K^f : \pi_0 K^W \to \pi_0 K^Z$$
is a bijection for all _Kan complexes_ $K$.

=--

+-- {: .proof}
###### Proof

One direction is easy: if $K$ is a Kan complex, then axiom SM7 for [[simplicial model categories]] implies  the functor $K^{(-)} : sSet^{op} \to sSet$ is a right [[Quillen functor]], so Ken Brown's lemma implies it preserves all weak homotopy equivalences; in particular, $\pi_0 K^{(-)} : sSet^{op} \to Set$ sends weak homotopy equivalences to bijections.

Conversely, when $K$ is a Kan complex, there is a natural bijection between $\pi_0 K^X$ and the hom-set $Ho (sSet) (X, K)$, and thus by the [[Yoneda lemma]], a morphism $f : Z \to W$ such that the induced morphism $\pi_0 K^W \to \pi_0 K^Z$ is a bijection for all Kan complexes $K$ is precisely a morphism that becomes an isomorphism in $Ho (sSet)$, i.e. a weak homotopy equivalence.

=--

### Properness
 {#Properness}

The Quillen model structure is both left and right [[proper model category|proper]].  Left properness is automatic since all objects are cofibrant.  Right properness follows from the following argument: it suffices to show that there is a functor $R$ which (1) preserves fibrations, (2) preserves pullbacks of fibrations, (3) preserves and reflects weak equivalences, and (4) lands in a category in which the pullback of a weak equivalence along a fibration is a weak equivalence.  For if so, we can apply $R$ to the pullback of a fibration along a weak equivalence to get another such pullback in the codomain of $R$, which is a weak equivalence, and hence the original pullback was also a weak equivalence.  Two such functors $R$ are

* geometric realization $sSet \to Top$, where $Top$ denotes a sufficiently [[convenient category of topological spaces]] (e.g. the category of [[k-spaces]] suffices) and
* $Ex^\infty : sSet \to Kan$, where $Kan$ is the category of [[Kan complexes]].

This may be found, for instance, in II.8.6--7 of [Goerss-Jardine](model+structure+on+simplicial+sets#GoerssJardine).  Another proof may be found in [Moss](model+structure+on+simplicial+sets#Moss), and a different proof of properness may be found in [Cisinski, Prop. 2.1.5](model+structure+on+simplicial+sets#Cisinski06).


### Quillen equivalence with $Top_{Quillen}$

+-- {: .num_theorem}
###### Theorem

The [[singular simplicial complex]]/[[geometric realization]]-[[nerve and realization|adjunction]] of example \ref{TopologicalRealizationOfSimplicialSets}
constitutes a [[Quillen equivalence]] of the classical model structure $sSet_{Quillen}$ of def. \ref{ClassesOfMorphismsOnsSetQuillen} with the  [[classical model structure on topological spaces]]:

$$
  ({\vert -\vert}\dashv Sing)
  : 
  Top_{Quillen}
  \stackrel{\overset{{\vert -\vert}}{\leftarrow}}{\underset{Sing}{\to}}
  sSet_{Quillen}
$$


=--

+-- {: .proof}
###### Proof

First of all, the adjunction is indeed a [[Quillen adjunction]]: prop. \ref{SingDetextsAndReflectsFibrations} says in particular that $Sing(-)$ takes [[Serre fibrations]] to [[Kan fibrations]] and prop. \ref{TopologicalRealizationOfsSetLandsInCWComplexes} gives that ${\vert-\vert}$ sends monomorphisms of simplicial sets to [[relative cell complexes]].

Now prop. \ref{UnitOfSingularNerveAndRealizationIsWEOnKanComplexes} says that the derived adjunction unit and counit are weak equivalences, and hence the Quillen adjunction is a Quillen equivalence.

=--



## Related concepts

* [[model structure on simplicial sets]]

* [[constructive model structure on simplicial sets]]

* [[model structure on reduced simplicial sets]]

* [[classical model structure on topological spaces]]

* [[Quillen adjunction between simplicial sets and connective dgc-algebras]]

## References


The original article is

* {#Quillen67} [[Dan Quillen]], chapter II, section 3 of _[[Homotopical Algebra]]_, Lecture Notes in Mathematics __43__, Springer-Verlag 1967, iv+156 pp.

The proof there is purely combinatorial (i.e. does not use topological spaces): he uses the theory of [[minimal Kan fibrations]], the fact that the latter are [[fiber bundles]], as well as the fact that the [[classifying space]] of a [[simplicial group]] is a [[Kan complex]]. This proof has been rewritten several times in the literature: 

* {#JoyalTierney05} [[André Joyal]], [[Myles Tierney]] _An introduction to simplicial homotopy theory_, 2005 ([chapter I](http://hopf.math.purdue.edu/cgi-bin/generate?/Joyal-Tierney/JT-chap-01), more notes [pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern47.pdf))

A proof (in fact two variants of it) using the [[Kan fibrant replacement]] $Ex^\infty$ functor is given 

* {#Cisinski06} [[Denis-Charles Cisinski]], section 2 of _[[joyalscatlab:Les préfaisceaux comme type d'homotopie]]_, Ast&#233;risque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf))
 

which discusses the topic as a special case of a _[[Cisinski model structure]]_.


The fun part is not that much about the existence of model structure, but to prove that the fibrations are precisely the [[Kan fibrations]] (and also to prove all the good properties of $Ex^\infty$ without using topological spaces); for two different proofs of this fact using $Ex^\infty$, see Prop. 2.1.41 as well as Scholium 2.3.21 for an alternative). For the rest, everything was already in the book of [[Gabriel and Zisman]], for instance.

Another approach also using $Ex^\infty$ is in

* {#Moss} Sean Moss, _Another approach to the Kan-Quillen model structure_, [arXiv](http://arxiv.org/abs/1506.04887).

A standard textbook references for the classical model structure is

* {#GoerssJardine99} [[Paul Goerss]], [[Rick Jardine]], chapter  1 of _[[Simplicial homotopy theory]]_, Birkh&#228;user 1999, 2009 ([ps](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html)).

A proof of the model structure not relying on the [[classical model structure on topological spaces]] nor on explicit models for [[Kan fibrant replacement]] is givn in 

* [[Christian Sattler]], _The Equivalence Extension Property and Model Structures_ ([arXiv:1704.06911](https://arxiv.org/abs/1704.06911))


[[!redirects Quillen model structure on simplicial sets]]
[[!redirects Kan-Quillen model structure on simplicial sets]]
[[!redirects Kan-Quillen model structure]]

[[!redirects classical model category of simplicial sets]]




