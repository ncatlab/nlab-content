

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}



## Idea

A *Riemannian immersion* or *isometric immersion* of [[Riemannian manifolds]] is an [[immersion]] $\Sigma \hookrightarrow X$ of their [[underlying]] [[smooth manifolds]] which is also an [[isometry]] with respect to their [[Riemannian metrics]].

Similarly, an *isometric embedding* is an isometric immersion which is also an [[embedding of smooth manifolds]], hence [[embedding of topological spaces|of the underlying topological spaces]].

The *isometric immersion/embedding problem* is to find isometric immersions/embeddings of Riemannian manifolds into large-dimensional but flat ([[Euclidean spaces|Euclidean]]) spaces (e.g. [Han & Hong 2006](#HanHong06), [Han & Lewicka 2023](#HanLewicka23)).



## Properties

### Adapted Darboux (co-)frames
 {#AdaptedDarbouxCoframes}

Given a [[Riemannian manifold]] $(X,g)$ of [[dimension of a manifold|dimension]] $D$, then 

* an **orthonormal local frame** is an [[open cover]] $p \colon \widehat{X} \twoheadrightarrow X$ equipped with a $D$-[[tuple]] of [[vector fields]]

  $$
    V
    \;\colon\;
    \mathbb{R}^{D} \xrightarrow{\;\;} T \widehat X
  $$

  such that at each point $\widehat x \,\in\, \widehat{X}$ we have that

  $$
    g\big(V,V\big)(x)
  $$

  is the canonical [[inner product]] on $\mathbb{R}^D$, hence in components

  $$
    g\big(V_a, V_b\big)(x)
    \;=\;
    \delta_{a b}
    \,;
  $$

* an **orthonormal local co-frame** is an [[open cover]] $p \colon \widehat{X} \twoheadrightarrow X$ equipped with a $\mathbb{R}^D$-valued [[differential 1-form]]

  $$
    E
    \;\colon\;
    T\widehat{X}
    \xrightarrow{\;\;}
    \mathbb{R}^D
  $$

  such that at each point $\widehat x \,\in\, \widehat{X}$ we have

  $$
    \delta_{a b} \, E^a \otimes E^b
    \;=\;
    g
    \,.
  $$

Now given moreover an [[immersion]] $\phi \colon \Sigma \hookrightarrow X$ into a [[Riemannian manifold]]

* such an orthonormal local frame $V$ is called *adapted* or *Darboux* (generalizing terminology originating in the [[differential geometry of curves and surfaces]], cf. [Guggenheimer 1977, p. 210](#Guggenheimer77)) for $\phi$ if for each $\sigma \in \Sigma$ and each lift $\widehat{\phi(\sigma)} \in \widehat{X}$ of $\phi(\sigma) \in X$ its first $dim(\Sigma)$ components are tangent to $\Sigma$:

  \[
    \label{DarbouxFrameProperty}
    \underset
      { a \leq dim(\Sigma) }
      {\forall}
    \;\;\;\;\;
    V_a(\sigma) 
      \,\in\, 
    T_\sigma \Sigma
      \subset
    T_{\widehat{\phi(\sigma)}} \widehat{X}
  \]

  ([Sternberg 1964, Def. 2.1 on p. 244](#Sternberg64); [Griffiths & Harris 1979 (1.12)](#GriffithsHarris79); [Berger, Bryant & Griffiths 1983, p. 818](#BergerBryantGriffiths83))

* such an orthonormal local co-frame $E$ is called *adapted* or *Darboux* for $\phi$ if its last $dim(X)-dim(\Sigma)$-components are transversal to $\Sigma$:

  \[
    \label{DarbouxCoFrameProperty}
    \underset
      { a \gt dim(\Sigma) }
      {\forall}
    \;\;\;\;\;
    \phi^\ast E^a
    \;=\;
    0
  \]
  
  ([Sternberg 1964, (2.11) on p. 246](#Sternberg64); [Zandi 1988, p. 426](#Zandi88); [Mastrolia, Rigoli & Setti 2012, Def. 1.17](#MastroliaRigoliSetti12); [Giron 2020, §3.2.2](#Giron20); [Chen & Giron 2021, §2.4](#ChenGiron21))

\begin{remark}
  \label{DarbouxCoFramePullingBackToCoframeOnImmersedManifold}
  The Darboux co-frame property (eq:DarbouxCoFrameProperty) immediately implies that the pullback of the remaining frame components 
$$
  e
  \;\coloneqq\;
  \big(
    e^a 
    \;\coloneqq\;
    \phi^\ast E^a
  \big)_{
    a \leq dim(\Sigma)  
  }
$$
is a local frame on $\Sigma$. We may summarize this by saying that a local Darboux co-frame $E$ gives
\[
  \label{DarbouxCoframePullsBackToCoframe}
  \phi^\ast E^a 
  \;=\;
  \left\{
  \begin{array}{ll}
    e^a & \text{for}\; a \leq dim(\Sigma)
    \\
    0 & \text{for}\; a \geq dim(\Sigma)
    \,.
  \end{array}
  \right.
\]
(cf. [Griffiths & Harris 1979 (1.13)](#GriffithsHarris79)).

Incidentally, this situation (eq:DarbouxCoframePullsBackToCoframe) of Darboux co-frames, when applied to the bosonic coframe components of [[super spacetimes]], has later independently come to be known as the "embedding condition" in the "[[super-embedding approach]]" to [[super p-branes]] &;brack;[Bandos 2011 (2.6-2.9)](super-embedding+approach#Bandos11); [Bandos & Sorokin 2023 (5.13-14)](super-embedding+approach#BandosSorokin23)&rbrack;, strenghtening the original "geometrodynamical condition" of [Bandos et al. 1995 (2.23)](super-embedding+formalism#BPSTV95), which is just the first condition in (eq:DarbouxCoframePullsBackToCoframe).
\end{remark}


\begin{proposition}
\label{ExistenceOfDarbouxFrames}
Given an immersion into a Riemannian manifold, local Darboux (co-)frames always exist. 
\end{proposition}
\begin{proof}
  Given an immersion $\iota \colon \Sigma \to X$, consider any point $\sigma \in \Sigma$. Since the immersion is *locally* an [[embedding of smooth manifolds|embedding]] (see [here](immersion+of+smooth+manifolds#ImmersionsAreLocalEmbeddings)), there exists an [[open neighbourhood]] $ \sigma \in U \subset \Sigma$ such that $\phi_{\vert U} \colon U \to X$ is the [[embedding of smooth manifolds|embedding]] of a [[submanifold]]. Therefore (by [this Prop.](submanifold#ExistenceOfSiceCharts)) there exists an [[open neighbourhood]] $U' \subset X$ of $\iota(\sigma) \in X$ which serves as a [[coordinate chart]] $X \supset U' \xrightarrow{\phi} \mathbb{R}^n$ for $X$ and a slice chart for $\Sigma \subset X$ in that it exhibits $\Sigma \cap U'$ as a rectilinear [[hyperplane]] in $\phi(U') \subset \mathbb{R}^n$.

Hence in this slice [[coordinate chart]] a local frame for $X$ is given by the $n$ canonical coordinate [[vector fields]] on with the first $k$ of them forming a local chart of $\Sigma$

$$
  \big\{ \partial_1, \cdots, \partial_{k} \big\}
  \hookrightarrow
  \big\{ 
    \partial_1, \cdots, \partial_{k}, 
    \,
    \partial_{k+1}, \cdots, \partial_n 
  \big\}
  \,.
$$

From this local frame the [[Gram-Schmidt process]] produces an *orthonormal* frame, first for $\Sigma$ and then extended to $X$:
$$
  \big\{ v_1, \cdots, v_{k} \big\}
  \hookrightarrow
  \big\{ 
    v_1, \cdots, v_{k}, 
    \,
    v_{k+1}, \cdots, v_n 
  \big\}
  \,,
  \;\;\;
  g(v_a, v_b) = \delta_{a b}
  \,
$$
This demonstrates the esistence of orthonormal local frames (cf. [Kayban 2021, Prop. 3.1](#Kayban21)).

To obtain an orthonormal local coframe we just dualize this local frame:

By construction, the matrix $\big(v_a^\mu\big)_{a,\mu}$ of components of the above frame (given by $v_a^\mu \partial_\mu = v_a$) is block diagonal (the upper diagonal block being the local frame on $\Sigma$).

This means (cf. e.g. [here](inverse+matrix#SD23)) that also the [[inverse matrix]] 
$$
  \big(e^a_\mu\big)_{\mu,a}
    \,\coloneqq\, 
  \Big(\big(v_a^\mu\big)_{\mu,a}\Big)^{-1}
$$
is block diagonal, with its upper diagonal block being the inverse matrix of the original upper left block.

This gives the desired [[coframe field]]:
$$
  e^{a} 
    \,\coloneqq\,
  e^a_\mu \, \mathrm{d}x^\mu
$$
which is orthonormal on $X$
$$
  e^a \otimes e_a
  \;=\;
  g(-,-)
$$
because
$$
  v_a^\mu g_{\mu \nu} v_b^\nu
  \;=\;
  \delta_{a b}
  \;\;\;\;
    \Leftrightarrow
  \;\;\;\;
  g_{\mu \nu}
  \;=\;
  e^a_\mu 
  \delta_{a b}
  e^b_\nu
  \,.
$$
and which is Darboux by the block-diagonal structure of $\big(e^a_\mu\big)$. 
\end{proof}

(For the further generality of [[sequences]] of Darboux frames for suitable [[sequences]] of immersions, see [Giron 2020](#Giron20) and [Chen & Giron 2021, Thm. 2.2](#ChenGiron21).)

Hence an immersion $\iota \colon \Sigma \hookrightarrow X$ of Riemannian manifolds is isometric iff around each point $\iota(\sigma)$ any of its Darboux coframe fields pull back to locally induce the given metric on $\Sigma$.

## References

* {#Sternberg64} [[Shlomo Sternberg]], _Lectures on differential geometry_, Prentice-Hall (1964), AMS (1983) &lbrack;ISBNJ:978-0-8218-1385-0, [ams:chel-316](https://bookstore.ams.org/chel-316), [ark:/13960/t1pg9dv6k](https://archive.org/details/lecturesondiffer0000ster)&rbrack;


* {#Guggenheimer77} [[Heinrich W. Guggenheimer]], *Differential Geometry*, Dover (1977) &lbrack;[isbn:9780486634333](https://store.doverpublications.com/products/9780486634333), [ark:/13960/t9t22sk9n](https://archive.org/details/differentialgeom0000gugg/)&rbrack;


* {#GriffithsHarris79} [[Phillip Griffiths]], [[Joseph Harris]], *Algebraic geometry and local differential geometry*, Annales scientifiques de l'École Normale Supérieure, Serie 4, Volume 12 no. 3 (1979) 355-452 &lbrack;[numdam:ASENS_1979_4_12_3_355_0](http://www.numdam.org/item/?id=ASENS_1979_4_12_3_355_0)&rbrack;

* {#BergerBryantGriffiths83} [[Eric Berger]], [[Robert Bryant]], [[Phillip Griffiths]], *The Gauss equations and rigidity of isometric embeddings*, Duke Math. J. **50** 3 (1983) 803-892 &lbrack;[doi:10.1215/S0012-7094-83-05039-1](http://dx.doi.org/10.1215/S0012-7094-83-05039-1)&rbrack;


* {#Zandi88} Ahmad Zandi, *Minimal immersions of surfaces in quaternionic projective space*, Tsukuba Journal of Mathematics **12** 2 (1988) 423-440 &lbrack;[jstor:43686661](https://www.jstor.org/stable/43686661)&rbrack;

* {#HanHong06} Qing Han, Jia-Xing Hong: *Isometric Embedding of Riemannian Manifolds in Euclidean Spaces*, Mathematical Surveys and Monographs **130**, AMS (2006) &lbrack;[ISBN:0821840711](https://maa.org/press/maa-reviews/isometric-embedding-of-riemannian-manifolds-in-euclidean-spaces)&rbrack;


* {#MastroliaRigoliSetti12} Paolo Mastrolia, Marco Rigoli, Alberto G. Setti, §1.3 *Some formulas for immersed submanifolds* in: *Yamabe-type Equations on Complete, Noncompact Manifolds*, Birkhäuser (2012) &lbrack;[doi:10.1007/978-3-0348-0376-2](https://doi.org/10.1007/978-3-0348-0376-2)&rbrack;

* {#Giron20} Tristan Pierre Giron, *On the Analysis of Isometric Immersions of Riemannian Manifolds*, PhD thesis (2020) &lbrack;[uuid:cae2f41d-c5a1-4138-9dec-5e824d21044e](https://ora.ox.ac.uk/objects/uuid:cae2f41d-c5a1-4138-9dec-5e824d21044e), [pdf](https://ora.ox.ac.uk/objects/uuid:cae2f41d-c5a1-4138-9dec-5e824d21044e/download_file?safe_filename=ThesisGironTristan.pdf&type_of_work=Thesis)&rbrack;

* {#ChenGiron21} Gui-Qiang G. Chen, Tristan P. Giron, *Weak continuity of curvature for connections in $L^p$* &lbrack;[arXiv:2108.13529](https://arxiv.org/abs/2108.13529)&rbrack;

* {#Kayban21} Nicholas Kayban, *Riemannian Immersions and Submersions* (2021) &lbrack;[pdf](https://www.math.uwaterloo.ca/~karigian/training/M11-kayban-final-project.pdf), [[Kayban-RiemannianImmersions.pdf:file]]&rbrack;

* {#HanLewicka23} Qing Han, Marta Lewicka, *Isometric immersions and applications*, Notices of the AMS 2023 &lbrack;[arXiv:2310.02566](https://arxiv.org/abs/2310.02566)&rbrack;


[[!redirects Riemannian immersions]]

[[!redirects isometric immersion]]
[[!redirects isometric immersions]]

[[!redirects isometric embedding]]
[[!redirects isometric embeddings]]

[[!redirects Darboux frame]]
[[!redirects Darboux frames]]

[[!redirects Darboux coframe]]
[[!redirects Darboux coframes]]



