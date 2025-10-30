> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak


***

The traditional definition of an orbifold:

\begin{definition}\label{OrbifoldDefinitionViaOrbifoldAtlas}
**(orbifold structure via orbifold atlas)**
\linebreak
Let $X$ be a [[paracompact topological space|paracompact]] [[Hausdorff space]].

1. An *orbifold [[chart]]* $\big(G \curvearrowright \widehat{U}, \phi\big)$ for $X$ is:

   1. $n \in \mathbb{N}$, the *dimension*,

   1. $\widehat U \subset \mathbb{R}^n$, a [[connected topological space|connected]] [[open subset]],

   1. $G \subset Diff(\widehat{U})$, a [[finite group]] of [[diffeomorphisms]] of $\widehat{U}$,

   1. $\phi : \widehat{U} \longrightarrow X$, a $G$-[[equivariant|invariant]] [[continuous function]] such that:

      1. its [[image]] $U \coloneqq \phi\big(\widehat{U}\big) \subset X$ is an [[open subset]],

      1. its [[quotient]] map $\widehat{U}/G \overset{\sim}{\longrightarrow} \phi\big(\widehat{U}\big) \subset X$ is a [[homeomorphism]] onto this image.

1. An *embedding* 

   $$
     \big(G_1 \curvearrowright \widehat{U}_1, \phi_1\big)
     \overset{\iota}{\hookrightarrow}
     \big(G_2 \curvearrowright \widehat{U}_2, \phi_2\big)
   $$

   between a [[pair]] of such orbifold charts is:

   * a [[smooth map|smooth]] [[embedding of smooth manifolds|embedding]] $\iota \colon \widehat{U}_1 \hookrightarrow \widehat{U}_2$

   such that:

   * $\phi_2 \circ \iota = \phi_1$.

1. An *orbifold atlas* for $X$ is:

   * a [[set]] $\Big\{\big(G_i \curvearrowright \widehat{U}_i, \phi_i\big)\Big\}_{i \in I}$ of orbifold charts

   such that:

   1. the images $\Big\{ U_i \xhookrightarrow{\phi} X \Big\}_{i \in I}$ form an [[open cover]] of $X$,

   1. for all pairs of charts $\big(G_1 \curvearrowright \widehat{U}_1, \phi_1\big)$, $\big(G_2 \curvearrowright \widehat{U}_2, \phi_2\big)$ in the set, and all $x \in U_1 \cap U_2$, there exists:

      1. an [[open neighbourhood]] $U_{12} \subset U_1 \cap U_2$ of $x$,

      1. an orbifold chart $\big(G_{12} \curvearrowright \widehat{U}_{12}, \phi_{12}\big)$ of $U_{12}$,

      1. embeddings $\big(G_{12} \curvearrowright \widehat{U}_{12}, \phi_{12}\big) \hookrightarrow \big(G_{i} \curvearrowright \widehat{U}_{i}, \phi_{i}\big)$ for $i \in \{1,2\}$.

1. An *equivalence* of a pair of such orbifold atlases is a third atlas which refines both via embeddings.

1. An *orbifold structure* on $X$ is a choice of [[equivalence class]] of orbifold atlases on $X$. 

\end{definition}

(cf. [Moerdijk & Pronk 1999 §1.1](#MoerdijkPronk99))


The above definition \ref{OrbifoldDefinitionViaOrbifoldAtlas} does not explicitly require that chart embeddings be [[equivariant maps|equivariant]], but this is implied (cf. [Moerdijk & Pronk 1999 §1.1.1(i)](#MoerdijkPronk99)):

\begin{lemma}
  \label{PairsOfOrbiChartEmbeddingsRelatedByGroupAction}
  For   
  $$
     \iota_i
     \,\colon\,
     \big(G_1 \curvearrowright \widehat{U}_1, \phi_1\big)
     \hookrightarrow
     \big(G_2 \curvearrowright \widehat{U}_2, \phi_2\big)  
  $$
  a [[pair]], $i \in \{1,2\}$, of embeddings of orbifold charts (Def. \ref{OrbifoldDefinitionViaOrbifoldAtlas}), there exists a unique $g_2 \in G_2$ such that
  $$
    \iota_2 = g_2 \circ \iota_1
    \mathrlap{\,.}
  $$
\end{lemma}
\begin{proof}
  By definition of chart embeddings, we have
  $$
    \phi_2 \circ \iota_1 
    =
    \phi_1
    =
    \phi_2 \circ \iota_2 
    \mathrlap{\,.}
  $$
  By the orbi-chart property of $\phi_2$, this means that for each point $x \in \widehat{U}_1$ there exists $g_2(x)$ such that
  $$
    \iota_2(x) = g_2(x) \circ \iota_1(x)
    \,,
  $$
  with $\widehat{U} \overset{g_2}{\longrightarrow} G_2 \colon x \to g_2(x)$ a [[continuous function]]. 

  Finally, by the assumption that $G_2$ is [[finite group|finite]], hence [[discrete group|discrete]], and that $\widehat{U}_1$ is [[connected topological space|connected]], this function must be [[constant function|constant]].
\end{proof}

\begin{proposition}
  Given an embedding of orbifold charts (Def. \ref{OrbifoldDefinitionViaOrbifoldAtlas})
  $$
     \iota
     \,\colon\,
     \big(G_1 \curvearrowright \widehat{U}_1, \phi_1\big)
     \hookrightarrow
     \big(G_2 \curvearrowright \widehat{U}_2, \phi_2\big)  
  $$
  there exists a unique [[group homomorphism]]
  $$
    \iota \colon G_1 \longrightarrow G_2
  $$
  such that for all $g_1 \in G_1$ and $x \in \widehat{U}_1$
  $$
    \lambda( g_1 \cdot x ) 
      \;=\;
    \lambda(g_1) \cdot \lambda(x)
    \,. 
  $$
\end{proposition}
\begin{proof}
  Noting that with $\lambda$ also $\lambda \circ g_1$ is am embedding,  Lem. \ref{PairsOfOrbiChartEmbeddingsRelatedByGroupAction} implies a unique $g_2$ with $g_2 \circ \lambda = \lambda \circ g_1$.
\end{proof}

\begin{remark}
  By the existence of invariant [[Riemann metrics]] and the differential version of the [[slice theorem]], every orbifold (Def. \ref{OrbifoldDefinitionViaOrbifoldAtlas}) may be given by an orbi-atlas all whose orbi-charts $\big(G, \widehat{U}, \phi\big)$ are [[open balls]] $\widehat{U} \simeq \mathbb{D}^n \subset \mathbb{R}^n$ equipped with an [[orthogonal group|orthogonal]] [[linear representation|linear]] [[group action]].
\end{remark}
(cf. [Moerdijk & Pronk 1999 §1.1.1(ii)](#MoerdijkPronk99))

...
