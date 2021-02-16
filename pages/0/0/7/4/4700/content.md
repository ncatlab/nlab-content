
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

A _graph complex_ is a certain [[cochain complex]] [[linear span|spanned]] by [[equivalence classes]] of certain labeled [[directed graphs]], whose [[differential]] encodes the operation of contracting away [[edges]] in a graph.

Two similar but different classes of examples are usually referred to by default as just "the graph complex", going back to hints in [Kontsevich 92, P. 11-12](#Kontsevich92), [Kontsevich 93, 5](#Kontsevich93):

Given a [[smooth manifold]] $\Sigma$, often taken to be [[Euclidean space]] $\mathbb{R}^D$, there is

1. a [graph complex model for the real cohomology of the unlabeled ordered configuration space of points](#IdeaGraphComplexModelsForConfigurationSpacesOfPoints) in $\Sigma$

1. a [graph complex model for the real cohomology of the space of knots](#IdeaGraphComplexModelForSpacesOfKnots) in $\Sigma$.

In both cases, the graphs are interpreted as [[Feynman diagrams]] for [[Chern-Simons theory]] and the map which identifies these with [[cocycles]] in [[real cohomology]] of either the (unlabeled & ordered) [[configuration space of points]] or the [[space of knots]] is given by sending a Feynman diagram to its [[Feynman amplitude]]. In the first case this is an [[n-point function]], [[correlator as differential form on configuration space of points|regarded as a differential form on the configuration space]] of $n$-points, while in the second case this is a [[vacuum amplitude]] depending on the [[isotopy]] [[equivalence class|class]] of the  [[Wilson loop]] encoded by the [[knot]] -- a [[Vassiliev knot invariant]].

\linebreak

**Beware** that these graph complex models **differ only in very small technical detail** as the manifold $\Sigma$ varies and the choice between models for configuration space of points or spaces of knots is made (see the [Overview of definitions](#OverviewOfDefinitions) below), and yet these small details **completely change the cohomological nature** of the resulting graph complexes; a point not often made manifest when any given author discusses  "the graph complex".

\linebreak


### Model for ordered configuration spaces of points
 {#IdeaGraphComplexModelsForConfigurationSpacesOfPoints}


The graph complex model for unlabeled & ordered [[configuration spaces of points]] was originally sketched in [Kontsevich 92 (p. 11-12)](#Kontsevich92) and worked out in detail in [Lambrechts-Volić 14](#LambrechtsVolic14) for $\Sigma = \mathbb{R}^D$ a [[Euclidean space]]. Other authors have claimed generalization to $\Sigma$ a [[closed manifold]] ([Campos-Willwacher 16](#CamposWillwacher16)) possibly [[manifold with boundary|with boundary]] ([Campos-Idrissi-Lambrechts-Willwacher 18](#CamposIdrissiLambrechtsWillwacher18)).

Here we denote this version of the graph complex by "$Graphs$", in contrast to "$KnotGraphs$" for the other model, discussed further [below](#IdeaGraphComplexModelForSpacesOfKnots).


<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/AGraphInTheGraphComplexII.jpg" width="160">
</div>



This graph complex is [[linear span|spanned]] by [[finite set|finite]] [[directed graphs]] with [[linear order|linearly ordered]] internal and external [[vertices]], subject to a sign rule reflecting the [[orientation]] of [[edges]]. The [[differential]] sends any graph to a signed sum of graphs obtained by contracting one of the [[edges]] with at least one internal vertex. 

Under ordered disjoint union of edges and _internal_ vertices this [[cochain complex]] becomes a [[differential graded-commutative algebra]]

$$
  Graphs_n\big( \mathbb{R}^D \big)
  \;\in\;
  dgcAlg_{\mathbb{R}}
  \phantom{AA}
  n, D \in \mathbb{N}
  \,,
$$

As such, this is [[quasi-isomorphism|quasi-isomorphic]] to the semi-algebraic [[de Rham algebra]]


$$
  \Omega^\bullet
  \big(
    \underset{{}^{1,\cdots,n}}{Conf}
    \big( 
      \Sigma
    \big)
  \big)
  \;\in\;
  dgcAlg_{\mathbb{R}}
  \phantom{AA}
  n, D \in \mathbb{N}
$$

of the [[Fulton-MacPherson compactification]] of the [[configuration space of points]] $\underset{{}^{1,\cdots,n}}{Conf}(\mathbb{R}^D)$ for $n$ points in $D$-dimensional [[Euclidean space]].

The [[chain map]] which exhibits this [[quasi-isomorphism]] is given by regarding a graph as a [[Feynman diagram]] for [[Chern-Simons theory]] on $\Sigma = \mathbb{R}^D$ and sending it to its corresponding [[Feynman amplitude]], namely to the [[configuration space of points|configuration space]]-[[integral]] of the [[wedge product]] of [[Chern-Simons propagators]] associated to the [[edges]], regarding [[Feynman amplitudes as differential forms on configuration spaces of points]]: 

\[
  \label{TheQuasiIsomorphism}
  \underset{
    \color{blue}
    \array{
      \phantom{A}
      \\
      \text{graph complex}
      \\
      \text{of n-point Feynman diagrams}
      \\
      \text{for Chern-Simons theory}
      \\
      \text{on} \; \Sigma 
    }
  }{
    Graphs_n(\Sigma)
  }
  \underoverset{
    \simeq_{\mathrlap{qi}}
  }
  {
    \color{blue}
    \array{
      \text{assign Feynman amplitudes}
      \\
      \text{of Chern-Simons theory}
      \\
      \phantom{A}
    }
  }
  {
    \longrightarrow
  }
  \underset{
    \color{blue}
    \array{
      \phantom{A}
      \\
      \text{de Rham algebra of}
      \\
      \text{ordered configuration space}
      \\
      \text{of n points in}\; \Sigma
    }
  }{
  \Omega^\bullet
  \big(
    \underset{{}^{ \{1,\cdots,n \} }}{Conf}\big(  \Sigma \big)
  \big)
  }
  \,.
\]

This means that for each [[edge]] in a [[graph]] a [[Chern-Simons propagator]] is assigned, and for each of $n_{int} \in \mathbb{N}$ internal [[vertices]] the [[wedge product]] of its adjacent [[Chern-Simons propagators]] is [[fiber integral|fiber integrated]] along the canonical [[fibration]] of [[configuration spaces of points]]:

$$
  \underset{
    {}^{\{1, \cdots, n + n_{int} \}}
  }{
    Conf
  }
  \big(
    \mathbb{R}^D 
  \big)
  \longrightarrow
  \underset{
    {}^{\{1,\cdots,n\}}
  }{
    Conf
  }
  \big( 
    \mathbb{R}^D 
  \big)
$$

just as befits the definition of a [[Feynman amplitude]] when [[correlator as differential form on configuration space of points|regarding them as differential forms on configuration spaces of points]].


\linebreak

### Model for spaces of knots  
 {#IdeaGraphComplexModelForSpacesOfKnots}

The graph complex model for [[spaces of knots]] was originally sketched in [Kontsevich 93, Section 5](#Kontsevich93) and worked out in [Cattaneo, Cotta-Ramusino, Longoni 02](#CattaneoCottaRamusinoLongoni02), [05](#CattaneoCottaRamusinoLongoni05), see also [Bar-Natan 91](#BarNatan91).

Here we denote this version of the graph complex by "$KnotGraphs$", in contrast to "$Graphs$" for the other model, discussed [above](#IdeaGraphComplexModelsForConfigurationSpacesOfPoints).

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/AKnotGraphInTheKnotGraphComplexII.jpg" width="190">
</div>


The explicit definition is almost exactly the same as that of the model for configuration spaces of points [above](#IdeaGraphComplexModelsForConfigurationSpacesOfPoints), except that the external vertices here have a degree -1 instead of 0, and that the differential sees contractible [[edges]] between consecutive external vertices, often called _arcs_, shown by dashed lines on the right.

Together these two innocent modifications make the graphs now represent [[vacuum amplitude|vacuum]] [[Feynman diagrams]] for [[Chern-Simons theory]] in the presence of a [[Wilson loop]], with the external vertices now attached to this [[knot]] (corresponding to the dashed line shown on the right):

\[
  \label{KnotGraphsTheQuasiIsomorphism}
  \underset{
    \color{blue}
    \array{
      \phantom{A}
      \\
      \text{graph complex}
      \\
      \text{of n-point Feynman diagrams}
      \\
      \text{for Chern-Simons theory}
      \\
      \text{on} \; \Sigma 
      \\
      \text{in the presence of a Wilson loop knot}
    }
  }{
    KnotGraphs_n(\Sigma)
  }
  \underoverset{
  }
  {
    \color{blue}
    \array{
      \text{assign Feynman amplitudes}
      \\
      \text{of Chern-Simons theory}
      \\
      \phantom{A}
    }
  }
  {
    \longrightarrow
  }
  \underset{
    \color{blue}
    \array{
      \phantom{A}
      \\
      \text{de Rham algebra}
      \\
      \text{of the space of knots}
      \\
      \text{in}\; \Sigma
      \\
      \text{(higher Vassiliev knot invariants)}
    }
  }{
  \Omega^\bullet
  \big(
    Emb(S^1,  \Sigma \big)
  \big)
  }
  \,.
\]


This yields higher [[Vassiliev knot invariants]], a good review is in [Volić 13](#Volic13). It is a [[conjecture]] ([Volić 13, Conjecture 4.8](#Volic13)) that this map, too, is a [[quasi-isomorphism]].

\linebreak

### Model for other spaces

There are yet other, inequivalent, graph complexes. Notably there is a type of graph complex whose (co)homology in degree 0 is the [[Lie algebra]] of the [[Grothendieck-Teichmüller group]] ([Willwacher 10](#Willwacher10), [Dolgushev-Rogers 12](#DolgushevRogers12)), and this is neither of the above two cases. (...)



## Definition
 {#GraphComplex}

### Overview
 {#OverviewOfDefinitions}

There are two different classes of (Kontsevich-) graph complexes, modelling the [[real cohomology]] of, respectively,

| [[configuration space]]   |    |   |  [[graph complex]]  |  |
|----|----|---|----|--|
| [[configuration spaces of points]] | $\underset{{}^{1,\cdots,n}}{Conf}(\Sigma)$ | $\;\;\leftrightarrow\;\;$ | $Graphs_n(\Sigma)$ |  [(1)](#GraphComplexesModellingConfigurationSpacesOfPoints) |  
| [[spaces of knots]] | $Emb(S^1,\Sigma)$ | $\;\;\leftrightarrow\;\;$ | $KnotGraphs(\Sigma)$ | [(2)](#GraphComplexesModellingSpacesOfKnots) |

Despite their very deifferent cohomological nature, the explicit definitions of these two kinds of graph complexes are mostly identical, except for some small but crucial difference in the definition of degrees and labels of edges (see [below](#KnotGraphsDefinition)).

In addition, the definition of the graph complex model for configuration spaces of points depends on a choice of [[smooth manifold]] $\Sigma$, possibly [[manifold with boundary|with boundary]], namely such that the graph complex $Graphs(\Sigma)$ provides a model for the cohomology of the [[configuration space of points]] in $\Sigma$

$$
  Graphs\big( \Sigma \big)
  \leftrightarrow
  \Omega^\bullet\big(  Conf(\Sigma) \big)
  \,.
$$

The [[configuration spaces of points]] are naturally [[filtering|filtered]] by [[subspaces]] of a fixed number $n \in \mathbb{N}$ of points. In the graph complexes this correpsonds to graphs with a fixed number $n$ of _external_ vertices:


$$
  \underset{
    \mathclap{
    \color{blue}
    \array{
       \phantom{A}
       \\
       \text{graphs with}
       \\
        n\;\text{external vertices}
    }
    }
  }{
    Graphs_n\big( \Sigma\big)
  }
  \;\;\;\leftrightarrow\;\;\;
  \Omega^\bullet\big(
     \underset{
       \mathclap{
       \color{blue}
       \array{
         \phantom{A}
         \\
         \text{configuration space}
         \\
         \text{of}\;n\;\text{points}
       }
       }
     }{  
       \underbrace{
         \underset{{}^{1,\cdots,n}}{Conf}(\Sigma) 
       }
     }
  \big)
  \,.
$$

The full graph complexes/configuration spaces are just the [[direct sum]]/[[union]] of those for fixed number $n$ of external vertices/points, hence one may focus attention on the latter.

The precise form of these relations is the content of the theorems discussed below. Before stating this in detail, we make some general remarks on how the situation depends on $\Sigma$:


Beware that the graphs $[\Gamma] \in Graphs_n(\Sigma)$ themselves are _not_ going to carry an embedding into the manifold $\Sigma$, they are just abstract graphs. But the construction of the above correspondence to the cohomology of the configuration space of points is given by associating with a graph the corresponding [[correlator as differential form on configuration space of points|correlator]] in a [[Chern-Simons theory|Chern-Simons]] [[perturbative quantum field theory]] on the space $\Sigma$.

As a consequence, the dependence of the graph complexes themselves on $\Sigma$ is mild:

In particular, in the case that $\Sigma = \mathbb{R}^D$ is a [[Euclidean space]], the corresponding graph complexes $Graphs\big( \mathbb{R}^D \big)$ depend essentially only on whether the [[dimension]] $D$ is [[even number|even]] or [[odd number|odd]]. Concretely, the degree of a graph in the [[graded vector space]] $Graphs_n(\mathbb{R}^D)$ is

\[
  \label{DegreeOfAGraph}
  deg\big( [\Gamma]\big) 
  \;=\;
  (D-1) \cdot \#\!Edges - D \cdot \#\!Vertices_{int}
  \,,
\]

hence each [[edge]] contributes a degree $D-1$ and each internal vertex a degree $-D$. As a consequence,  due to the [[signs in supergeometry|sign rule]] in the [[graded-commutative algebra]] [[structure]] on $Graphs_n(\mathbb{R}^D)$ we have the following parities

|   $\Sigma = \mathbb{R}^D$ | edges | internal vertices |
|-------------------|-------|-------------------|
| $D$ even |  odd  | even |
| $D$ odd  | even | odd | 

Up to an absolute _even_ change of grading, the graph complexes $Graphs_n(\mathbb{R}^D)$ depend only on these parities, hence depend only on whether $D$ is [[even number|even]] or [[odd number|odd]].
 
Finally, beware that many authors consider the case where $\Sigma = \mathbb{R}^D$ by default, and don't mention a dependence on a choice of manifold, but just on a natural number $D$. This natural number is then often denoted "$d$" or "$n$".

For instance:

* the "graph complex with anti-symmetric set of edges" of [Bar-Natan & McKay, Def. 3.3](#BarNatanMcKay) is denoted $GC_2$ in [Willwacher 10](#Willwacher10) and is our $Graphs_0\big(\mathbb{R}^2\big)$;

* similarly $GC_3$ in [Koroshkin-Willwacher-Živković 14](#KoroshkinWillwacherZivkovic14) is our $KnotGraphs\big( \mathbb{R}^3\big)$.

(While the cohomology of $Graphs_0(\Sigma)$ -- being equivalent to that of $Conf_0(\Sigma) \simeq \ast$ -- is trivial, these authors consider further filtrations which have non-trivial cohomology in filtration stages, see [Bar-Natan & McKay, Def. 3.6](#BarNatanMcKay)).



\linebreak

### **1)** Graph complexes modelling configuration spaces of points
 {#GraphComplexesModellingConfigurationSpacesOfPoints}

We discuss graph complexes $Graphs_n(\Sigma)$ modelling the [[real cohomology]] of [[configuration spaces of points]] $\underset{{}^{1,\cdots,n}}{Conf}(\Sigma)$. 

For the case of $\Sigma = \mathbb{R}^D$ these were originally hinted at in [Kontsevich 92 (p. 11-12)](#Kontsevich92) and discussed in detail in [Lambrechts-Volić 14](#LambrechtsVolic14).

\linebreak

#### $Graphs_n\big( \mathbb{R}^3 \big)$
{#GraphComplexForConfigurationsOfPointsInR3}


We state the definition of the graph complexes $Graphs_n\big( \mathbb{R}^3\big)$ (as motivated [above](#IdeaGraphComplexModelsForConfigurationSpacesOfPoints), see Def. \ref{GraphComplexDgcAlgebra} below) associated with [[Euclidean space]] of [[dimension]] 3, following [Lambrechts-Volić 14, Section 6](#LambrechtsVolic14).


##### Graphs

+-- {: .num_defn #Graphs}
###### Definition
**(graphs)**

In the following, by a **[[graph]]** we mean specifically:

1. a [[finite set|finite]] [[directed graph]] 

   $$
     Edg \underoverset{t}{s}{\rightrightarrows} Vert
     \,,
   $$

1. a decomposition  of the [[finite set]] $Vert$ of [[vertices]] as a [[disjoint union]]

   $$
     Vert \simeq Vert_{ext} \sqcup Vert_{int}
   $$

   of "external" and "internal" vertices.

1. a [[linear order]] on $Vert$, such that $Vert_{ext} \lt Vert_{int}$.

Hence both $Vert_{ext}$ and $Vert_{int}$ are [[linear orders]], and 

$$
  Vert = Vert_{ext} \sqcup_{{}_{\lt}} Vert_{int}
$$

is their ordered [[disjoint union]].

An [[isomorphism]] $\Gamma \simeq \Gamma'$ of such graphs is a [[pair]] of [[bijections]] between sets of edges and vertices

\[
  \label{IsomorphismOfGraphs}
  \array{
    Edg &\underoverset{t}{s}{\rightrightarrows}& Vert_{ext} \sqcup Vert_{int}
    \\
    \mathllap{{}^{\simeq}}\big\downarrow
    &&
    \mathllap{{}^{\simeq}}\big\downarrow
    \\
    Edg' &\underoverset{t'}{s'}{\rightrightarrows}& Vert'_{ext} \sqcup Vert'_{int}
  }
\]

which respects all [[structure]], hence the [[source]] and [[target]] maps, the decomposition into external and internal vertices, and the [[linear order]].


=--

([Lambrechts-Volić 14, Def. 6.1](#LambrechtsVolic14))


+-- {: .num_remark #EmptyGraph}
###### Remark
**([[empty graph]])**

The [[empty graph]] counts as a graph, according to Def. \ref{Graphs}.

=--


We write $\#\! Vert \coloneqq \left\vert Vert \right\vert$ for the [[cardinality]] of the sets of vertices, etc.


+-- {: .num_defn #DenotationForLinearOrderOnVertices}
###### Remark
**(denotation for linear order on vertices)**

The  [[linear order]] on the [[vertices]] in Def. \ref{Graphs} is equivalently a choice of [[bijection]] of $Vert$ with the set of the first $\#\!Vert$ [[natural numbers]]

\[
  \label{NaturalNumberLabelsOfVertices}
  Vert
  \;\simeq\;
  \big\{
    1, 2, \ldots, \# Vert_{ext}, \# Vert_{ext} + 1, \ldots , \# Vert_{ext} + \# Vert_{int}
  \big\}
\]

With this understood, we may depict graphs as as diagrams with oriented edges and numbered vertices.

=--



+-- {: .num_defn #DegreeOfAGraph}
###### Definition
**(degree of a graph)**

Given a graph 

$$
  \Gamma
  \;=\;       
  \big(
    Edg 
      \underoverset{t}{s}{\rightrightarrows} 
    Vert_{ext} 
      \sqcup
    Vert_{int}
  \big)
$$

according to Def. \ref{Graphs}, its _degree_ is the [[natural number]]

$$
  deg(\Gamma)
  \;\coloneqq\;
  2 \cdot \#\!Edg
  -
  3 \cdot \#\!Vert_{int}
  \,,
$$

hence the sum of 2 for each [[edge]] and of -3 for each internal [[vertex]].

=--

([Lambrechts-Volić 14, Def. 6.6](#LambrechtsVolic14))


If we also agree to

1. denote internal vertices by a bullet;

1. denote external vertices by... _no_ denotation (as usual for [[Feynman diagrams]]!)

then the ingredients of these graphs are as shown in the following figure:

<center>
<img src="https://ncatlab.org/nlab/files/GraphComplexIngredients.jpg" width="880">
</center>

The following shows some very simple examples of graphs, depicted this way:


<center>
<img src="https://ncatlab.org/nlab/files/SomeExamplesOfGraphs.jpg" width="610">
</center>

**Beware** that graphs need not be [[planar graph|planar]], may have edges between two external vertices (chords) and other effects not seen in these simple examples (... need to draw more generic examples...). 

In particular, graphs may have [[tadpoles]]. But the next definition makes such graphs vanish in the graph complex:

+-- {: .num_defn #SignRulesForGraphs}
###### Definition
**(sign rules for graphs)**

For a fixed [[finite set|finite]] [[linear order]] $Vert_{ext} \simeq \{1, 2, \cdots, \#\!Vert_{ext}\}$, consider the [[real numbers|real]] [[linear span]] on the [[set]] of [[isomorphism classes]] (eq:IsomorphismOfGraphs) of graphs, according to Def. \ref{Graphs}, with that set of external [[vertices]]:

\[
  \label{LinearSpanOfIsoClassesOfGraphs}
  \mathbb{R}
  \Big[
    \big\{
     Edg 
      \underoverset{t}{s}{\rightrightarrows} 
     Vert_{ext} 
      \sqcup
     Vert_{int}
     \;\vert\;
     Vert_{int} \in FinLinOrd
    \big\}_{/\sim}
  \Big]
  \;\in\;
  Vect_{\mathbb{R}}
  \,.
\]

The degree associated with a graph (Def. \ref{DegreeOfAGraph}) makes this a [[graded vector space]].

On this [[real vector space]], consider the linear [[equivalence relation]]  $\sim$ generated by 


\[
  \label{SignFromOrientationReversal}
  \Gamma
  \;\sim\;
  -\Gamma'
  \phantom{AA}
  \array{
    \text{if}\;\Gamma'\; \text{is}\;\Gamma\;\text{with}
    \\
    \text{orientation of one edge reversed}
  }
\]


<center>
<img src="https://ncatlab.org/nlab/files/GraphComplexSignsFromOrientationReversal.jpg" width="400">
</center>



and


\[
  \label{SignRuleFromOrderingInternalVertices}
  \Gamma
  \;\sim\;
  -\Gamma'
  \phantom{AA}
  \array{
    \text{if}\;\Gamma'\;\text{is}\;\Gamma\;\text{with}
    \\
    \text{a pair of consecutive internal vertices transposed}
  }
\]


=--

([Lambrechts-Volić 14, Def. 6.5 & Def. 6.5](#LambrechtsVolic14))

Since this [[equivalence relation]] is linear, the set of its [[equivalence classes]] is still a [[vector space]], and since the equivalence relation also preserves the degrees (Def. \ref{DegreeOfAGraph}), it is still a [[graded vector space]]:


+-- {: .num_defn #GradedVectorSpaceOfGraphs}
###### Definition
**(graded vector space of graphs)**

For $n \in \mathbb{N}$, $n \coloneqq \#\! Vert_{ext}$, we write


\[
  \label{VectorSpaceOfGraphsWithSignRulesImposed}
  \widehat{Graphs}_n\big(\mathbb{R}^3\big)
  \;\coloneqq\;
  \mathbb{R}
  \Big[
    \big\{
     Edg 
      \underoverset{s}{t}{\rightrightarrows} 
     Vert_{ext} 
      \sqcup
     Vert_{int}
     \;\vert\;
     Vert_{int} \in FinLinOrd
    \big\}_{/\sim}
  \Big]_{/\sim}
  \;\in\;
  Vect_{\mathbb{R}}
  \,.
\]

for the [[real vector space|real]] [[graded vector space]] of [[equivalence classes]] under the sign rules (eq:SignFromOrientationReversal) and (eq:SignRuleFromOrderingInternalVertices) in the [[linear span]] (eq:LinearSpanOfIsoClassesOfGraphs) of the [[isomorphism classes]] of graphs (Def. \ref{Graphs}) with $n$ external vertices.

For $\Gamma$ any graph, we write 

\[
  \label{EquivalenceClassOfAGraphForSignRules}
  \big[ \Gamma \big]
  \;\in\;
  \widehat{Graphs}_n\big(\mathbb{R}^3\big)
  \,.
\]

for the [[equivalence class]] of the element in this [[real vector space|real]] [[graded vector space]] that it represents. 

When there is not risk of confusion, we will still refer to this equivalence class $[\Gamma]$ as a _graph_.

=--



A further [[quotient space]] $Graphs_n(\mathbb{R}^3)$ of $\widehat Graphs_n(\mathbb{R}^3)$ (eq:VectorSpaceOfGraphsWithSignRulesImposed) will underly the actual graph complex [below](#TheGraphComplex).



+-- {: .num_example #GraphsWithDirectLoopsVanish}
###### Example
**(no tadpoles)**

A direct consequence of quotienting out the [[equivalence relation]]
(eq:SignFromOrientationReversal)
is that graphs with "[[tadpoles]]", namely with edges
that have coinciding [[source]] and [[target]] [[vertex]], 
vanish in $\widehat Graphs_n(\mathbb{R}^3)$ (eq:VectorSpaceOfGraphsWithSignRulesImposed):

$$
  e \in Edg_\Gamma
  \;\text{s.t.}\;
  s(e) = t(e)
  \phantom{AA}
  \Rightarrow
  \phantom{AA}
  \big[ \Gamma \big]
  \;=\;
  0
$$

(This holds more generally for all $\mathbb{R}^D$ with odd $D  = 2k + 1$.)

<center>
<img src="https://ncatlab.org/nlab/files/GraphsWithDirectLoopsVanishInTheGraphComplex.jpg" width="700">
</center>

=--

+-- {: .num_example #TrivalenGraphs}
###### Example
**(trivalent graphs)**

A graph without external vertices has degree (Def. \ref{DegreeOfAGraph}) equal to zero precisely if all its vertices (which are all internal, by assumption) are trivalent:

$$
  \#\!Verts_{ext} = 0
  \;\;\Rightarrow\;\;
  \big(
     deg(\Gamma) = 0
     \;\;\Leftrightarrow\;\;
     \text{all vertices are trivalent}
  \big)
  \,.
$$

The following is the smallest example of such a trivalent graph:

<center>
<img src="https://ncatlab.org/nlab/files/TheDegreeZeroGraph.jpg" width="240">
</center>

Hence in general, the degree of a trivalent graph is three times its number of external vertices:

$$
  \Gamma 
  \;
  \text{trivalent}
  \;\;\;\Rightarrow \;\;\;
  deg\big( [\Gamma] \big)
  \;=\;
  3 \cdot \#\!Verts_{ext}
  \,.
$$

(Because such a graph is the result of taking a trivalent graph in degree 0 and replacing internal vertices of degree -3 with external vertices of degree 0.)

For example, the following graph, obtained from the above trivalent graph by replacing the three internal vertices labeled 1,2 and 3 with external vertices, is of degree $3 \cdot 3 = 9$:

<center>
<img src="https://ncatlab.org/nlab/files/ATrivalentGraphOfDegree9.jpg" width="240">
</center>


=--






\linebreak

##### The algebra of graphs

+-- {: .num_defn #WedgeProductOfGraphs}
###### Definition
**(wedge product of graphs)**

For 

$$
  [\Gamma_1], [\Gamma_2]
  \;\in\;
  \widehat Graphs_n\big( \mathbb{R}^D\big)
$$ 

two equivalence classes (eq:VectorSpaceOfGraphsWithSignRulesImposed) of isomorphism classes of graphs (Def. \ref{GradedVectorSpaceOfGraphs}) with the same number of external, their _wedge product_ is the element

$$
  [\Gamma_1] \wedge [\Gamma_2]
  \coloneqq
  [\Gamma_1 \wedge \Gamma_2]
  \;\in\;
  \widehat Graphs_n\big( \mathbb{R}^D\big)
$$ 

represented by the graph (Def. \ref{Graphs}) which is given by the [[disjoint union]] of [[linear orders]] of edges and _internal_ vertices

$$
  \Gamma_1 \wedge \Gamma_2
  \;\coloneqq\;
  \Big(
    Edgs_{\Gamma_1}
    \sqcup_{{}_{\lt}}
    Edgs_{\Gamma_2}
    \underoverset{t_1 \sqcup_{\lt} t_2}{s_1 \sqcup_{\lt} s_2}{\rightrightarrows}
    Vert_{ext}
    \sqcup_{{}_{\lt}}
    \big(    
      Vert_{int,1}
      \sqcup_{{}_{\lt}}
      Vert_{int,2}
    \big)
  \Big)
  \,.
$$


=--

([Lambrechts-Volić 14, 6.3](#LambrechtsVolic14))

It is immediate that:

+-- {: .num_defn #GradedCommutativeAlgebraOfGraphs}
###### Lemma
**(graded commutative algebra of graphs)**

For $n \in \mathbb{N}$, the [[graded vector space]] $\widehat Graphs_n\big( \mathbb{R}^3\big)$ (eq:VectorSpaceOfGraphsWithSignRulesImposed) of graphs  (Def. \ref{GradedVectorSpaceOfGraphs}) equipped with the wedge product of graphs from Def. \ref{WedgeProductOfGraphs}

$$
  \array{
    \widehat{Graphs}_n(\mathbb{R}^3)
    \otimes
    \widehat{Graphs}_n(\mathbb{R}^3)
    &\overset{\wedge}{\longrightarrow}&
    \widehat{Graphs}_n(\mathbb{R}^3)
    \\
    \big(
      [\Gamma_1], [\Gamma_2]
    \big)
    &\mapsto&
    [\Gamma_1 \wedge \Gamma_2]
  }
$$

is a [[graded-commutative algebra]].

=--










\linebreak


##### The differential on graphs
 {#TheDifferential}

The [[differential]] on the graded vector space of equivalence classes of graphs (eq:VectorSpaceOfGraphsWithSignRulesImposed) is defined in terms of contraction of certain edges in the graph (Def. \ref{ContractionOfAnEdge} below). For this we first say which edges count as _contractible_ (Def. \ref{ContractibleEdges}) and which sign is picked up when contracting them (Def. \ref{SignOfAContractibleEdge}):

+-- {: .num_defn #ContractibleEdges}
###### Definition
**(contractible edges)**

Given a graph  $\Gamma$ (Def. \ref{Graphs}) we say that an [[edge]] $e \in Edg_\Gamma$ is a _contractible edge_ if the following conditions hold:

1. $e$ is not a [[tadpole]] (Example \ref{GraphsWithDirectLoopsVanish}):

   $$
     s(e) \neq t(e)
   $$ 

1. $e$ has at least one internal vertex:

   $$  
     s(e) \in Vert_{int} 
     \phantom{AA}
     \text{or}
     \phantom{AA}
     t(e) \in Vert_{int} 
   $$


1. every internal vertex of $e$ is connected to more than just one other vertex, i.e. $e$ is _not_ a solid arrow in a diagram of the following form

<center>
<img src="https://ncatlab.org/nlab/files/DeadEndsInGraphComplex.jpg" width="570">
</center>


We write

\[
  \label{SetOfContractibleEdges}
  Edg^{contr}_\Gamma
  \;\subset\;
  Egd_\Gamma
\]

for the [[subset]] of the contractible edges inside all edges of a graph $\Gamma$.


=--

([Lambrechts-Volić 14, p. 60](#LambrechtsVolic14))

+-- {: .num_defn #ContractionOfAnEdge}
###### Definition
**(contraction of an edge)**

Given a graph $\Gamma$ (Def. \ref{Graphs}) and a contractible edge $e \in Edg_\Gamma$ (Def. \ref{ContractibleEdges}) consider the induced graph obtained by removing that edge and the one of its vertices with the larger label

$$
  \Gamma / e
  \;\coloneqq\;
  \big(
    Edg_\Gamma
    \setminus \{e\}
  \big)
  \underoverset{q \circ t}{q \circ s}{\rightrightarrows}
  \big(
    Vert_\Gamma
    \setminus \{ max(s(e),t(e))  \}
  \big)
$$

and connecting all edges previously attached with the removed vertex to the remaining vertex of that edge (ie. the one with the smaller label):

$$
  \array{
    Vert_\Gamma &\overset{}{\longrightarrow}& Vert_{\Gamma/e}
    \\
    v &\mapsto& 
   \left\{
    \array{
       min(s(e),t(e)) &\vert& \text{if}\; v = max(s(e),t(e))
       \\
       v &\vert& \text{otherwise}
    }
   \right.
  }
$$

=--

([Lambrechts-Volić 14, Def. 6.9](#LambrechtsVolic14))


+-- {: .num_defn #SignOfAContractibleEdge}
###### Remark
**(sign of a contractible edge)**

Given a _contractible edge_ $e \in Egd_\Gamma$ (Def. \ref{ContractibleEdges}) in some graph $\Gamma$ (Def. \ref{Graphs}) we associate a sign as follows:

$$
  \epsilon(e)
  \;\coloneqq\;
  \left\{
  \array{
    (-1)^{ t(e) } &\vert& t(e) \gt s(e)
    \\
    -(-1)^{s(e)} &\vert& s(e) \gt t(e)
  }
  \right.
  \,,
$$

where on the right we are identifying the [[linear order]] on the vertices with their [[natural number]]-labels as in (eq:NaturalNumberLabelsOfVertices).


=--

([Lambrechts-Volić 14, p. 65](#LambrechtsVolic14))


+-- {: .num_defn #DifferentialOnGraphs}
###### Definition
**(differential on graphs)**

For $Vert_{ext}$ a fixed [[finite set|finite]] [[linear order]] of $n = \#\! Vert_{ext}$ external vertices, define on the [[graded vector space]] 
$\widehat Graphs_n\big( \mathbb{R}^3\big)$ (eq:VectorSpaceOfGraphsWithSignRulesImposed) a [[linear map|linear]] [[endomorphism]] $d$ given on the class $[\Gamma]$ \eqref{EquivalenceClassOfAGraphForSignRules} of a graph $\Gamma$ (Def. \ref{Graphs}) by the [[linear combination]] of all its edge contractions $\Gamma/e$ (Def. \ref{ContractionOfAnEdge}) for all contractible edges (Def. \ref{ContractibleEdges}) weighted by their sign (Def. \ref{SignOfAContractibleEdge}):

$$
  \array{
    \widehat Graphs_n\big( \mathbb{R}^3\big)
    &\overset{d}{\longrightarrow}&
    \widehat Graphs_n\big( \mathbb{R}^3\big)
    \\
    [\Gamma]
    &\mapsto&
    \underset{ e \in Edg^{contr}_\Gamma }{\sum}
    \epsilon(\Gamma) \cdot [\Gamma/e]
  }
  \,.
$$

=--

([Lambrechts-Volić 14, (84) ](#LambrechtsVolic14))

+-- {: .num_example #DifferentialOnLinearGraph}
###### Example
**(differential of propagator graph vanishes)**

The differential from Def. \ref{DifferentialOnGraphs}
vanishes on all graphs without any internal vertices (since these have no contractible edges in the sense of Def. \ref{ContractibleEdges}). 
In particular it vanishes on the graph for the single [[Chern-Simons propagator]]:

<center>
<img src="https://ncatlab.org/nlab/files/DifferentialOnPropagatorGraphVanishes.jpg" width="270">
</center>

=--

+-- {: .num_example #DifferentialOnLinearGraph}
###### Example
**(differential on linear graphs)**

The differential of Def. \ref{DifferentialOnGraphs} applied to the linear graph with one internal vertex:

<center>
<img src="https://ncatlab.org/nlab/files/DifferentialOfSimpleLinearGraphInGraphComplex.jpg" width="700">
</center>

Here the right hand side vanishes, due to the sign rule (eq:SignFromOrientationReversal).

While this example illustrates the general action of the differential, beware that this particular differential relation will not actually contribute to the graph complex, as the graph on the left is a "vanishing graph" in the sense of Def. \ref{VanishingGraphs} below (since the valence of the internal vertex is $\lt 3$).


=--



+-- {: .num_example #ThreeTermRelation}
###### Example
**(differential of trivalent diagram with single internal vertex)**

The image of the single trivalent internal vertex under the differential from Def. \ref{DifferentialOnGraphs} is as shown in the following:

<center>
<img src="https://ncatlab.org/nlab/files/DifferentialOfSingleTrivalentInternalVertex.jpg" width="800">
</center>


Under the [[quasi-isomorphism]] (eq:TheQuasiIsomorphism) from the [[graph complex]] to the [[de Rham complex]] on the [[Fulton-MacPherson compactification]] of a [[configuration space of points]], given by sending each [[graph]] to its [[Chern-Simons propagator|Chern-Simons]] [[Feynman amplitude on compactified configuration spaces of points]] ([this Prop.](Fulton-MacPherson+operad#QuasiIsomorphismBetweenGraphComplexAndDeRhamComplexOfFM)), this relation becomes the "3-term relation" ([this Prop.](Fulton-MacPherson+operad#DeRhamCohomologyOfFMCompactification)):

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
    \Omega^2_{PA}
    \Big(
      \underset{{}^{1,\cdots,n}}{Conf}
      \big(
        \mathbb{R}^D 
      \big)  
    \Big)
  \right)
  \,.
$$

=--

([Lambrechts-Volić 14, Figure 1 and 2](#LambrechtsVolic14))


+-- {: .num_example #DifferentialOfMinimalTrivalenVacuumGraph}
###### Example
**(Differential of minimal trivalent [[vacuum diagram]])**

The differential of the minimum trivalent [[vacuum diagram]] from Example \ref{TrivalenGraphs}:


<center>
<img src="https://ncatlab.org/nlab/files/The0CocycleInTheGraphComplex.jpg" width="800">
</center>


=--


+-- {: .num_example #DifferentialOfTrivalentTreeWithTwoInternalVertices}
###### Example
**(differential of trivalent tree with two internal vertices)**

The differential (Def. \ref{DifferentialOnGraphs}) on the trivalent tree
with two internal vertices:

<center>
<img src="https://ncatlab.org/nlab/files/DiffTrivTreeWthTwoIntVertices.jpg" width="800">
</center>

=--


+-- {: .num_lemma #DifferentialProperties}
###### Lemma
**(differential graded algebra structure)**

The [[linear map]] $d$ in Def. \ref{DifferentialOnGraphs} makes the [[graded vector space]] $\widehat Graphs_n(\mathbb{R}^D)$ a [[cochain complex]], and, with its [[graded algebra]]-[[structure]] from Lemma \ref{GradedCommutativeAlgebraOfGraphs} in fact a [[differential graded algebra]], in that:

1. (well defined) $d$ indeed only depends on the equivalence class $[\Gamma]$;

1. (degree) $d$ increases degree by +1

1. (nilpotency) 

   $$
     d \circ d = 0
   $$

1. ([[derivation]])  

   $$
     d( [\Gamma_1] \wedge [\Gamma_2] )
     \;=\;
     \big( d[\Gamma_1]  \big) \wedge [\Gamma_2]
     +
     (-1)^{deg(\Gamma_1)} [\Gamma_1] \wedge \big( d [\Gamma_2]\big)     
     \,.
   $$

=--

([Lambrechts-Volić 14, Lemmas 6.11 - 6.14](#LambrechtsVolic14))








\linebreak


##### The graph complex
 {#TheGraphComplex}

+-- {: .num_defn #VanishingGraphs}
###### Definition
**(vanishing graphs)**

We say that a graph $\Gamma$ (Def. \ref{Graphs}) is a _vanishing graph_ if it is one or more of the following:

* it is a [[tadpole-diagram]]: $\Gamma$ contains an edge $e$ with $s(e) = t(e)$ (Example \ref{GraphsWithDirectLoopsVanish});

* it is a [[vacuum diagram]]: $\Gamma$ contains an internal vertex which is not connected, via some path of edges, to an external vertex;

* it has [[parallel edges]]: $\Gamma$ contains a pair $(a,b)$ of vertices, with more than one edge between them, i.e. if the [[preimage]] $(s,t)^{-1}\big\{(a,b)\big\}$ contains more than one element.
 
* it is less than trivalent: $\Gamma$ contains an internal vertex $v \in Verts_{int}$ that is less than trivalent, hence an internal vertex with less than 3 edges attached to it;



Write 

$$
  {\widehat Graphs}^{nil}_n(\mathbb{R}^3)
  \;\subset\;
  \widehat Graphs_n\big( \mathbb{R}^3 \big)
$$

for the [[subspace]] spanned by vanishing graphs $[\Gamma]$ inside the [[graded vector space]] (eq:VectorSpaceOfGraphsWithSignRulesImposed) of all graphs.


=--

([Lambrechts-Volić 14, Def. 6.16](#LambrechtsVolic14))


+-- {: .num_lemma #VanishingGraphsAreDifferentialIdeal}
###### Lemma
**(vanishing graphs form a differential ideal)**

The subspace of vanishing graphs (Def. \ref{VanishingGraphs}) is a [[differential ideal]] in the [[differential graded-commutative algebra]] of all graphs (Lemma \ref{DifferentialProperties}).

=--

([Lambrechts-Volić 14, Lemma 6.17](#LambrechtsVolic14))

This implises that the quotient of all graphs by the vanishing graphs is still a differential graded-commutative algebra:

+-- {: .num_defn #GraphComplexDgcAlgebra}
###### Definition
**(graph complex)**

For $n \in \mathbb{N}$, the _graph complex_ on $n$ external vertices is the [[differential graded-commutative algebra]]

\[
  \label{TheGraphComplexAsQuotientByVanishingGraphs}
  Graphs_n
  \big(
    \mathbb{R}^3
  \big)
  \;\coloneqq\;
  \frac{
    {\widehat Graphs}_n\big( \mathbb{R}^3\big)
  }
  {
    {\widehat Graphs}^{nil}_n\big( \mathbb{R}^3\big)
  }
\]

of the [[differential graded-commutative algebra]] of all graphs (Lemma \ref{DifferentialProperties}) by its [[differential ideal]] (Lemma \ref{VanishingGraphsAreDifferentialIdeal}) of vanishing graphs (Def. \ref{VanishingGraphs}).

=--

([Lambrechts-Volić 14, Def. 6.19](#LambrechtsVolic14))

+-- {: .num_example #A9CocycleInGraphs3}
###### Example
**(A 9-cocycle in $Graphs_3(\mathbb{R}^3)$)**

The trivalent graph of degree 9 from Example \ref{TrivalenGraphs} is a [[cocycle]] in $Graphs_3(\mathbb{R}^3)$ (Def. \ref{GraphComplexDgcAlgebra}):

<center>
<img src="https://ncatlab.org/nlab/files/A9CocycleInGraphs3.jpg" width="610">
</center>

The computation of the differential is just as  for the 3-term relation in Example \ref{ThreeTermRelation},
but now all summands on the right have [[parallel edges]] and hence are vanishing graphs (Def. \ref{VanishingGraphs}) that are zero in the quotient (eq:TheGraphComplexAsQuotientByVanishingGraphs) defining the  graph complex $Graphs_3\big( \mathbb{R}^3 \big)$ (Def. \ref{GraphComplexDgcAlgebra}).

> This trivalent diagram must be exact, as there is not supposed to be any cohomology in degree 9 (by Prop. \ref{RealCohomologyOfConfigurationSpaceOfOrderedPointsInEuclideanSpace}). What's a trivializing coboundary?

=--

+-- {: .num_lemma #GraphsAreInNonNegativeDegree}
###### Lemma
**(graphs are in non-negative degree)**

For all $n \in \mathbb{N}$, the degrees (Def. \ref{DegreeOfAGraph})  of any non-vanishing graph $[\Gamma]$ in the graph complex $Graphs_n(\mathbb{R}^3)$ (Def. \ref{GraphComplexDgcAlgebra}) are non-[[negative number|negative]]

$$
  deg\big( [\Gamma] \big)
  \;\geq\;
  0
  \;\;
  \in
  \;\;
  Graphs_n(\mathbb{R}^3)
  \,.
$$

Moreover, the only graphs of degree 0 are those containg the external vertices and nothing else:

$$
  deg\big( [\Gamma]\big)
  =
  0
  \;\;\;\;\;\;\Leftrightarrow\;\;\;\;\;\;
  [\Gamma] = 0
  \;\;\;\text{or}\;\;\;
  [\Gamma] = \big[ {}_1 \;\; {}_2 \;\; \cdots \;\; {}_n  \big]
  \;\;\;\;\in\;\;
  Graphs_n(\mathbb{R}^3)
  \,.
$$

=--


+-- {: .proof}
###### Proof

Since [[tadpole]] graphs are vanishing graphs by Def. \ref{VanishingGraphs}, we may assume that each edge in $\Gamma$ has two distint vertices it ends on, for otherwise we have the zero element in the graph complex.

Now, since each edge has degree 2 (according to Def. \ref{DegreeOfAGraph}), we may think of each edge as contribution a degree +1 for each of its two vertices, via the coresponding half-edge ending on that vertex.

Since external vertices have degree 0, together with the half-edges that end on them they contribute a non-negative number to the total degree.

While internal vertices have degree -3 (according to Def. \ref{DegreeOfAGraph}), we have a vanishing graph if less than three edges meet at an internal vertex (by Def. \ref{VanishingGraphs}) and hence, once vanishing graphs have been quotiented out, also internal vertices together with the half-edges ending on them contribute a non-negative number to the  total degree.

This proves the first claim. 

For the second claim, recall from Example \ref{TrivalenGraphs} that a graph has degree 0 precisely if it is a disjoint union of a) isolated external vertices and b) trivalent graphs all whose vertices are internal.

But if there is any disjoint non-empty sub-graph with only internal vertices, the total graph is again a vanishing graph by Def. \ref{VanishingGraphs}, since it contains internal vertices not connected to any external vertex.


<center>
<img src="https://ncatlab.org/nlab/files/VacuumDiagramVanishesInGraphComplex.jpg" width="610">
</center>


Hence the only non-vanishing graphs of degree 0 are those which have some isolated external vertices and nothing else. 


<center>
<img src="https://ncatlab.org/nlab/files/BareExternalVCerticesGenerateH0OfGraphComplex.jpg" width="610">
</center>


=--








\linebreak



#### $Graphs_n\big(  \mathbb{R}^2 \big)$

(...)





\linebreak

### **2)** Graph complexes modelling spaces of knots
  {#GraphComplexesModellingSpacesOfKnots}


We discuss graph complexes $KnotGraphs(\Sigma)$ modelling the [[real cohomology]] of [[spaces of knots]] $Emb(S^1,\Sigma)$. 

For the case of $\Sigma = \mathbb{R}^D$ these were originally hinted at in [Kontsevich 93, Section 5](#Kontsevich93) and discussed in detail in [Cattaneo, Cotta-Ramusino, Longoni 02](#CattaneoCottaRamusinoLongoni02) [05](#CattaneoCottaRamusinoLongoni05), see also [Bar-Natan 91](#BarNatan91). Review is in [Volić 13, Section 4](#Volic13).


\linebreak

#### $KnotGraphs\big( \mathbb{R}^3 \big)$
 {#KnotGraphsDefinition}

We state the definition of the graph complexes $KnotGraphs\big( \mathbb{R}^3\big)$ of _knot graphs_ (according to the [above](#IdeaGraphComplexModelForSpacesOfKnots)) associated with [[Euclidean space]] of [[dimension]] 3, following [Cattaneo, Cotta-Ramusino, Longoni 02](#CattaneoCottaRamusinoLongoni02) [05](#CattaneoCottaRamusinoLongoni05).

The definition is almost exactly the same as that of $\oplus_n Graphs_n\big( \mathbb{R}^3\big)$ [above](#GraphComplexForConfigurationsOfPointsInR3), except for the following two differences:

**1)** external vertices now carry degree -1, so that the formula (eq:DegreeOfAGraph) for the degree of a graph is changed to

\[
  \label{DegreeOfAKnoptGraph}
  deg\big( [\Gamma]\big) 
  \;=\;
  (D-1) \cdot \#\!Edges 
  \;
  - D \cdot \#\!Vertices_{int}
  \;
  - 1 \cdot \#\!Vertices_{ext}
  \,,
\]

([CCRL 02, (4.6)](#CattaneoCottaRamusinoLongoni02), [Volić 13, Def. 4.3](#Volic13))

**2)** There is implicit a contractible edge from the $k$th to the $(k+1)$st external vertex (an _arc_), in that the definition of the differential (Def. \ref{DifferentialOnGraphs}) regards these as contractible edges.

([CCRL 02, 4.2](#CattaneoCottaRamusinoLongoni02), [Volić 13, p. 35](#Volic13))

**3)** Apparently it must be understood that graphs whose labelling of external vertices differs by a cyclic permutation are identified. (?!)

(...)

+-- {: .num_example #KnotGraphCocycleOfOrder2}
###### Example
**(knot graph cocycle of order 2)**

The differential in $KnotGraphs(\mathbb{R}^3)$ of the single trivalent internal vertext is a variant of that in $Graphs_3\big(\mathbb{R}^3\big)$ (Example \ref{ThreeTermRelation}) and that in $Graphs_0\big( \mathbb{R}^3\big)$ (Example \ref{DifferentialOfMinimalTrivalenVacuumGraph}):

<center>
<img src="https://ncatlab.org/nlab/files/The3TermRelationInTheKnotGraphComplexII.jpg" width="680">
</center>

Notice how the edges parallel to the outer dashed arcs do not make the graphs in the first line vanish, but the [[parallel edges]] appearing in the second line make vanishing graphs (Def. \ref{VanishingGraphs}).

In contrast, the differential of the diagram in $KnotGraphs(\mathbb{R}^3)$ consisting of just two overlapping chords gets contributions only from contraction of the four arcs:

<center>
<img src="https://ncatlab.org/nlab/files/Diff2ChordsDiagramInKnotGraphs.jpg" width="720">
</center>

In both cases, the identification of graphs whose external labels are ccyclically permutated identifies the right hand sides of both these coboundaries with multiples of one and the same element in the graph complex.

Accordingly, the corresponding linear combination 

is a [[cocycle]] of degree 0 in $KnotGraphs(\mathbb{R}^3)$:

<center>
<img src="https://ncatlab.org/nlab/files/CocycleInKnotGraphs.jpg" width="460">
</center>


=--

([Bar-Natan 91, 4.3.2](#BarNatan91), [Cattaneo, Cotta-Ramusino, Longoni 02, Figure 2](#CattaneoCottaRamusinoLongoni02))


<div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/KnotGraphCocycleOfOrder2.jpg" width="300">
</div>

\linebreak
\linebreak

$\in H^0\Big( KnotGraphs\big( \mathbb{R}^3 \big) \Big)$

For the corresponding [[Feynman amplitude]] [[knot invariant]] see Prop. \ref{FirstKnotInvariantFromChernSimonsFeynmanAmplitude} below.


\linebreak



## Properties
 {#Properties}

> under construction

### Cohomology of configuration spaces via Feynman diagrams
 {#RelationToConfigurationSpaces}

Reading the graphs as [[Chern-Simons theory]] [[Feynman diagrams]], hence as instructions for [[configuration space of points|configuration space]]-[[integrals]] of [[wedge products]] of [[Feynman propagators]] assigned to [[edges]] in a graph, with [[propagators regarded as differential forms on configuration spaces]],
yields a [[quasi-isomorphism]] from the graph complex to the [[real cohomology]] of [[configuration spaces of points]].

([Lambrechts-Volić 14, Section 9](#LambrechtsVolic14))

\[
  \underset{
    \color{blue}
    \array{
      \phantom{A}
      \\
      \text{graph complex}
      \\
      \text{of n-point Feynman diagrams}
      \\
      \text{for Chern-Simons theory}
      \\
      \text{on} \; \Sigma 
    }
  }{
    Graphs_n(\Sigma)
  }
  \underoverset{
    \simeq_{\mathrlap{qi}}
  }
  {
    \color{blue}
    \array{
      \text{assign Feynman amplitudes}
      \\
      \text{of Chern-Simons theory}
      \\
      \text{by configuration-space integral}
      \\
      \text{of internal vertices over}\; \Sigma
      \\
      \phantom{A}
    }
  }
  {
    \longrightarrow
  }
  \underset{
    \color{blue}
    \array{
      \phantom{A}
      \\
      \text{de Rham algebra}
      \\
      \text{of semi-algebraic differential forms}
      \\
      \text{on the FM-compactification}
      \\
      \text{of the configuration space of n points}
      \\
      \text{in}\; \Sigma
    }
  }{
  \Omega^\bullet_{PA}
  \big(
    \underset{{}^{1,\cdots,n}}{Conf}\big(  \Sigma \big)
  \big)
  }
  \,.
\]


+-- {: .num_prop #RealCohomologyOfConfigurationSpaceOfOrderedPointsInEuclideanSpace}
###### Proposition
**([[real cohomology]] of configuration spaces of ordered points in [[Euclidean space]])**

The [[real cohomology|real]] [[cohomology ring]] of the configuration spaces 

$$
  \underset{{}^{1,\cdots,n}}{Conf}\big( \mathbb{R}^D \big) 
  \;\coloneqq\;
  \big( \mathbb{R}^D \big)^n \setminus FatDiag
$$

of $n$ ordered points in [[Euclidean space]] $\mathbb{R}^D$ is [[generators and relations|generated]] by elements 

$$ 
  \omega_{i j}
  \;\;
  \in
  H^2
  \Big(
    \underset{{}^{1,\cdots,n}}{Conf}\big( \mathbb{R}^D \big),
    \mathbb{R}
  \Big)
$$

for $i, j \in \{1, \cdots, n\}$

subject to these three [[generators and relations|relations]]:

1. $\omega_{i j} = (-1)^D \omega_{j i} $;

1. $\omega_{i j} \wedge \omega_{i j} \;=\; 0$;

1. $\omega_{i j} \wedge \omega_{j k} + \omega_{j k} \omega_{k i} + \omega_{k i} \wedge \omega_{i j} = 0$.

Hence:

$$
  H^\bullet
  \Big(
    \underset{{}^{1,\cdots,n}}{Conf}\big( \mathbb{R}^D \big),
    \mathbb{R}
  \Big)
  \;\simeq\;
  \mathbb{R}\Big[ \big\{\omega_{i j} \big\}_{i, j \in \{1, \cdots, n\}} \Big]
  \Big/
  \left(
    \array{
      \omega_{i j} = (-1)^D \omega_{j i}
      \\
      \omega_{i j} \wedge \omega_{i j} = 0
      \\
      \omega_{i j} \wedge \omega_{j k} + \omega_{j k} \omega_{k i} + \omega_{k i} \wedge \omega_{i j} = 0    
     }
     \;\;
     \text{for}\;
     i,j \in \{1, \cdots, n\}
  \right)
$$

=--

This is due to [Arnold 69](configuration+space+of+points#Arnold69), [Cohen 73](configuration+space+of+points#Cohen73).



| [[real cohomology]] of [[configuration space of points]] |  [[graph complex]] ([this Prop.](configuration+space+of+points#RealCohomologyOfConfigurationSpaceOfOrderedPointsInEuclideanSpace)) | 
|------------------|-------------------------|
| generator <br/> $\omega_{i j} \in H^2\Big( \underset{{}^{1,\cdots,n}}{Conf}\big( \mathbb{R}^3\big) \Big)$ | [[edge]] <br/> $i \longrightarrow j$   | 
| **[[generators and relations|relations]]:** | **[[generators and relations|relations]]:** |
| $\omega_{i j} = - \omega_{j i} $ | graph changes sign when edge is reversed (Def. \ref{SignRulesForGraphs}) | 
| $\omega_{i j} \wedge \omega_{i j} \;=\; 0 $ | graph with [[parallel edges]] vanishes (Def. \ref{VanishingGraphs}) |  
| $\omega_{i j} \wedge \omega_{j k} + \omega_{j k} \omega_{k i} + \omega_{k i} \wedge \omega_{i j} = 0$ | coboundary of trivalent vertex (Example \ref{ThreeTermRelation}) | 



\linebreak

### Cohomology of knot space / higher Vassiliev invariants

The [[Feynman amplitudes]] of knot graphs (as [above](#KnotGraphsDefinition)) are  [[Vassiliev knot invariants]].

This was originally hinted at in [Kontsevich 93, Section 5](#Kontsevich93).
Details are in [Cattaneo, Cotta-Ramusino, Longoni 02](#CattaneoCottaRamusinoLongoni02).
Review is in [Volić 13, Section 4](#Volic13).

\[
  \underset{
    \color{blue}
    \array{
      \phantom{A}
      \\
      \text{graph complex}
      \\
      \text{of n-point Feynman diagrams}
      \\
      \text{for Chern-Simons theory}
      \\
      \text{on} \; \Sigma 
    }
  }{
    KnotGraphs(\Sigma)
  }
  \underoverset{
  }
  {
    \color{blue}
    \array{
      \text{assign Feynman amplitudes}
      \\
      \text{of Chern-Simons theory}
      \\
      \text{by configuration-space integral}
      \\
      \text{of internal vertices over}\; \Sigma
      \\
      \text{and of external vertices along the knot}
      \\
      \phantom{A}
    }
  }
  {
    \longrightarrow
  }
  \underset{
    \color{blue}
    \array{
      \phantom{A}
      \\
      \text{de Rham algebra of}
      \\
      \text{space of knots in}\; \Sigma
    }
  }{
  \Omega^\bullet_{PA}
  \big(
    Emb\big( S^1, \Sigma\big)
  \big)
  }
  \,.
\]


+-- {: .num_prop #FirstKnotInvariantFromChernSimonsFeynmanAmplitude}
###### Proposition
**([[knot invariant]] from [[Chern-Simons theory]] [[Feynman amplitude]])**


The [[Feynman amplitude]] 
of the knot graph cocycle [[Feynman diagram]] from Example \ref{KnotGraphCocycleOfOrder2}, in [[Chern-Simons theory]] with a [[Wilson loop]] [[knot]], is a [[knot invariant]]:


<center>
<img src="https://ncatlab.org/nlab/files/FeynmanAmplitudeKnotInvariant.jpg" width="600">
</center>


=--


This is due to [Guadagnini-Martellini-Mintchev 89](#GuadagniniMartelliniMintchev89)
and [Bar-Natan91](#BarNatan91), recalled im [Volić 13, Theorem 3.3.5](#Volic13).

\linebreak


Various authors discuss [[Vassiliev invariants]] in terms of graphs subject to the "[[STU-relation]]"  

([Kontsevich 93, Figure 8](#Kontsevich93), [Bar-Natan 95, Figure 3](Vassiliev+invariant#BarNatan95)) and the "IHX-relation"  which it implies ([Bar-Natan 95, Theorem 6](Vassiliev+invariant#BarNatan95))


<center>
<img src="https://ncatlab.org/nlab/files/KontsevichSTURelation.jpg" width="440">
</center>

> graphics grabbed from [Kontsevich 93](#Kontsevich93)

That these relations characterize the cohomology of the knot-graph complex in the respective degrees is shown in [Koytcheff-Munson-Volic 13, Section 3.4](#KoytcheffMunsonVolic13)


<center>
<img src="https://ncatlab.org/nlab/files/VolicSTURelation.jpg" width="520">
</center>

> graphics grabbed from [Koytcheff-Munson-Volic 13](#KoytcheffMunsonVolic13)

### Cohomology of knot graph complex is weight systems on chord diagrams

[[cohomology of knot graph complex is weight systems on chord diagrams]]


## Further applications

...moduli spaces

...deformation theory

...Rozansky-Witten theory

...description of the classifying space $BOut(F_n)$ of the group of outer automorphisms of a free group with $n$ generators

... another graph complex controls the universal $L_\infty$-deformations of the space of polyvector fields. 


## Related concepts

* [[configuration space of points]], [[space of knots]]

* [[Fulton-MacPherson operad]]

* [[Chern-Simons propagator]]

* [[correlator as differential form on configuration space of points]]


* [[Kontsevich formality]]

* [[Rozansky-Witten theory]]

* [[formal noncommutative symplectic geometry]] 




## References

### General

The rough definition of the graph complex, and its relation to [[Chern-Simons theory]] [[Feynman amplitudes]] and [[Vassiliev knot invariants]] was sketched in

* {#Kontsevich92} [[Maxim Kontsevich]], pages 11-12 of _Feynman diagrams and low-dimensional topology_, First European Congress of Mathematics, 1992, Paris, vol. II, Progress in Mathematics __120__, Birkh&#228;user (1994), 97&#8211;121 ([pdf](http://www.ihes.fr/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf))

* {#Kontsevich93} [[Maxim Kontsevich]], Section 5 of: _Vassiliev's knot invariants_, Advances in Soviet Mathematics, Volume 16, Part 2, 1993 ([pdf](http://pagesperso.ihes.fr/~maxim/TEXTS/VassilievKnot.pdf), [[KontsevichVassilievInvariants93.pdf:file]])

* {#Kontsevich99b} [[Maxim Kontsevich]], around Def. 15 and Lemma 3 in _Operads and Motives in Deformation Quantization_, Lett. Math. Phys. 48 35-72, 1999 ([arXiv:math/9904055](https://arxiv.org/abs/math/9904055))

### As a rational model for configuration spaces

A clean account and proof of the graph complex as a model for the [[rational homotopy type]] of the [[Fulton-MacPherson compactification]] of [[configuration spaces of points]] (exhibiting the [[formal smooth manifold|formality]] of the [[little n-disk operads]]) is in

* {#LambrechtsVolic14} [[Pascal Lambrechts]], [[Ismar Volić]], sections 6 and 7 and 9 of: _Formality of the little N-disks operad_, Memoirs of the American Mathematical Society no. 1079, 2014  ([arxiv:0808.0457](https://arxiv.org/abs/0808.0457), [doi:10.1090/memo/1079](http://dx.doi.org/10.1090/memo/1079))

Discussion as a direct model for the rationalized [[homotopy groups]] of the [[configuration space of points]]:

* [[Pascal Lambrechts]], [[Victor Tourtchine]], _Homotopy graph-complex for configuration and knot spaces_, Transactions of the AMS, Volume 361, Number 1, January 2009, Pages 207–222 ([arxiv:math/0611766](https://arxiv.org/abs/math/0611766))


further review:

* {#Fresse18} [[Benoit Fresse]], _Little discs operads, graph complexes and Grothendieck--Teichmüller groups_, in [[Haynes Miller]] (ed.) _[[Handbook of Homotopy Theory]]_ ([arXiv:1811.12536](https://arxiv.org/abs/1811.12536))


Further discussion of the graph complex as a model for the [[de Rham cohomology]] of  [[configuration spaces of points]] is in


* [[Najib Idrissi]], _The Lambrechts-Stanley Model of Configuration Spaces_, Invent. Math, 2018 ([arXiv:1608.08054](https://arxiv.org/abs/1608.08054), [doi:10.1007/s00222-018-0842-9](https://dx.doi.org/10.1007/s00222-018-0842-9))

* {#CamposWillwacher16} [[Ricardo Campos]], [[Thomas Willwacher]], _A model for configuration spaces of points_ ([arXiv:1604.02043](https://arxiv.org/abs/1604.02043))

* {#Campos17} [[Ricardo Campos]], _Batalin-Vilkovisky formality and configuration spaces of points_, 2017 ([doi:10.3929/ethz-a-010886114](https://doi.org/10.3929/ethz-a-010886114))


* {#CamposIdrissiLambrechtsWillwacher18} [[Ricardo Campos]], [[Najib Idrissi]], [[Pascal Lambrechts]], [[Thomas Willwacher]], _Configuration Spaces of Manifolds with Boundary_ ([arXiv:1802.00716](https://arxiv.org/abs/1802.00716))

* [[Ricardo Campos]], Julien Ducoulombier, [[Najib Idrissi]], [[Thomas Willwacher]], _A model for framed configuration spaces of points_ ([arXiv:1807.08319](https://arxiv.org/abs/1807.08319))

See also

* {#Kontsevich99a} [[Maxim Kontsevich]], _Rozansky&#8211;Witten invariants via formal geometry_, Compositio Mathematica __115__: 115&#8211;127, 1999, [doi](http://dx.doi.org/10.1023/A:1000619911308), [arXiv:dg-ga/9704009](http://arxiv.org/abs/dg-ga/9704009)


* [[Andrey Lazarev]], _Operads and topological conformal field theories_, [pdf](http://www.maths.lancs.ac.uk/~lazarev/1-10.pdf); and older versio: _Graduate lectures on operads and topological field theories_, zip file with 11 pdfs, [over 5 Mb](http://www2.le.ac.uk/departments/mathematics/extranet/staff-material/staff-profiles/al179/New%20Folder.zip)

* [[Alastair Hamilton]], _A super-analogue of Kontsevich's theorem on graph homology_, Lett. Math. Phys. __76__ (2006), no. 1, 37--55, [math.QA/0510390](http://arxiv.org/abs/math/0510390)

* A. Lazarev, [[Alexander Voronov]], _Graph homology: Koszul and Verdier duality_ ([math.QA/0702313](http://arxiv.org/abs/math/0702313))

* [[Mikhail Movshev]], _A definition of graph homology and graph K-theory of algebras_ ([math.KT/9911111](http://arxiv.org/abs/math/9911111))


* [[Kiyoshi Igusa]], _Graph cohomology and Kontsevich cycles_, Topology __43__ (2004), n. 6, p. 1469-1510, [MR2005d:57028](http://www.ams.org/mathscinet-getitem?mr=2005d:57028), [doi](http://dx.doi.org/10.1016/j.top.2004.03.004)



* [[Vasily Dolgushev]], [[Christopher Rogers]], [[Thomas Willwacher]], _Kontsevich's graph complex, GRT, and the deformation complex of the sheaf of polyvector fields_ ([arxiv/1211.4230](http://arxiv.org/abs/1211.4230))

* [[Damien Calaque]], Carlo A. Rossi, _Lectures on [[Duflo isomorphism]]s in Lie algebra and complex geometry_, European Math. Soc. 2011

* [[Sergei Merkulov]], _Graph complexes with loops and wheels_, in (Manin's Festschrift:) Algebra, Arithmetic, and Geometry, Progress in Mathematics __270__ (2009) 311-354, [doi](http://dx,doi.org/10.1007/978-0-8176-4747-6_10), [pdf](http://www2.math.su.se/~sm/Papers/graph_complexes.pdf)


* [[Martin Markl]], [[Sergei Merkulov]], S. Shadrin, _Wheeled PROPs, graph complexes and the master equation_, J. Pure Appl. Algebra, 213(4):496–535, 2009, [math.AT/0610683](https://arxiv.org/abs/math/0610683)

The following survey has discussion of context between the graph complex and [[Batalin-Vilkovisky formalism]]:

* Jian Qiu, Maxim Zabzine, _Introduction to graded geometry, Batalin-Vilkovisky formalism and their applications_, [arxiv/1105.2680](http://arxiv.org/abs/1105.2680) 
* Jian Qiu, Maxim Zabzine, _Knot weight systems from graded symplectic geometry_, [arxiv/1110.5234](http://arxiv.org/abs/1110.5234) 

* [[Alastair Hamilton]], [[Andrey Lazarev]], _Graph cohomology classes in the [[BV-BRST formalism|Batalin-Vilkovisky formalism]]_, J.Geom.Phys. __59__:555-575, 2009, [arxiv/0701825](http://arxiv.org/abs/math/0701825)


### As construction of higher order Vassiliev invariants

Discussion of the graph complex as computing higher order [[Vassiliev invariants]], hence the [[real cohomology]] of spaces of [[knots]] (with the cohomology in degree-0 being the ordinary [[Vassiliev invariants]]):

* [Kontsevich 93, Section 5](#Kontsevich93)

* Daniel Altschuler, Laurent Freidel, _Vassiliev knot invariants and Chern-Simons perturbation theory to all orders_, Commun. Math. Phys. 187 (1997) 261-287 ([arxiv:q-alg/9603010](https://arxiv.org/abs/q-alg/9603010))

* {#CattaneoCottaRamusinoLongoni02} [[Alberto Cattaneo]], Paolo Cotta-Ramusino, Riccardo Longoni, _Configuration spaces and Vassiliev classes in any dimension_, Algebr. Geom. Topol. 2 (2002) 949-1000 ([arXiv:math/9910139](https://arxiv.org/abs/math/9910139))

* {#CattaneoCottaRamusinoLongoni05} [[Alberto Cattaneo]], Paolo Cotta-Ramusino, Riccardo Longoni, _Algebraic structures on graph cohomology_, Journal of Knot Theory and Its Ramifications, Vol. 14, No. 5 (2005) 627-640 ([arXiv:math/0307218](https://arxiv.org/abs/math/0307218), [doi:10.1142/S0218216505004019](http://dx.doi.org/10.1142/S0218216505004019), [math.GT/0307218](http://arxiv.org/abs/math/0307218), [MR2006g:58021](http://www.ams.org/mathscinet-getitem?mr=2006g:58021))

* {#GuadagniniMartelliniMintchev89} E. Guadagnini, E. Martellini, M. Mintchev, _Chern-Simons field theory and  link invariants_,  In:   _Knots,  Topology  and  QuantumField Theories_,  Proceedings of the Johns Hopkins Workshop onCurrent Problems in Particle Theory 13, Florence (1989), World Scientific ([doi:10.1142/9789814540742](https://doi.org/10.1142/9789814540742))

* {#BarNatan91} [[Dror Bar-Natan]], _Perturbative aspects of the Chern-Simons topological quantum field theory_, thesis 1991 ([spire:323500](http://inspirehep.net/record/323500), [proquest:303979053](https://search.proquest.com/docview/303979053), [[BarNatanPerturbativeCS91.pdf:file]])



Reviewed in:

* {#Volic13} [[Ismar Volić]], Section 4 of: _Configuration space integrals and the topology of knot and link spaces_, [Morfismos, Vol 17, no 2, 2013](https://fdocuments.co/amp/document/morfismos-vol-17-no-2-2013.html) ([arxiv:1310.7224](https://arxiv.org/abs/1310.7224))


### Coproduct

Discussion of [[coproducts]] on a graph complex, given by decomposition of graphs into subgraphs and contractions of subgraphs:

* {#Ionescu03} [[Lucian Ionescu]], _Perturbative Quantum Field Theory and Configuration Space Integrals_, In: John Byden, _Advances in Topological Quantum Field Theory_ ([arXiv:hep-th/0307062](https://arxiv.org/abs/hep-th/0307062), [doi:10.1007/978-1-4020-2772-7](https://link.springer.com/book/10.1007/978-1-4020-2772-7))

* {#Ionescu05} [[Lucian Ionescu]], _Cohomology of Feynman graphs and perturbative quantum field theory_, In: O. Kovras, _Focus on Quantum Field Theory_, Nova Publishers Inc. 2004,  ([arXiv:math/0506142](https://arxiv.org/abs/math/0506142))



### Cohomology
 {#ReferencesCohomology}

On the [[cochain cohomology]] of [[graph complexes]]:

Characterization of cohomology of (...) in terms of [[STU-relations]] and HKX-relations:

* {#KoytcheffMunsonVolic13} Robin Koytcheff, Brian A. Munson, [[Ismar Volić]], Section 3.4 of: _Configuration space integrals and the cohomology of the space of homotopy string links_, J. Knot Theory Ramif. 22, no. 11, 73 pp. (2013) ([arXiv:1109.0056](https://arxiv.org/abs/1109.0056))

Concrete examples of cohomology classes in certain bi-degrees in $Graphs_0(\mathbb{R}^2)$ by [[computer experiment]]:

* {#BarNatanMcKay} [[Dror Bar-Natan]], [[Brendan McKay]], _Graph cohomology -- An overview and some computations_ ([[BarNatanMcKayGraphCohomology.pdf:file]])


$H^0\big( Graphs_0(\mathbb{R}^2) \big)$ is the [[Lie algebra]] of the [[Grothendieck-Teichmüller group]]:

* {#Willwacher10} [[Thomas Willwacher]], _M. Kontsevich's graph complex and the Grothendieck-Teichmueller Lie algebra_, Invent. math. (2015) 200: 671 ([arxiv:1009.1654](http://arxiv.org/abs/1009.1654))

* {#DolgushevRogers12} [[Vasily Dolgushev]], [[Christopher Rogers]], _Notes on Algebraic Operads, Graph Complexes, and Willwacher's Construction_, In: Mathematical aspects of quantization 583 (2012): 25-145. ([arXiv:1202.2937](https://arxiv.org/abs/1202.2937))

* [[Vasily Dolgushev]], _A manifestation of the Grothendieck-Teichmuellergroup in geometry_ ([slides pdf](https://math.temple.edu/~vald/AMSslides.pdf))

See also:

* Kevin Morand, _A note on multi-oriented graph complexes and deformation quantization of Lie bialgebroids_ ([arXiv:2102.07593](https://arxiv.org/abs/2102.07593))


More:

* {#KoroshkinWillwacherZivkovic14} Anton Khoroshkin, [[Thomas Willwacher]], Marko Živković, _Differentials on graph complexes_ ([arXiv:1411.2369](https://arxiv.org/abs/1411.2369))

### More

In relation to [[Feynman rules]]:

* Marko Berghoff, [[Dirk Kreimer]], _Graph complexes and Feynman rules_ ([arXiv:2008.09540](https://arxiv.org/abs/2008.09540))




[[!redirects graph complexes]]

[[!redirects graph homology]]
[[!redirects graph homology group]]
[[!redirects graph homology groups]]

[[!redirects graph cohomology]]
[[!redirects graph cohomology group]]
[[!redirects graph cohomology groups]]

[[!redirects knot graph complex]]
[[!redirects knot graph complexes]]
[[!redirects knot graph cohomology]]


[[!redirects knot-graph complex]]
[[!redirects knot-graph complexes]]



