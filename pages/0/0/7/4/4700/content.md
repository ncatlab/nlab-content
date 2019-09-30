

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

A _graph complex_ is a certain [[cochain complex]] [[linear span|spanned]] by [[equivalence classes]] of certain labeled [[directed graphs]], whose [[differential]] encodes the operation of contracting away [[edges]] in a graph.

A concrete implementation of this general idea 
originally sketched in [Kontsevich 94 (p. 11-12)](#Kontsevich94) and worked out in [Lambrechts-Volić 14](#LambrechtsVolic14)
is often referred to by default as _the graph complex_ and yields a [[real numbers|real]] [[cochain complex]], and in fact a [[differential graded-commutative algebra]]

$$
  Graphs_n(D)
  \;\in\;
  dgcAlg_{\mathbb{R}}
  \phantom{AA}
  n, D \in \mathbb{N}
  \,,
$$


which is [[quasi-isomorphism|quasi-isomorphic]] to the [[de Rham cohomology]], and in fact to the semi-algebraic [[de Rham algebra]]


$$
  \Omega^\bullet_{PA}
  \big(
    Conf_n
    \big( 
      \mathbb{R}^D
    \big)
  \big)
  \;\in\;
  dgcAlg_{\mathbb{R}}
  \phantom{AA}
  n, D \in \mathbb{N}
$$

of (the [[Fulton-MacPherson compactification]] of) the [[configuration space of points]] $Conf_n(\mathbb{R}^D)$ for $n$ points in $D$-dimensional [[Euclidean space]].

The [[chain map]] which exhibits this [[quasi-isomorphism]] is essentially given by sending each graph to the corresponding [[Feynman amplitude]] in [[free field theory|free]] [[Chern-Simons theory|Chern-Simons]]/[[AKSZ theory]] on $X$, by regarding [[Feynman amplitudes as differential forms on configuration spaces of points]]:

\[
  \label{TheQuasiIsomorphism}
  Graphs_n(D)
  \underoverset{
    \simeq_{\mathrlap{qi}}
  }
  {
    \color{blue}
    {
      \text{
        assign Feynman amplitudes
      }
      \atop
      \text{
        in free CS/AKSZ theory
      }
    }
  }
  {
    \longrightarrow
  }
  \Omega^\bullet_{PA}
  \big(
    Conf_n\big(  \mathbb{R}^D \big)
  \big)
  \,.
\]

This means that for each [[edge]] in a [[graph]] a [[Chern-Simons propagator]] is assigned, and for each of $n_{int} \in \mathbb{N}$ internal [[vertices]] the [[fiber integral]] of the adjacent [[Chern-Simons propagators]] along the canonical [[fibration]] of [[configuration spaces of points]]:

$$
  Conf_{n + n_{int}}( \mathbb{R}^D )
  \longrightarrow
  Conf_{n}( \mathbb{R}^D )
  \,.
$$

This was originally sketched in [Kontsevich 94, p. 11-12](#Kontsevich94). A detailed construction and proof was laid out in [Lambrechts-Volić 14](#LambrechtsVolic14). Other authors have claimed various generalizations of this result, generalizing [[Euclidean space]] $\mathbb{R}^D$ to more general [[smooth manifolds]], possibly [[manifold with boundary|with boundary]].

 


## Definition
 {#GraphComplex}



A clean definition of the graph complex for points in [[Euclidean space]] $\mathbb{R}^D$ is given in [Lambrechts-Volić 14, Section 6](#LambrechtsVolic14). For definiteness, we here state the definition for $D = 3$. 

(But for general $D \in \mathbb{N}$ the definition is essentially the same, differing only in the degrees assigned to graphs, and in the signs appearing in the equivalence relation between graphs and in the definition of the differential. For even dimensions these signs depend on a linear order on the set of edges instead of fthe set of vertices.)


### Graphs

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

1. a [[linear order]] on $V$, such that $V_{ext} \lt V_{int}$.

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

We write $\#\! Vert \coloneqq \left\vert V \right\vert$ for the [[cardinality]] of the sets of vertices, etc.


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

$$
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
  \Big]
  \;\in\;
  Vect_{\mathbb{R}}
  \,.
$$

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


and


$$
  \Gamma
  \;\sim\;
  -\Gamma'
  \phantom{AA}
  \array{
    \text{if}\;\Gamma'\;\text{is}\;\Gamma\;\text{with}
    \\
    \text{a pair of consecutive internal vertices transposed}
  }
$$


=--

([Lambrechts-Volić 14, Def. 6.5 & Def. 6.5](#LambrechtsVolic14))

Since this [[equivalence relation]] is linear, the set of its [[equivalence classes]] 

\[
  \label{VectorSpaceOfGraphsWithSignRulesImposed}
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

is still a [[vector space]], and since the equivalence relation preserves the degrees, it is still a [[graded vector space]]

For $\Gamma$ any graph, we write 

\[
  \label{EquivalenceClassOfAGraphForSignRules}
  \big[ \Gamma \big]
  \;\in\;
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
  \,.
\]

for its [[equivalence class]].

<center>
<img src="https://ncatlab.org/nlab/files/GraphComplexSignsFromOrientationReversal.jpg" width="400">
</center>



+-- {: .num_example #GraphsWithDirectLoopsVanish}
###### Example
**(no tadpoles)**

A direct consequence of quotienting out the [[equivalence relation]]
(eq:SignFromOrientationReversal)
is that graphs with "[[tadpoles]]", namely with edges
that have coinciding [[source]] and [[target]] [[vertex]], 
vanish in the graph complex:

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

(This holds for all odd $D  = 2k + 1$.)

<center>
<img src="https://ncatlab.org/nlab/files/GraphsWithDirectLoopsVanishInTheGraphComplex.jpg" width="700">
</center>


=--


### The differential
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
<img src="https://ncatlab.org/nlab/files/DeadEndsInGraphComplex.jpg" width="700">
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

For $Vert_{ext}$ a fixed [[finite set|finite]] [[linear order]] of external vertices, define on the [[graded vector space]] (eq:VectorSpaceOfGraphsWithSignRulesImposed) of [[isomorphism classes]] of graphs, modulo the sign rules of Def. \ref{SignRulesForGraphs}, the [[linear map|linear]] [[endomorphism]] $d$ which is given on the class $[\Gamma]$ \eqref{EquivalenceClassOfAGraphForSignRules} of a graph $\Gamma$ by the [[linear combination]] of all its edge contractions $\Gamma/e$ (Def. \ref{ContractionOfAnEdge}) for all contractible edges (Def. \ref{ContractibleEdges}) weighted by their sign (Def. \ref{SignOfAContractibleEdge}):

$$
  d [\Gamma]
  \;\coloneqq\;
  \underset{ e \in Edg^{contr}_\Gamma }{\sum}
  \epsilon(\Gamma) \cdot [\Gamma/e]
  \,.
$$

=--

([Lambrechts-Volić 14, (84) and Lemma 6.11](#LambrechtsVolic14))

+-- {: .num_example #ThreeTermRelation}
###### Example
**(the "3-term relation")**

The image of the single trivalent vertex under the differential from Def. \ref{DifferentialOnGraphs} is as shown in the following:

<center>
<img src="https://ncatlab.org/nlab/files/GraphComplexThreeTermRelation.jpg" width="800">
</center>

Under the [[quasi-isomorphism]] (eq:TheQuasiIsomorphism) from the [[graph complex]] to the [[de Rham complex]] on the [[Fulton-MacPherson compactification]] of a [[configuration space of points]] given by sending each [[graph]] to its [[Chern-Simons propagator|Chern-Simons]] [[Feynman amplitude on compactified configuration spaces of points]] ([this Prop.](Fulton-MacPherson+operad#QuasiIsomorphismBetweenGraphComplexAndDeRhamComplexOfFM)) this relation becomes the "3-term relation" ([this Prop.](Fulton-MacPherson+operad#DeRhamCohomologyOfFMCompactification)):

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

([Lambrechts-Volić 14, Figure 1 and 2](#LambrechtsVolic14))


### The graph complex

The actual graph complex is now the quotient of the complex defined above by the [[differential ideal]] of non-admissible graphs 

(...)

## Properties

### General properties

There is a canonical [[graded object|bigrading]] on the graph complex, where $\mathcal{G}_{i j}$ is generated by those graphs which have $i$ [[vertices]] and $j$ [[edges]]; the differential has bidegree $(-1,-1)$; each $\mathcal{G}_{i j}$ is finite-dimensional, while the whole complex is infinite-dimensional. 

The graph complex splits into a [[direct sum]] of subcomplexes labelled by the  [[Euler characteristics]] of the underlying graph. 

The structure of a graph complex reflects a structure in the [[Chevalley-Eilenberg complex]] of a certain [[Lie algebra]]; and the graph homology to the relative Lie homology of that Lie algebra as shown by Kontsevich. 


### $L_\infty$-algebra structure

The Graph complex carries the structure of a [[dg-Lie algebra]] ([[L-infinity algebra]]) which acts on the space of choices of [[formal deformation quantization]] of [[Poisson manifolds]]. Its degree-0 [[chain homology]] is the [[Lie algebra]] of the [[Grothendieck-Teichmüller group]]. 

The homology in negative degree vanishes and that in positive degree is still unknown, but computer experiements show that at least the third cohomology contains nontrivial elements.

The degree-0 homology is also isomorphic, up to one "scaling class", to the 0th cohomology of the [[derivations]] of the [[Ek-operad|E2 operad]].

([Willwacher 10](#Willwacher10))

### Relation to Grothendieck-Teichm&#252;ller group and deformation quantization

See at _[deformation quantization -- Motivic Galois group action on the space of quantizations](deformation+quantization#MotivicGaloisGroup)_.

See at _[Grothendieck-Teichm&#252;ller group -- relation to the graph complex](Grothendieck-Teichm%C3%BCller+tower#RelationToTheGraphComplex)_.


### Relation to configuration spaces
 {#RelationToConfigurationSpaces}

The system of graph complexes is [[quasi-isomorphism|quasi-isomorphic]] to the [[real cohomology]] of [[configuration spaces of points]] ([Campos-Willwacher 16, theorem 1](#CamposWillwacher16)).

## Examples 

* Graph complexes may be obtained from the [[Feynman transform]] of a [[modular operad]].


## Further applications

...moduli spaces

...deformation theory

...Rozansky-Witten theory

...Vassiliev invariants

...description of the classifying space $BOut(F_n)$ of the group of outer automorphisms of a free group with $n$ generators

Graph complex controls the universal $L_\infty$-deformations of the space of polyvector fields. 

## Generalizations

There are generalizations for $d$-algebras (algebras over little disc operad in higher dimension). The cohomological graph complex is then the case for $d=2$. There is also a "directed" version. On the other hand, graph complex 

## Related concepts

* [[Kontsevich formality]]

* [[Rozansky-Witten theory]]

* [[formal noncommutative symplectic geometry]] 

* [[Fulton-MacPherson operad]]


## References

Various versions of the definition of the graph complex were introduced in

* {#Kontsevich94} [[Maxim Kontsevich]], pages 11-12 of _Feynman diagrams and low-dimensional topology_, First European Congress of Mathematics, 1992, Paris, vol. II, Progress in Mathematics __120__, Birkh&#228;user (1994), 97&#8211;121 ([pdf](http://www.ihes.fr/~maxim/TEXTS/Feynman%20%20diagrams%20and%20low-dimensional%20topology.pdf))

* {#Kontsevich99b} [[Maxim Kontsevich]], around Def. 15 and Lemma 3 in _Operads and Motives in Deformation Quantization_, Lett. Math. Phys. 48 35-72, 1999 ([arXiv:math/9904055](https://arxiv.org/abs/math/9904055))

Decent review of the graph complex as a model for the [[de Rham cohomology]] of the [[Fulton-MacPherson compactification]] of [[configuration spaces of points]] (exhibiting the [[formal smooth manifold|formality]] of the [[little n-disk operads]]) is in

* {#LambrechtsVolic14} [[Pascal Lambrechts]], [[Ismar Volić]], sections 6 and 7 of _Formality of the little N-disks operad_, Memoirs of the American Mathematical Society no. 1079, 2014  ([arxiv:0808.0457](https://arxiv.org/abs/0808.0457), [doi:10.1090/memo/1079](http://dx.doi.org/10.1090/memo/1079))

further review:

* {#Fresse18} [[Benoit Fresse]], _Little discs operads, graph complexes and Grothendieck--Teichmüller groups_, in [[Haynes Miller]] (ed.) _[[Handbook of Homotopy Theory]]_ ([arXiv:1811.12536](https://arxiv.org/abs/1811.12536))


Further discussion of the graph complex as a model for the [[de Rham cohomology]] of  [[configuration spaces of points]] is in

* {#Willwacher10} [[Thomas Willwacher]], _M. Kontsevich's graph complex and the Grothendieck-Teichmueller Lie algebra_, Invent. math. (2015) 200: 671 ([arxiv:1009.1654](http://arxiv.org/abs/1009.1654))

* Najib Idrissi, _The Lambrechts-Stanley Model of Configuration Spaces_, Invent. Math, 2018 ([arXiv:1608.08054](https://arxiv.org/abs/1608.08054), [doi:10.1007/s00222-018-0842-9](https://dx.doi.org/10.1007/s00222-018-0842-9))

* {#CamposWillwacher16} [[Ricardo Campos]], [[Thomas Willwacher]], _A model for configuration spaces of points_ ([arXiv:1604.02043](https://arxiv.org/abs/1604.02043))

* {#Campos17} [[Ricardo Campos]], _Batalin-Vilkovisky formality and configuration spaces of points_, 2017 ([doi:10.3929/ethz-a-010886114](https://doi.org/10.3929/ethz-a-010886114))


* {#CamposIdrissiLambrechtsWillwacher18} [[Ricardo Campos]], Najib Idrissi, [[Pascal Lambrechts]], [[Thomas Willwacher]], _Configuration Spaces of Manifolds with Boundary_ ([arXiv:1802.00716](https://arxiv.org/abs/1802.00716))

* [[Ricardo Campos]], Julien Ducoulombier, Najib Idrissi, [[Thomas Willwacher]], _A model for framed configuration spaces of points_ ([arXiv:1807.08319](https://arxiv.org/abs/1807.08319))

See also

* {#Kontsevich99a} [[Maxim Kontsevich]], _Rozansky&#8211;Witten invariants via formal geometry_, Compositio Mathematica __115__: 115&#8211;127, 1999, [doi](http://dx.doi.org/10.1023/A:1000619911308), [arXiv:dg-ga/9704009](http://arxiv.org/abs/dg-ga/9704009)


* {#MarklShniderStasheff02} [[Martin Markl]], [[Steve Shnider]], [[James Stasheff]], _Operads in algebra, topology and physics_, Math. Surveys and Monographs __96__, Amer. Math. Soc. 2002.

* [[Andrey Lazarev]], _Operads and topological conformal field theories_, [pdf](http://www.maths.lancs.ac.uk/~lazarev/1-10.pdf); and older versio: _Graduate lectures on operads and topological field theories_, zip file with 11 pdfs, [over 5 Mb](http://www2.le.ac.uk/departments/mathematics/extranet/staff-material/staff-profiles/al179/New%20Folder.zip)

* [[Alastair Hamilton]], _A super-analogue of Kontsevich's theorem on graph homology_, Lett. Math. Phys. __76__ (2006), no. 1, 37--55, [math.QA/0510390](http://arxiv.org/abs/math/0510390)

* A. Lazarev, [[Alexander Voronov]], _Graph homology: Koszul and Verdier duality_ ([math.QA/0702313](http://arxiv.org/abs/math/0702313))

* [[Mikhail Movshev]], _A definition of graph homology and graph K-theory of algebras_ ([math.KT/9911111](http://arxiv.org/abs/math/9911111))

* [[Alberto S. Cattaneo]], Paolo Cotta-Ramusino, Riccardo Longoni, _Algebraic structures on graph cohomology_, Journal of Knot Theory and Its Ramifications, Vol. 14, No. 5 (2005) 627-640 ([doi:10.1142/S0218216505004019](http://dx.doi.org/10.1142/S0218216505004019), [math.GT/0307218](http://arxiv.org/abs/math/0307218), [MR2006g:58021](http://www.ams.org/mathscinet-getitem?mr=2006g:58021))

* [[Kiyoshi Igusa]], _Graph cohomology and Kontsevich cycles_, Topology __43__ (2004), n. 6, p. 1469-1510, [MR2005d:57028](http://www.ams.org/mathscinet-getitem?mr=2005d:57028), [doi](http://dx.doi.org/10.1016/j.top.2004.03.004)



* [[Vasily Dolgushev]], [[Christopher Rogers]], [[Thomas Willwacher]], _Kontsevich's graph complex, GRT, and the deformation complex of the sheaf of polyvector fields_ ([arxiv/1211.4230](http://arxiv.org/abs/1211.4230))

* [[Damien Calaque]], Carlo A. Rossi, _Lectures on [[Duflo isomorphism]]s in Lie algebra and complex geometry_, European Math. Soc. 2011

* [[Sergei Merkulov]], _Graph complexes with loops and wheels_, in (Manin's Festschrift:) Algebra, Arithmetic, and Geometry, Progress in Mathematics __270__ (2009) 311-354, [doi](http://dx,doi.org/10.1007/978-0-8176-4747-6_10), [pdf](http://www2.math.su.se/~sm/Papers/graph_complexes.pdf)


* [[Martin Markl]], [[Sergei Merkulov]], S. Shadrin, _Wheeled PROPs, graph complexes and the master equation_, J. Pure Appl. Algebra, 213(4):496–535, 2009, [math.AT/0610683](https://arxiv.org/abs/math/0610683)

The following survey has discussion of context between the graph complex and [[Batalin-Vilkovisky formalism]]:

* Jian Qiu, Maxim Zabzine, _Introduction to graded geometry, Batalin-Vilkovisky formalism and their applications_, [arxiv/1105.2680](http://arxiv.org/abs/1105.2680) 
* Jian Qiu, Maxim Zabzine, _Knot weight systems from graded symplectic geometry_, [arxiv/1110.5234](http://arxiv.org/abs/1110.5234) 

* [[Alastair Hamilton]], [[Andrey Lazarev]], _Graph cohomology classes in the [[BV-BRST formalism|Batalin-Vilkovisky formalism]]_, J.Geom.Phys. __59__:555-575, 2009, [arxiv/0701825](http://arxiv.org/abs/math/0701825)




[[!redirects graph complexes]]

[[!redirects graph homology]]
[[!redirects graph homology group]]
[[!redirects graph homology groups]]

[[!redirects graph cohomology]]
[[!redirects graph cohomology group]]
[[!redirects graph cohomology groups]]
