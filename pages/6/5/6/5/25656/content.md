[[!redirects meshes]]
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

Meshes are towers of [[stratified space#constructible_strat_bun|constructible]] [[stratified space#stratified_bundle|stratified bundles]] whose fibers are points or [[framing|framed]] stratified 1-manifolds. Meshes play a central role in the local description of directed (namely, [[directed space#framed_spaces|framed]]) regular [[cell complex|cell]] and [dual-cell](https://en.wikipedia.org/wiki/Poincar%C3%A9_duality#Dual_cell_structures) complexes.

## Definition

Meshes are certain [[stratified space|stratified spaces]] with additional [[structure]] (namely, structure that records spatial [[directed space|directions]] via a notion of [[directed space#framed_spaces|framings]]). In the following definition, framings can be understood in the [[framing|ordinary sense]].

\begin{defn} A _1-mesh_ is a framed [[contractible]] $k$-[[manifold]] $M$, $k \leq 1$, together with a [[stratification]] $f$ on $M$ whose strata are open $l$-disks, $l \leq 1$.
\end{defn}

Contractability implies that any 1-mesh framed embeds in standard framed $\mathbb{R}$: we call such embeddings _mesh-trivializations_.

To prepare for the definition of a bundle of 1-meshes, recall, the [[stratified space#fundamental_categories|fundamental $\infty$-category]] functor $\mathcal{E} : \mathcal{S}\mathit{trat} \to \mathbf{Cat}_\infty$ maps [[stratified space#conical_strat|conical stratifications]] to their fundamental [[∞-categories]]: for defining the latter, we work with [[stratified space#exit_entrance_conv|entrance paths]] (which is the opposite convention to working with [[stratified space#exit_entrance_conv|exit paths]]). 

\begin{rmk} For simplicity, below one can replace the [[(infinity,1)-functor|$\infty$-functor]] $\mathcal{E}$ with the ordinary fundamental *[[poset]]* [[functor]] $\mathsf{E}$. This yields an equivalent definition of $n$-meshes (even though the definition of $n$-mesh *bundles* will differ).
\end{rmk}

The following definition abstractly characterizes bundles of 1-meshes (see Rmk. \ref{rmk_mesh_bundles_concrete} for an elaboration). We assume all stratifications to be conical.

\begin{defn} A _1-mesh bundle_ $p : (M,f) \to (B,g)$ is a [[stratified space#stratified_bundle|stratified bundle]] with 1-mesh fibers $(M_x, f_x)$, for $x \in B$, and a fiberwise mesh-trivializing bundle embedding $p \hookrightarrow (\pi_B : B \times \mathbb{R} \to B)$ into the trivial $\mathbb{R}$-bundle over $B$, such that

1. $\mathcal{E}(p)$ is an [[Conduché functor|exponentiable fibration]],
2. $\mathcal{E}(p_{(0)})$ is an [[Grothendieck fibration#opfibrations_and_bifibrations|opfibration]],
3. $\mathcal{E}(p_{(1)})$ is a [[Grothendieck fibration|fibration]],

where $p_{(i)}$ denotes the restriction of $p$ to the union of strata in its domain whose non-empty intersections with fibers are all of dimension $i$.
\end{defn}

\begin{rmk} \label{rmk_mesh_bundles_concrete} A concrete way to think about 1-mesh bundles is explained in [Dorn-Douglas 2021, Ch. 4](#DornDouglas21): a 1-mesh bundle $p$ is a stratified bundle of 1-meshes that can be trivialized in the trivial framed line bundle, such that the image of the trivialization has continuous upper and lower fiberwise bounds, and such that entrance paths $b \to b'$ in the base, with $p(x) = b$ for $x$ a point in a $0$-stratum in the fiber over $b$, have unique lifts to entrance paths $x \to x'$.
\end{rmk}

\begin{defn} An _$n$-mesh bundle_ $M$ over a base stratification $(B,g)$ is a tower of 1-mesh bundles
$$
    (M_n, f_n) \to (M_{n-1}, f_{n-1}) \to ... \to (M_1, f_1) \to (M_0,f_0) = (B,g)
$$
If $(B,g) = \ast$ is the trivial stratification then the $n$-mesh bundle is simply called an _$n$-mesh_ $M$.
\end{defn}

\begin{rmk} There are several equivalent phrasings and variations of the definitions of 1- and $n$-mesh bundles. For instance, the assumption of contractability in the definition of 1-meshes can be weakened.
\end{rmk}

\begin{terminology} \label{closed_and_open_meshes} An $n$-mesh $M$ is call _closed_ if $M_n$ is [[compact]], and _open_ if $M_n \cong \mathbb{R}^n$.
\end{terminology}

\begin{defn} An _$n$-mesh map_ $F : M \to N$ is a stratified map of towers that fiberwise preserves the framing. (In fact, this makes mesh maps framed maps in the sense of [[directed topological space#framed_spaces|framed directed spaces]].)
\end{defn}


## Properties

### Cell structures

Closed meshes are regular cell complexes (cf. [Wikipedia entry](https://en.wikipedia.org/wiki/CW_complex#Regular_CW_complexes)). More generally, meshes $M$ are [[stratified space#fundamental_categories|stratified $0$-types]] (meaning the fundamental $\infty$-categories $\mathcal{E}(M_i,f_i)$ are $0$-[[truncated]] as $\infty$-categories, i.e. equivalent to [[posets]]).

### Classification

The fundamental categories $\mathcal{E}(M) = \mathcal{E}(f_n \to f_{n-1} \to ... \to f_0)$ of meshes are certain towers of poset maps 'with structure': this gives rise to a combinatorial notion called [[trusses]]. In fact, $n$-meshes up to framed stratified homeomorphism are classified by $n$-trusses (see [[n-truss#combinatorial_meshes|at trusses]] for details), and $n$-mesh bundles up to bundle isomorphism are classified by $n$-truss bundles (and thus share the same [[n-truss#truss_bundle_classifications|classifying category]]).

### Duality

As a consequence of [[n-truss#duality|truss duality]] and of the classification of meshes by trusses, we obtain a involutive [[dualization]] endofunctor on the category of meshes. This functor can be understood as a geometric dualization operation in the sense of [[Poincare duality]]. It maps open to closed meshes and vice versa (see Trm. \ref{closed_and_open_meshes}).


## Related concepts

* [[n-truss|n-trusses]]

* [[manifold diagrams]]

* [[framed combinatorial topology]]

## References

* {#DornDouglas22} [[Christoph Dorn]] and [[Christopher Douglas]], _Manifold diagrams and tame tangles_, 2022 ([arXiv](https://arxiv.org/abs/2208.13758), [latest](https://cxdorn.github.io/manifold-diagram-paper/))

* {#DornDouglas21} [[Christoph Dorn]] and [[Christopher Douglas]], _Framed combinatorial topology_, 2021 ([arXiv](https://arxiv.org/abs/2112.14700), [latest](https://cxdorn.github.io/fct-book/))

[[!redirects mesh]]
[[!redirects meshes]]