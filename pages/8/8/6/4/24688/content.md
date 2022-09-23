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

Several definitional variants exist in dimensions $\leq 4$ (see also at [[surface diagram|surface diagrams]]). In general dimensions, manifold diagrams can be defined as the local models of conical cellulable stratifications on [[directed topological space|directed spaces]].

\begin{defn} A **manifold $n$-diagram** is a conical cellulable stratification of standard $n$-dimensional directed space.
\end{defn}

In the definition, note:

* the term "standard" is another way of saying "local model" (concretely, we can take this to be [[directed topological space#framed_spaces|standard $\mathbb{R}^n$ with standard directions]]),
* the term "cellulable" refers to a directed variation of usual [[stratified space#rmk_cellulable|cellulability]]; namely, one requires the stratification to have a subdivision by regular topological directed cells,
* the term "conical" means a directed version of usual [[stratified space#conical_strat|conicality]]; namely, in the context of directed spaces one requires tubular neighborhoods to interact nicely with the directions of the underlying directed space.

A more detailed description of the situation can be found in [Dorn and Douglas 22](#DornDouglas22) and [Dorn and Douglas 22B](#DornDouglas22B). Note that, "cellulable" is also called "meshable", or "tame".


## References

* {#BaezDolan95} [[John Baez]] and [[James Dolan]], _Higher-dimensional Algebra and Topological Quantum Field Theory_ 1995 ([arXiv](http://arxiv.org/abs/q-alg/9503002))

* {#Carter} Scott Carter, _An excursion in diagrammatic algebra_, 2012

* {#DornDouglas22} Christoph Dorn and Christopher Douglas, _Manifold diagrams and tame tangles_, 2022 ([pdf](https://cxdorn.github.io/assets/pdfs/mdiag_latest.pdf))

* {#DornDouglas22B} Christoph Dorn and Christopher Douglas, _A brief introduction to framed combinatorial topology_, 2022 ([pdf](https://cxdorn.github.io/assets/pdfs/fctintro_latest.pdf))