# Contents
* automatic toc
{: toc}

## Idea

*Manifold $n$-diagrams* generalize [[string diagram|string diagrams]] to higher dimensions---they recover string diagrams in dimension $n = 2$. For $n = 3$, they specialize to the notion of [[surface diagram|surface diagrams]].

The idea of manifold diagrams has its roots in the relation between [[stratified space|stratified]] [[manifold|manifolds]] and [[higher category theory|higher categories]]. One way to think about this relation is by noting that stratified manifolds arise after dualizing (in the sense of [[Poincaré duality]]) [[pasting diagram|pasting diagrams of directed cells]] in higher categories.

A well-known instance of this relation materializes in the [[generalized tangle hypothesis]]: indeed, [[tangle|tangles]] can (in a canonical way) be regarded as examples of manifold diagrams.

<center>
<figure>
  <img src="https://ncatlab.org/nlab/files/some_tangles_Baez_Dolan.png" alt="" style="width:90%; max-width: 500px; height:auto;">
<figcaption>Figure 1: m-Tangles in dimension n can be regarded as manifold diagrams (picture reproduces part of Fig. 30 in <a href="#BaezDolan95">BaezDolan95</a>); note that k = n-m is the codimension of the tangle).</figcaption>
</figure>
</center>

From the perspective of the tangle hypothesis, manifold diagrams can be used to express the structure of coherently dualizable objects. More precisely, this translates between "manifold singularities" and relations satisfied by the higher morphisms associated to a coherently dualizable objects. For instance, the manifold diagram in Figure 2 expresses the "swallowtail identity" satisfied by [[biadjunction|coherent biadjunctions]] (this is a _manifold 4-diagram_: think about the two surfaces as embedded in 3-dimensional space, and in the 4th spatial dimension we deform the top surface into the bottom one). The terminology derives from Thom's classification of classical singularities (cf. [this picture](https://mathworld.wolfram.com/SwallowtailCatastrophe.html)).

<center>
<figure>
  <img src="https://ncatlab.org/nlab/files/swallow_tail_MSRI_cropped.jpeg" alt="" style="width:90%; max-width: 500px; height:auto;">
<figcaption>Figure 2: The swallowtail identity as a manifold 4-diagram (reproducing the title image of <a href="https://www.msri.org/programs/323">MSRI program 323: higher categories and categorification</a>).</figcaption>
</figure>
</center>

