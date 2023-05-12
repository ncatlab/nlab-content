[[!redirects geometric n-category]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of manifold-diagrammatic higher categories (in some [places](#geocats) also referred to as a 'geometric' or 'geometrical' higher categories) broadly refers to [[higher categories]] whose [[composition]] [[operation]] is modelled on the [[stratified space|stratified-geometric]] notion of [[manifold diagram|manifold diagrams]]. 

## Sketch of approach

Models of [[higher categories]] are usually defined as certain collections of [[k-morphisms]] that are parametrized by (that is, [[presheaf|presheafs]] on) some category of 'combinatorial shapes': examples include presheafs of [[globular set|globular]], [[simplicial set|simplicial]] or [[opetope|opetopic]] shapes. [[manifold diagram|Manifold diagrams]], while defined in geometric terms, admit a combinatorialization in terms of [[n-truss|trusses]] (or, more precisely, [[trusses#comb_mdiag|combinatorial manifold diagrams]]) and can therefore be used as combinatorial shapes for defining higher categories as presheafs on them. Importantly, combinatorial manifold diagrams come with a rich class of combinatorial mappings which (in contrast to most other classes of shapes) include internal representations of both 'embeddings' (='face and degeneracy' maps, up to geometric dualization) as well as 'quotients' (='subdivisions', up to geometric dualization). We give geometric insight into these classes below, but ultimately only care about their combinatorial definitions.


### Embeddings of manifold diagrams

*Embeddings* of manifold $n$-diagrams are [[manifold diagram#framed_map_euclidean_case|framed]] [[stratified space|stratified maps]] whose underlying maps are [[subspace|embeddings]] of spaces (this is different from the notion of [[stratified space#stratified_map_types|substratifications]]). The next figure illustrates mappings in this class (in dimension $n = 2$).

<center>
<figure>
  <img src="https://ncatlab.org/nlab/files/mdiag_inclusions_and_coarsenings_v2.svg" alt="" style="width:90%; max-width: 600px; height:auto;">
<figcaption>Figure 1: Embeddings of manifold diagrams (for which <i>substratifications</i> and <i>coarsenings</i> form a factorization system).</figcaption>
</figure>
</center>

Geometric dualization unveils that embeddings of manifold diagrams are precisely 'cellular' maps of their dual framed cell complexes ('cellular' is usually meant to imply that maps map closed cells to closed cells), which can be seen to have an [[(epi,mono) factorization system]] by degeneracy and face maps. The next figure illustrates this: the shown maps are precisely the the geometric duals of the maps in the previous figure.

<center>
<figure>
  <img src="https://ncatlab.org/nlab/files/mdiag_faces_and_degeneracies_v4.svg" alt="" style="width:90%; max-width: 600px; height:auto;">
<figcaption>Figure 2: Geometric duals of embeddings are cellular maps (for which <i>face</i> and <i>degeneracy</i> maps form a factorization system)</figcaption>
</figure>
</center>

Combinatorially, embeddings of combinatorial manifold diagrams $T,S$ are described by [[spans]] of the form

\begin{center}
\begin{tikzcd}
        T & {T'} & S
        \arrow["{\mathsf{norm}}"', from=1-2, to=1-1]
        \arrow[hook, from=1-2, to=1-3]
\end{tikzcd}
\end{center}

where $T' \xrightarrow{\mathsf{norm}} T$ is a [[n-truss#normalizing_map|normalizing map]] and $T' \hookrightarrow S$ is map of labeled trusses whose underlying map is a [[n-truss#n-truss_bundle_map|regular]] inclusion. Such spans can be composed by [[pullback]].



### Quotients of manifold diagrams

*Quotients* of manifold diagrams are [[manifold diagram#framed_map_euclidean_case|framed]] stratified maps whose underlying maps are [[quotient space|quotient maps]]. The next figure illustrates mappings in this class (in dimension $n = 2$).

<center>
<figure>
  <img src="https://ncatlab.org/nlab/files/mdiag_quotients_v2.svg" alt="" style="width:90%; max-width: 600px; height:auto;">
<figcaption>Figure 3: Quotients of manifold diagrams are the <i><a href="https://ncatlab.org/nlab/show/n-truss#duality">categorically dual notion</a></i> to embeddings.</figcaption>
</figure>
</center>

Geometric dualization unveils that quotients of manifold diagrams correspond to subdivisions of framed cell complexes. The next figure illustrates the geometric duals of the quotient maps in the preceding figure.

<center>
<figure>
  <img src="https://ncatlab.org/nlab/files/mdiag_subdivisions_v2.svg" alt="" style="width:90%; max-width: 600px; height:auto;">
<figcaption>Figure 4: The geometric duals of quotients are subdivisions.</figcaption>
</figure>
</center>

Combinatorially, quotients of combinatorial manifold diagrams $T, S$ are maps of labeled trusses

$$
    T \twoheadrightarrow S
$$

whose underlying map of trusses is a [[n-truss#n-truss_bundle_map|singular]] quotient map.

\begin{rmk} To summarize: while the notion embeddings of manifold diagrams recovers (after geometric dualization) face and degeneracy maps often found in the combinatorics of shapes, in contrast, the notion of quotients dual to that of embeddings captures (after geometric dualization) something new: namely, subdivisions of cells. This is quite powerful e.g. for describing compositions as we will exploit below.(Moreover, it turns out that classifying subdivisions is generally a difficult (undecidable) problem, see e.g. [Dorn-Douglas 2021](#DornDouglas21), so it is convenient that it can be easily solved in the setting of manifold diagrams!) \end{rmk}

### Sketch Definition


Together (and, henceforth, working purely combinatorially), embeddings and quotients organize into the *[[double category]] $\mathbb{M}\mathsf{Diag}_n$ of combinatorial manifold $n$-diagrams*, with horizonal morphisms being embeddings, vertical morphisms being quotients, squares being commuting diagrams of the following form:

\begin{center}
    \begin{tikzcd}
        {T_1} & {T'_1} & {S_1} \\
        {T_2} & {T'_2} & {S_2}
        \arrow["{\mathsf{norm}}"', from=1-2, to=1-1]
        \arrow[hook, from=1-2, to=1-3]
        \arrow["{\mathsf{norm}}"', from=2-2, to=2-1]
        \arrow[hook, from=2-2, to=2-3]
        \arrow[two heads, from=1-1, to=2-1]
        \arrow[two heads, from=1-3, to=2-3]
        \arrow[dashed, two heads, from=1-2, to=2-2]
    \end{tikzcd}
\end{center}

(note that the dashed arrow is unique if it exists.) The *category of manifold $n$-diagrams* $\mathsf{MDiag}_n$ will refer to just the horizontal part of this double category.

When defining higher categories parametrized by manifold $n$-diagrams, we would want higher categories to be compatible both with embeddings ('morphism attachment') and quotients ('morphism composition') in the following sense. 

{#SketchDefinition} ***Sketch definition***. A *manifold diagrammatic $n$-category* $\mathcal{C}$ should be a presheaf on $\mathsf{MDiag}_n$ subject to the following two conditions.

1. The collection of morphisms parametrized by a given diagram should be determined by subdiagrams that [[cover]] it. Formally, this can be enforced by an appropriate [[sheaf]] condition.
2. The composition of a given diagram should be compatible with the composition of its subdiagrams. Formally, this can be enforced by requiring that $\mathcal{C}$ extends to a double-(co)presheaf $\mathbb{M}\mathsf{Diag}^{\mathrm{op},\mathrm{co}}_n \to \mathbb{S}\mathbf{et}$ (covariant in the vertical part, where $\mathbb{S}\mathbf{et}$ is the double category of [[double category#examples|squares]] $\mathrm{Sq}(\mathbf{Set})$ in [[Set]])).

\begin{rmk} (Coherence conditions). What's worth pointing out about the above definition sketch is that there are no explicit higher-categorical coherence conditions (like [[Kan complex#KanComplexes|filler]] or [[Segal condition|Segal]] conditions) beyond ordinary sheaf conditions. This is because coherences can be expressed internally to the category of manifold diagrams (namely, as so-called 'manifold-diagram [[isotopies]]' including, for instance, a [[braiding]]).
\end{rmk}

{#mdiag_infty}
\begin{rmk} \label{mdiag_infty} (The $n = \infty$ case). So far we worked with $n$-diagrams for fixed finite $n \in \mathbb{N}$ which work well as parametrizing objects for $n$-categories. However, we can also address the case $n = \infty$ as follows. Given a manifold $n$-diagram $f$, note that $f \times \mathbb{R}$ is a manifold $(n+1)$-diagram. This defines a chain of inclusions of (ordinary resp. double) categories, the colimit of which is a category of manifold diagrams $\mathsf{MDiag}$ (resp. the double category $\mathbb{M}\mathsf{Diag}$) which may then be used to parametrized $(\infty,\infty)$-categories via the sketch definition above.
\end{rmk}

### Variants

Instead of considering presheafs on combinatorial manifold diagrams, one may also consider

* presheafs on (unlabeled) [[n-truss|trusses]]
* presheafs on (unlabeled) [[n-truss##atomic_trusses_terminology|atomic trusses]]

with various sheaf conditions in place. In both cases, faces, degeneracies and compositions may be understood via mappings as outlined above. The potential advantage of dropping labelings from our parametrizing objects in this way (i.e. considering trusses in place of labeled trusses) is simplicity. For instance, an immediate simplification is that we can work with truss maps instead of spans of truss maps when combinatorially modelling embeddings. This could simplify the comparison to other presheaf models of higher categories.

Another related, potentially useful observation is that the spans occurring in the definition of the category of manifold diagrams may be expressed concisely in terms of bundles (slightly generalizing the notion of labeled [[trusses|truss bordism]]).

Several other approaches to and variations of the idea of manifold-diagrammatic higher categories are currently under consideration. The categories of combinatorial shapes considered here (whether combinatorial manifold diagrams, or (atomic) trusses, or similar) often have peculiarities that one doesn't encounter in other settings (e.g. failure to be a [[Reedy category]] due to the novel concept of normalizing maps). The precise nature of these shape categories remains to be fully understood.

## Examples

* [[geometric computad|Geometric computads]] are [[free object|free]] instances of manifold-diagrammatic $n$-categories.

* [[associative n-category|Associative $n$-categories]] are, in an extended sense, instances of manifold diagrammatic $n$-categories (and, in fact, their combinatorics precedes some of the stratified-geometric ideas of manifold-diagrammatic $n$-categories). 

\begin{rmk} (Globular sets in associative $n$-categories). Note that associative $n$-categories use [[globe|globular shapes]] as parametrizing objects rather than manifold diagrams. This can be related to the above discussion as follows. Using Rmk. \ref{mdiag_infty}, denote by $\mathsf{MDiag^{st}}$ the category of ('strictly globular') manifold diagrams with source/target inclusions as maps, and by $\mathsf{Glob}$ the [[globe category]]. Then there is a retraction $\mathsf{Glob} \hookrightarrow \mathsf{MDiag^{st}}$ (which maps $n$ as the 'terminal' manifold $n$-diagram, namely, the geometric dual of the $n$-globe) and $\mathsf{MDiag^{st}} \to \mathsf{Glob}$ (which maps an $n$-manifold diagram to the $n$-globe). This retraction can be used to '*work with [[globular sets]] whose composition is defined via manifold diagrams*'.
\end{rmk}


## Remarks

* {#coherence_paradigm} As mentioned above, [[coherence law|coherences]] in manifold-diagrammatic categories derive from isotopies of manifold diagrams. This provides a different mechanism for coherence construction than the mechanism found in many existing, spatially-inspired models of [[higher categories]] (which create coherences by enforcing contractibility of 'spaces of composites'). The conceptual difference between the two mechanisms is discussed in more detail in this [blog post](https://cxdorn.github.io/research/paradigms-of-higher-cats/).

* {#geocats} Manifold-diagrammatic categories have also been referred to 'geometric higher categories' or 'geometrical higher categories', based on a distinction of 'geometric', 'topological' and 'combinatorial' models of higher structures as explained [here](https://golem.ph.utexas.edu/category/2023/03/an_invitation_to_geometric_hig.html). See also [here](https://nforum.ncatlab.org/discussion/16159/geometric-ncategory/#Item_10) for a relevant discussion about terminology.


## Related concepts

* [[manifold diagram|manifold $n$-diagrams]]

* [[n-mesh|meshes]]

* [[n-truss|trusses]]

* [[directed topological space|directed topological spaces]]

* [[stratified space|stratified spaces]]

* [[higher category theory]]

## References

An introduction to and overview of some relevant ideas in the area can be found in:

* {#NCC} [An Invitation to Geometric Higher Categories](https://golem.ph.utexas.edu/category/2023/03/an_invitation_to_geometric_hig.html), $n$-Category Café post

with further details spelled out in:

* {#Dorn23} [[Christoph Dorn]], _Nine short stories about geometric higher categories_, 2023 ([pdf](https://cxdorn.github.io/assets/pdfs/nine-stories.pdf))

The type of 'directed combinatorial topology' that governs the stratified topology of manifold diagrams was described in:

* {#DornDouglas21} [[Christoph Dorn]] and [[Christopher Douglas]], _Framed combinatorial topology_, 2021 ([arXiv](https://arxiv.org/abs/2112.14700), [latest](https://cxdorn.github.io/fct-book/))


[[!redirects manifold-diagrammatic n-categories]]
[[!redirects manifold-diagrammatic higher category]]
[[!redirects manifold-diagrammatic higher categories]]
[[!redirects manifold-diagrammatic higher category theory]]

[[!redirects geometric n-category]]
[[!redirects geometric n-categories]]
[[!redirects geometric higher category]]
[[!redirects geometric higher categories]]
[[!redirects geometric higher category theory]]
[[!redirects geometrical n-category]]
[[!redirects geometrical n-categories]]
[[!redirects geometrical higher category]]
[[!redirects geometrical higher categories]]
[[!redirects geometrical higher category theory]]

[[!redirects geometric category]]
[[!redirects geometrical category]]