Many other interesting categorical and [[higher algebra|higher-algebraic identities]] can be expressed in manifold diagrams in a similar way. As an example, the [Yang–Baxter equation](https://en.wikipedia.org/wiki/Yang%E2%80%93Baxter_equation) (or, relatedly, the Reidemeister moves) can be expressed in manifold 4-diagrams as well, see Figure 3.

<center>
<figure>
  <img src="https://ncatlab.org/nlab/files/yang_baxter_movie.png" alt="" style="width:90%; max-width: 500px; height:auto;">
<figcaption>Figure 3: The Yang-Baxter identity as a manifold 4-diagram, illustrated as movie of 1-tangles in dimension 3 read from left to right.</figcaption>
</figure>
</center>

In higher dimensions the types of identites become more and more complicated: Figure 4 shows a _manifold 5-diagram_ representing the [Zamolodchikov tetrahedron equation](https://blogs.ams.org/visualinsight/2016/03/15/zamolodchikov-tetrahedron-equation/)). Much diagrammatic algebra of surfaces along these lines as been developed by [Carter](#Carter) and collaborators.

<center>
<figure>
  <img src="https://ncatlab.org/nlab/files/zamolodchikov_tetrahedron.jpg" alt="" style="width:90%; max-width: 500px; height:auto;">
<figcaption>Figure 4: The Zamolodchikov tetrahedron equation as a manifold 5-diagram, illustrated as a movie from left to right (but the movie only has 2 frames).</figcaption>
</figure>
</center>

Manifold diagrams are meant to provide a definitional framework for higher algebraic laws such as those above in _all_ dimensions. Moreover, while the above examples only illustrate such laws for tangles (i.e. for embedded ordinary manifolds), in full generality manifold diagrams are diagrams of [[stratified space|stratified]] [[manifold|manifolds]].


## Definition 

### Outline

Several definitional variants exist in dimensions $\leq 4$ (see also at [[surface diagram|surface diagrams]]). In general dimensions, manifold diagrams (introduced in [Dorn-Douglas 2022](#DornDouglas22)) can be defined as conical, compactly triangulable stratifications of [[directed topological space|directed euclidean space]].

\begin{defn} A **manifold $n$-diagram** is a conical, compactly triangulable stratification of standard $n$-dimensional directed space.
\end{defn}

Here, "standard directed space" can be taken to mean [[directed topological space#framed_spaces|standard $\mathbb{R}^n$ with standard $n$-framing]]. The term "conical" means a directed version of usual [[stratified space#conical_strat|conicality]]; namely, in the context of directed spaces one requires tubular neighborhoods to interact nicely with the directions of the underlying directed space. "Compact triangulability" means, roughly, that up to isomorphism a description by finite data can be given.


### Details

We provide details for the preceding definition.

\begin{defn} The _standard $n$-framing_ of $\mathbb{R}^n$ is the chain of oriented $\mathbb{R}$-fiber bundles $\pi_i : \mathbb{R}^i \to \mathbb{R}^{i-1}$ ($1 \leq i \leq n$) with $\pi_i$ defined to be the map that forgets the last coordinate of $\mathbb{R}^i$ (and fibers carry the standard orientation of $\mathbb{R}$ after identifying $\mathbb{R}^i = \mathbb{R}^{i-1} \times \mathbb{R}$).
\end{defn}

When considering $\mathbb{R}^n$ we tacitly always think of it as 'standard framed $\mathbb{R}^n$' and, thus, we stop mentioning the standard framing as an explicit structure all-together. Indeed, more important than defining the standard $n$-framing is to define the maps that preserve it.

{#framed_map_euclidean_case}
\begin{defn} A _framed map_ $F : \mathbb{R}^n \to \mathbb{R}^n$ is a map for which there exist (necessarily unique) maps $F_j : \mathbb{R}^j \to \mathbb{R}^j$ ($0 \leq j \leq n$) with $F_n = F$ such that $\pi_i \circ F_i = F_{i-1} \circ \pi_i$ with $F_i$ preserving orientations of fibers of $\pi_i$ (i.e. mapping fibers strictly monotously).
\end{defn}

A framed _stratified_ map $(\mathbb{R}^n,f) \to (\mathbb{R},g)$ is a [[stratified space#the_category_of_stratifications|stratified map]] whose underlying map $\mathbb{R}^n \to \mathbb{R}^n$ is framed. Moreover, when working with products $(\mathbb{R}^k,f) \times (\mathbb{R}^{n-k}, g)$ we will identitify $\mathbb{R}^n \cong \mathbb{R}^k \times \mathbb{R}^{n-k}$ in the standard way; and, when working with [[stratified space#conical_strat|cone stratifications]] $(\mathrm{Cone}(S^{n-1}), \mathrm{cone}(l))$, we will standard embed $S^{n-1} \into \mathbb{R}^n$ and identify $\mathrm{Cone}(S^{n-1}) \cong \mathbb{R}^n$ by mapping $(x \in S^{n-1},\lambda \in [0,1))$ to $\frac{\lambda}{1 - \lambda}x \in \mathbb{R}^n$.

\begin{defn} A stratification $(\mathbb{R}^n,f)$ is _framed conical_ if each point $x \in \mathbb{R}^n$ it has a framed stratified neighborhood (framed) homeomorphic to $\mathbb{R}^k \times (\mathrm{Cone}(S^{n-k-1}), \mathrm{cone}(l))$ with $x \in \mathbb{R}^k \times \{0\}$, where $0 \leq k \leq n$ and $(S^{n-1}, l)$ is some stratification.
\end{defn}

\begin{defn} A _compactly-described triangulation_ $K$ of $\mathbb{R}^n$ is a finite stratification of $\mathbb{R}^n$ by open disks whose closures are the images of [linear embeddings](https://math.stackexchange.com/questions/1326711/what-is-a-linear-embedding-from-a-simplex-deltan-to-mathbbrn) $\Delta^k \times \mathbb{R}^l_{\geq 0} \into \mathbb{R}^n$ ($k + l \leq n$). This now translates to the framed stratified case as follows: a stratification $(\mathbb{R}^n,f)$ is _framed compactly triangulable_ if it admits a framed stratified subdivision $(\mathbb{R}^n,K) \to (\mathbb{R}^n,f)$ of $f$ by a compactly-described triangulation $K$.
\end{defn}

We can now put these concepts together to obtain the following form definition of manifold diagrams.

\begin{defn}(Formalization of earlier sketch). A **manifold $n$-diagram** is a framed conical, framed compactly triangulable stratification of $\mathbb{R}^n$.
\end{defn}

The natural 'isomorphism' relation of manifold diagrams is framed stratified homeomorphism.


## Properties

The definition has several important consequences, which we list in this section. These consequences have been formally worked out in [Dorn and Douglas 22](#DornDouglas22). (Note the primary definition in the latter text differs from that given here, but a comparison is given.)

### Combinatorialization theorem

While the compact triangulability condition requires the existence of _some_ combinatorial representation, there is in fact a _canonical_ combinatorial representation for isomorphism classes of manifold diagrams. This leads to a theory of combinatorial objects called [[n-truss|trusses]]. The full 'combinatorialization theorem' is spelled out [[n-truss#manifold_diagram_classification|here]].

### Framed smooth structure of strata

Strata in manifold diagrams are, indeed, manifolds. Moreover, they have canonical smooth structures. This follows since manifold strata carry canonical PL structure, and are canonically framed, and since framed PL manifolds have unique compatible framed smooth structure.

### Well-definedness of links

Links of tubular neighborhoods in manifold diagrams are in fact well-defined. That is, there is, up to isomorphism, a unique choice of link. This stands in contrast to classical topological conical stratifications, where non-homeomorphic choices of links exist.

### Dual cellular theory of manifold diagrams

Manifold diagrams have canonical geometric duals (in the sense of Poincaré duality). This relates manifold diagrams to 'diagrams of directed cells' in the sense of classical [[pasting diagram|pasting diagrams]] (but with  cell shapes that generalize many common classes of shapes such as 'globular', 'simplicial', or 'opetopic' shapes). Details are spelled out in [Dorn and Douglas 22, Sec. 2.4](#DornDouglas22).

## Related concepts

* [[n-truss]]

* [[n-mesh]]

* [[manifold-diagrammatic n-category]]

* [[homotopy.io]]

* [[directed topological space]]


## References

* {#BaezDolan95} [[John Baez]] and [[James Dolan]], _Higher-dimensional Algebra and Topological Quantum Field Theory_, 1995 ([arXiv](http://arxiv.org/abs/q-alg/9503002))

* {#Carter} [[Scott Carter]], _An excursion in diagrammatic algebra_, 2012, World Scientific ([doi:10.1142/8315](https://doi.org/10.1142/8315))

* {#DornDouglas22} [[Christoph Dorn]] and [[Christopher Douglas]], _Manifold diagrams and tame tangles_, 2022 ([arXiv](https://arxiv.org/abs/2208.13758), [latest](https://cxdorn.github.io/manifold-diagram-paper/))

* {#Dorn23} [[Christoph Dorn]], _Nine short stories about geometric higher categories_, 2023 ([pdf](https://cxdorn.github.io/assets/pdfs/nine-stories.pdf))

Brief introductions:

* *From zero to manifold diagrams*, TallCat Seminar Talk, ([video](https://www.youtube.com/watch?v=67RAzY-13r4))

* *[An Invitation to Geometric Higher Categories](https://golem.ph.utexas.edu/category/2023/03/an_invitation_to_geometric_hig.html)*, $n$-Category Café post


* [[Christoph Dorn]], *Manifold Diagrams -- A Brief Report*, [talk at](https://ncatlab.org/nlab/show/Center+for+Quantum+and+Topological+Systems#DornNov2023) [[CQTS]] (15 Nov 2023) &lbrack;[[Dorn-ManifoldDiagramsReport.pdf:file]]&rbrack;




[[!redirects manifold diagrams]]

