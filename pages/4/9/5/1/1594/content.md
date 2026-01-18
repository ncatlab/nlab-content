
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


\tableofcontents


## Idea

An [[orbifold]] is much like a [[smooth manifold]] but possibly with [[singularities]] of the form of [[fixed points]] of [[finite group|finite]] [[group]]-[[actions]].

\begin{imagefromfile}
  "file_name": "OrbifoldTypes.jpg",
  "width": 240,
  "float": "right",
  "margin": {
    "top": -30,
    "right": 0,
    "bottom": 10,
    "left": 20,
    "unit": "px"
  },
  "caption": "(from [Hyde-Ramsden-Robins 14](#HydeRamsdenRobins14))" 
\end{imagefromfile}

{#OrbifoldChartIdea} Where a [[smooth manifold]] is a [[space]] locally modeled on [[Cartesian spaces]]/[[Euclidean spaces]] $\mathbb{R}^n$, an _orbifold_ is, more generally, a [[space]] that is locally modeled on [[quotients]] of $\mathbb{R}^n$s, suitably understood, by [[group action|actions]] of [[finite groups]] of [[diffeomorphisms]]. Here [[fixed points]] of the [[group action]] become [[singularity|singular]] points in the quotient, like the tip of a [[cone]], which are not allowed in mere manifolds:

\begin{imagefromfile}
  "file_name": "OrbifoldChartSchematics.png",
  "width": 440,
  "margin": {
    "top": -30,
    "right": 10,
    "bottom": 10,
    "left": 10,
    "unit": "px"
  }
\end{imagefromfile}



One way to make precise the nature of these quotients is as [[quotient stack|stacky]] [[homotopy quotients]], hence as
[[Lie groupoid|smooth]] [[action groupoids]] $\mathbb{R}^n\sslash G$.  The global structure of an orbifold is then captured ([Moerdijk & Pronk 1997](#MoerdijkPronk97), [Moerdijk 2002](#Moerdijk02)) by saying that orbifolds are [[proper groupoid|proper]] [[étale groupoid|étale]] [[Lie groupoids]], and with [[Morita equivalence|Morita equivalent]] Lie groupoids understood to give the same orbifold this means that orbifolds are ([[étale groupoid|étale]]) [[smooth stacks]].

The word _orbifold_ was introduced by [Thurston 1992](#Thurston92), while the concept goes back to [Satake 1956](#Satake1956), who originally spoke of  *$V$-manifolds* and took them in a more restrictive sense, assuming that the [[actions]] of [[finite groups]] on the charts are always [[effective group action|effective]]. Nowadays these are called _effective orbifolds_. 

> There is also a notion of finite stabilizers in [[algebraic geometry]]. A singular variety is called an (algebraic) _orbifold_ if it has only so-called _orbifold singularities_.


\linebreak

{#ArtisticIllustrations} Artistic illustrations of 2-dimensional [[flat orbifolds]] (arising as [[quotient orbifold|quotients]] of the [[plane]] by [[wallpaper groups]]) are presented by [Conway, Burgiel & Goodman-Strauss 2008](#CBG08):

\begin{imagefromfile}
  "file_name": "CBG-3star3-orbifold.png",
  "width": 570,
  "margin": {
    "top": -30,
    "right": 0,
    "bottom": 10,
    "left": 20,
    "unit": "px"
  },
  "caption": "(from [CBG 2008 p. 114](#CBG08))" 
\end{imagefromfile}

\linebreak

\begin{imagefromfile}
  "file_name": "CBG-2222-orbifold.png",
  "width": 670,
  "margin": {
    "top": -30,
    "right": 0,
    "bottom": 10,
    "left": 20,
    "unit": "px"
  },
  "caption": "(from [CBG 2008 p. 116](#CBG08))" 
\end{imagefromfile}

\linebreak

## Definition

### Via orbifold atlases
 {#DefinitionViaOrbifoldAtlases}

The traditional definition of orbifolds, going back to [Satake 1956](#Satake1956):

\begin{definition}\label{OrbifoldDefinitionViaOrbifoldAtlas}
**(effective orbifold structure via orbifold atlas)**
\linebreak
Let $X$ be a [[paracompact Hausdorff space]].

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

\begin{remark}
\label{IsotropyActionOfTraditionalOrbiDefinitionIsEffective}
The assumption in Def. \ref{OrbifoldDefinitionViaOrbifoldAtlas} that the orbi-chart groups $G$ be [[subgroups]] of the [[diffeomorphism group]] implies that their [[group action|action]] on the chart is [[effective group action|effective]]. One also speaks of *effective orbifolds* to distinguish this original definition from the more relaxed one where the chart actions are only required to be through any [[group homomorphism]] $G \longrightarrow Diff\big(\widehat{U}\big)$.
\end{remark}

The above definition \ref{OrbifoldDefinitionViaOrbifoldAtlas} does not explicitly require that chart embeddings be [[equivariant maps|equivariant]], but this is implied (cf. [MP99 §1.1.1(i)](#MoerdijkPronk99)):

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
  \[
    \label{EquivarianceOfOrbiChartEmbedding}
    \iota( g_1 \cdot x ) 
      \;=\;
    \iota(g_1) \cdot \iota(x)
    \,. 
  \]
  Moreover, if the orbifold is effective (Rem. \ref{IsotropyActionOfTraditionalOrbiDefinitionIsEffective}), the this group homomorphism is [[monomorphism|injective]].
\end{proposition}
\begin{proof}
  Noting that with $\lambda$ also $\lambda \circ g_1$ is am embedding,  Lem. \ref{PairsOfOrbiChartEmbeddingsRelatedByGroupAction} implies a unique $g_2$ with $g_2 \circ \lambda = \lambda \circ g_1$. This gives the group homomorphism.

To see that this homomorphism is injective of the chart actions are [[effective group action]], assume that $g_1$ is such that that $\iota(g_1) = \mathrm{e}$. We need to see that then already $g_1 = \mathrm{e}$. But the equivariance property (eq:EquivarianceOfOrbiChartEmbedding) just proven states that, for all $x \in \widehat{U}_1$,
$$
  \iota(g_1 \cdot x) 
  =
  \iota(x)
  \,.
$$
Since $\iota$ is an [[embedding of smooth manifolds]], this implies that $g_1 \cdot x = x$ for all $x \in \widehat{U}_1$, for all $x$. By [[effective group action|effectiveness]], this implies that $g_1 = \mathrm{e}$.
\end{proof}

\begin{remark}
Every orbifold (Def. \ref{OrbifoldDefinitionViaOrbifoldAtlas}) may be given by an orbi-atlas all whose orbi-charts $\big(G, \widehat{U}, \phi\big)$ are [[open balls]] $\widehat{U} \simeq \mathbb{D}^n \subset \mathbb{R}^n$ equipped with an [[orthogonal group|orthogonal]] [[linear representation|linear]] [[group action]].This follows by the existence of invariant [[Riemannian metrics]] and the differential version of the [[slice theorem]], 
\end{remark}
(cf. [MP99 §1.1.1(ii)](#MoerdijkPronk99))



### Via proper étale groupoids
  {#DefinitionViaProperEtaleGroupoids}

Equivalently, an orbifold is a [[smooth stack]] presented by an [[orbifold groupoid]] &lbrack;[Moerdijk & Pronk 1997](#MoerdijkPronk97), [1999](#MoerdijkPronk99)&rbrack;. 

\begin{definition}
  \label{OrbifoldAsProperEtaleGroupoid}
  An *orbifold* is a [[Lie groupoid]] $\mathcal{G}$ which is

1. [[étale groupoid|étale]]:

   the [[source]] map $s \colon Mor(\mathcal{G}) \longrightarrow Obj(\mathcal{G})$ is a [[local diffeomorphisms]] (as are then all the other structure maps),

1. [[proper Lie groupoid|proper]]: 

   the [[pair]] of the [[source]] and [[target]] maps $(s,t) \colon Mor(\mathcal{G}) \longrightarrow Obj(\mathcal{G})$ is a [[proper map]].

\end{definition}

\begin{remark}
  From the perspective of the traditional Definition \ref{OrbifoldDefinitionViaOrbifoldAtlas} one may rather want to say that (cf. [Moerdijk 2002 §3.2](#Moerdijk02)):
An *orbifold structure* on a [[paracompact Hausdorff space]] $X$ is a choice of Lie groupoid $\mathcal{G}$ as in Def. \ref{OrbifoldAsProperEtaleGroupoid}, together with a [[homeomorphism]] from its space of [[isomorphism classes]], $Obj(\mathcal{G})/\mathrm{Mor}(\mathcal{G}) \overset{\sim}{\longrightarrow} X$.

But since $X$ is determined, up to homeomorphism, from the groupoid $\mathcal{G}$, the evident [[category]] of orbifold structures in this sense is [[equivalence of categories|equivalent]] to the [[homotopy category]] of the corresponding [[Lie groupoids]]/[[differentiable stacks]] (cf. [Moerdijk 2002 §3.3](#Moerdijk02))
\end{remark}

\begin{remark}
  The main ingredient in the construction (cf. [Amenta 2012, Cor. 2.4.13](#Amenta12)) of an orbifold atlas (Def. \ref{OrbifoldDefinitionViaOrbifoldAtlas}) from an effective  proper étale Lie groupoid (Def. \ref{OrbifoldAsProperEtaleGroupoid}) is the fact that every point $x$ in the object space of a proper étale Lie groupoid has an [[open neighbourhood]] $U \subset Obj(\mathcal{G})$ on which the groupoid structure restricts to an [[action groupoid]] $U \sslash G_x$ of the [[finite group|finite]] [[automorphism group]]/[[isotropy group]] $G_x \coloneqq Hom_{\mathcal{G}}(x,x)$ of $x$. (cf. [Moerdijk & Pronk 1997, pp. 15](#MoerdijkPronk97), [Amenta 2012, Thm. 2.4.11](#Amenta12))

Conversely, the construction of a proper étale Lie groupoid (Def. \ref{OrbifoldAsProperEtaleGroupoid}) from an orbifold atlas (Def. \ref{OrbifoldDefinitionViaOrbifoldAtlas}) is indicated in [Moerdijk & Pronk 1999, inside proof of Thm. 4.1.1](#MoerdijkPronk99).
\end{remark}



## Properties

### General

* One can consider a [[bicategory]] of proper &#233;tale Lie groupoids and the orbifolds will be the objects of certain bicategorical [[localization]] of this bicategory (a result of [Moerdijk-Pronk 97](#MoerdijkPronk97)). 


* Equivalently, every orbifold is globally a quotient of a smooth manifold by an [[action]] of finite-dimensional [[Lie group]] with finite [[stabilizer subgroup|stabilizers]] in each point. (eg ([Adem-Leida-Ruan 2007](#ALR07)), Corollary 1.24)


### Global quotient orbifolds
 {#GlobalQuotientOrbifolds}

In ([ALR 07, theorem 1.23](#ALR07)) it is asserted that every effective orbifold $X$ (paracompact, Hausdorff) is isomorphic to a [[global quotient orbifold]], specifically to a global quotient of $O(n)$ (where $n$ is the dimension of $X$) acting on the [[frame bundle]] of $X$ (which is a manifold).

### (Co)homology

It has been noticed that the topological invariants of the underlying topological space of an orbifold as a topological space with an orbifold structure are not appropriate, but have to be corrected leading to [[orbifold Euler characteristics]], [[orbifold cohomology]] etc. One of the constructions which is useful in this respect is the [[inertia orbifold]] (the inertia stack of the original orbifold) which gives rise to "twisted sectors" in Hilbert space of a quantum field theory on the orbifold, and also to twisted sectors in the appropriate cohomology spaces. A further generalization gives multitwisted sectors. 




## Examples

\begin{example}
\label{SignInvolutionOrbifoldOfNTorus}
**(sign involution orbifold of the $n$-torus)**
\linebreak
 A basic class of examples of closed [[flat orbifolds]] are the [[orbifold quotients]] $\mathbb{T}^n \sslash C_2$ of the [[n-torus|$n$-torus]] $\mathbb{T}^n \,\coloneqq\, \mathbb{R}^n/\mathbb{Z}^n$ by the [[involution]]-[[group action|action]] inverting the sign of the canonical [[coordinates]]:

* For $n = 0$ this is the [[delooping groupoid]] $\mathbf{B} \mathbb{Z}_2$.

* For $n = 1$ this plays the central role in  [[Hořava-Witten theory]].

* For $n = 2$ this is known as the [[pillowcase orbifold]].

* For $n = 3$ this does not have a special name but appears as the [[Brillouin torus]] orbifold for [[crystal|crystalline]] materials with [[time-reversal symmetry]] when considering their [[K-theory classification of topological phases of matter]], and in some [[string theory vacuum|string backgrounds]] (e.g. [arXiv:2205.09764](https://arxiv.org/abs/2205.09764)).

* For $n = 4$ this is known as the [Kummer surface](K3+surface#KummerSurface).

* For $n = 5$ this appears as the [[MO5-plane]] [[spacetime]] in [[M-theory]].
 
\end{example}


**Further examples:**


* Some basic building blocks of orbifolds:

  The quotient of a  [[ball]] by a [[discrete group|discrete]] [[subgroup]] of the [[special orthogonal group]] of rotations is an orbifold, and orbifolds may be obtained by cutting out balls from ordinary [[smooth manifolds]] and gluing in these orbifold quotients.

* The [[moduli stack of elliptic curves]] over the [[complex numbers]] is an orbifold, being the [[homotopy quotient]] of the [[upper half plane]] by the [[special linear group]] acting by [[Möbius transformations]].

* For $\mathcal{G}$ any orbifold, then the [[mapping space]] $\mathcal{G}^{\Pi(S^1)} = \mathcal{G}^{B\mathbb{Z}}$ is again an orbifold, called the [[inertia orbifold]].

* [[pillowcase orbifold]]

* [[spindle orbifold]]

* [[G₂-orbifolds]]

* [[lens spaces]]

* [[ADE singularities]]

* [[metric cones]]

* See also [Lange 2024](#Lange24)


## Related concepts

* [[presentable orbifold]], [[good orbifold]], [[very good orbifold]]

* [[étale groupoid]], [[differentiable stack]]

* [[orbispace]], [[topological stack]]

* [[Riemannian orbifold]]

  * [[flat orbifold]]

* [[Lorentzian orbifold]]

* [[complex orbifold]]

* [[symplectic orbifold]]

* [[super-orbifold]]

* [[discrete torsion]]

* [[motivation for higher differential geometry]]

* [[orbifold Euler characteristic]]

* [[orbifold K-theory]], [[orbifold differential K-theory]]

Orbifolds are in [[differential geometry]] what [[Deligne-Mumford stacks]] are in [[algebraic geometry]]. See also at _[[geometric invariant theory]]_ and _[[GIT-stable point]]_.

Orbifolds may be regarded as a kind of _[[stratified spaces]]_.

See also: 

* [[étale groupoid]]

* [[stable map]]

* [[orbifold cohomology]]

* [[Gromov-Witten theory]]

Orbifolds in [[string theory]]:

* [[fractional D-brane]]

  [[permutation D-brane]]

* [[ADE singularity]]

* [[orientifold]]



## References

### General
 {#ReferencesGeneral}

Essentially the modern definition of orbifolds [via orbifold atlases](#DefinitionViaOrbifoldAtlases) was first given by:

* {#Satake1956} [[Ichiro Satake]]: _On a generalisation of the notion of manifold_, Proc. Nat. Acad. Sci. U.S.A. **42** (1956), 359-363 &lbrack;[doi:10.1073/pnas.42.6.359](https://doi.org/10.1073/pnas.42.6.359)&rbrack;

* [[Ichiro Satake]]: _The Gauss-Bonnet theorem for $V$-manifolds_, J. Math. Soc. Japan **9** (1957) 464-492 &lbrack;[euclid:1261153826](https://projecteuclid.org/euclid.jmsj/1261153826)&rbrack;

under the name "V-manifolds". (Satake's motivation for this terminology has not survived. One claim &lbrack;[MO:q/97901](https://mathoverflow.net/q/97901/381)&rbrack; is that: According to a colleague who asked Satake about it, the "V" in "V-manifold" stands for the German word '*Verzweigung*, which means "branching" or "ramification", as in *[[ramified cover]]*.)


The term "orbifold" was introduced by:

<div style="float:right;margin:-30px 0px 00px 20px;">
<a href="https://ncatlab.org/nlab/files/Thurston-3dGeometry-2002.pdf#page=318"><img src="/nlab/files/Thurston-NamingOrbifold.png" width="500"></a>
</div>

* {#Thurston92} [[William Thurston]], §3.2 of: *Three-dimensional geometry and topology*, preliminary draft, University of Minnesota (1992) &lbrack;1979: [ark:/13960/t3714t34v](https://archive.org/details/ThurstonTheGeometryAndTopologyOfThreeManifolds/mode/2up), 1991:  [[Thurston-3dGeometry-1991.pdf:file]], 2002: [pdf](https://www.math.unl.edu/~jkettinger2/thurston.pdf), [[Thurston-3dGeometry-2002.pdf:file]]&rbrack;
   
the first three chapters of which are published in expanded form as:

* [[William Thurston]]: _The Geometry and Topology of Three-Manifolds_, Princeton University Press (1997) &lbrack;[ISBN:9780691083049](https://press.princeton.edu/books/hardcover/9780691083049/three-dimensional-geometry-and-topology-volume-1), [Wikipedia page](https://en.wikipedia.org/wiki/The_geometry_and_topology_of_three-manifolds)&rbrack;


Further early discussion:

* [[André Haefliger]], _Groupoides d'holonomie et classifiants_, Astérisque **116** (1984) 70-97 &lbrack;[numdam:AST_1984__116__70_0/](http://www.numdam.org/item/AST_1984__116__70_0/)&rbrack;

* [[Peter Scott]], section 2 of: *The Geometries of 3-Manifolds*, Bulletin of the LMS **15** 5 (1983) 401-487 &lbrack;[doi:10.1112/blms/15.5.401](https://doi.org/10.1112/blms/15.5.401), [hdl:2027.42/135276](https://hdl.handle.net/2027.42/135276)&rbrack;

and specifically for orbifolds in [[complex geometry]]:

* [[Walter Lewis Baily]], _On the quotient of an analytic manifold by a group of analytic homeomorphisms_, PNAS **40** 9 (1954) 804-808 &lbrack;[doi:10.1073/pnas.40.9.804](https://doi.org/10.1073/pnas.40.9.804)&rbrack;

* [[Walter Lewis Baily]], _The Decomposition Theorem for V-Manifolds_, American Journal of Mathematics Vol. 78, No. 4 (Oct., 1956), pp. 862-888 ([jstor:2372472](https://www.jstor.org/stable/2372472))

For careful comparative review of the definitions in these original articles see also [IKZ 10](#IKZ10).


Survey of basic orbifold theory:

* Daryl Cooper, Craig Hodgson, Steve Kerckhoff, _Three-dimensional Orbifolds and Cone-Manifolds_,  MSJ Memoirs Volume 5, 2000 ([pdf](https://web.math.ucsb.edu/~cooper/37.pdf), [euclid:1389985812](https://projecteuclid.org/euclid.msjm/1389985812))

* [[Ieke Moerdijk]], [[Janez Mrčun]], Section 2.4 of: _[[Introduction to foliations and Lie groupoids]]_, Cambridge Studies in Advanced Mathematics  __91__ (2003) &lbrack;ISBN: 0-521-83197-0, [doi:10.1017/CBO9780511615450](https://doi.org/10.1017/CBO9780511615450)&rbrack;

* {#BoyerGalicki07} [[Charles Boyer]], [[Krzysztof Galicki]], Chapter 4 of: _Sasakian Geometry_, Oxford Mathematical Monographs, Oxford University Press, 2007 ([doi:10.1093/acprof:oso/9780198564959.001.0001](https://www.oxfordscholarship.com/view/10.1093/acprof:oso/9780198564959.001.0001/acprof-9780198564959))

* {#Kaye07} Adam Kaye, _Two-Dimensional Orbifolds_ (2007) &lbrack;[pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2007/REUPapers/FINALFULL/Kaye.pdf)&rbrack;

* {#CBG08} [[John H. Conway]], [[Heidi Burgiel]], [[Chaim Goodman-Strauss]]: *Orbifolds*, chapter 9 of: *The Symmetries of Things*, CRC Press (2008) &lbrack;[ISBN:9781568812205](https://www.routledge.com/The-Symmetries-of-Things/Conway-Burgiel-Goodman-Strauss/p/book/9781568812205)&rbrack;

* Michael Davis, _Lectures on orbifolds and reflection groups_, (2008) &lbrack;[pdf](https://math.osu.edu/sites/math.osu.edu/files/08-05-MRI-preprint.pdf)&rbrack;

* {#Porti09} Joan Porti, _An introduction to orbifolds_ (2009) &lbrack;[pdf](http://mat.uab.es/~porti/orbifoldLeiden.pdf)&rbrack;

* {#Snowden11} Andrew Snowden: _Introduction to orbifolds_ (2011) &lbrack;[webpage](https://ocw.mit.edu/courses/18-904-seminar-in-topology-spring-2011/resources/mit18_904s11_finlorbifolds/), [[Snowden-Orbifolds.pdf:file]]&rbrack;

* {#AdemKlaus} [[Alejandro Adem]], Michele Klaus, _Lectures on orbifolds and group cohomology_ ([pdf](http://www.math.ubc.ca/~adem/hangzhou.pdf), [[AdemKlausOrbifolds.pdf:file]])

* Francisco C. Caramello Jr: *Introduction to orbifolds* &lbrack;[arXiv:1909.08699](https://arxiv.org/abs/1909.08699)&rbrack;

See also:

* Wikipedia: _[Orbifolds](http://en.wikipedia.org/wiki/Orbifold)_ 

* Alanod Sibih: *Orbifold Atlas Groupoids*, PhD thesis, Dalhousie (2013) &lbrack;[pdf](https://dalspaceb.library.dal.ca/server/api/core/bitstreams/313bac18-de54-4a7f-81a4-75949f57b404/content)&rbrack; 

On [[good orbifolds]]:

* {#Lange24} Christian Lange: *Good, but not very good orbifolds* &lbrack;[arXiv:2404.14234](https://arxiv.org/abs/2404.14234)&rbrack;


Textbook accounts:

* {#Ratcliffe06} [[John Ratcliffe]], _Geometric Orbifolds_, chapter 13 in _Foundations of Hyperbolic Manifolds_, Graduate Texts in Mathematics **149**, Springer (2006) &lbrack;[doi:10.1007/978-0-387-47322-2](https://doi.org/10.1007/978-0-387-47322-2), <a href="http://entsphere.com/pub/pdf/Ratcliffe%20-%20Foundations%20of%20hyperbolic%20manifolds%20(2e)%20-%20GTM%20149.pdf">pdf</a>&rbrack;

* [[Michael Kapovich]], Chapter 6 of: _Hyperbolic Manifolds and Discrete Groups_,  Modern Birkhäuser Classics, Birkhäuser (2008) &lbrack;[doi:10.1007/978-0-8176-4913-5](https://link.springer.com/book/10.1007/978-0-8176-4913-5)&rbrack;

Application to [[moduli spaces of curves]] and [[moduli spaces of Riemann surfaces]]:

* Lizhen Ji, [[Shing-Tung Yau]], _Transformation Groups and Moduli Spaces of Curves_, International Press of Boston 2011 ([ISBN:9781571462237](https://www.intlpress.com/site/pub/pages/books/items/00000353/index.php))

On [[Riemannian orbifolds]]:

* Christian Lange, _Orbifolds from a metric viewpoint_ ([arXiv:1801.03472](https://arxiv.org/abs/1801.03472))

* Renato G. Bettiol, Andrzej Derdzinski, Paolo Piccione, _Teichmüller theory and collapse of flat manifolds_, Annali di Matematica (2018) 197: 1247 ([arXiv:1705.08431](https://arxiv.org/abs/1705.08431), [doi:10.1007/s10231-017-0723-7](https://doi.org/10.1007/s10231-017-0723-7))

* {#HydeRamsdenRobins14} S. T. Hyde, S. J. Ramsden and V. Robins, _Unification and classification of two-dimensional crystalline patterns using orbifolds_, Acta Cryst. (2014). A70, 319-337 ([doi:10.1107/S205327331400549X](https://doi.org/10.1107/S205327331400549X))


Assorted applications in [[mathematical physics]] and notably in [[string theory]]:

* {#AdemMoravaRuan02} [[Alejandro Adem]], [[Jack Morava]], [[Yongbin Ruan]], _[[Orbifolds in Mathematics and Physics]]_, Contemporary Mathematics **310**, American Mathematical Society (2002) &lbrack;[ISBN:978-0-8218-2990-5](https://bookstore.ams.org/conm-310)&rbrack;


Orbifolds often appear as [[moduli spaces]] in [[differential geometry]]: 

* [[Joel W. Robbin]], [[Dietmar A. Salamon]]: _A construction of the Deligne--Mumford [[orbifold]]_, J. Eur. Math. Society **8** 4 (2006) 611--699 &lbrack;[arXiv:math/0407090](https://arxiv.org/abs/math/0407090), [MR2009d:32012](http://www.ams.org/mathscinet-getitem?mr=2009d:32012)&rbrack;, _Corrigendum_, J. Eur. Math. Soc. (JEMS)  __9__  4 (2007) 901--905 &lbrack;[doi:10.4171/JEMS/101](https://doi.org/10.4171/JEMS/101)&rbrack;

The generalization of orbifolds to *weighted [[branched manifolds]]*:

* [[Dusa McDuff]]: _Groupoids, branched manifolds and multisections_, J. Symplectic Geom. **4** 3 (2006) 259-315 &lbrack;[project euclid](http://projecteuclid.org/euclid.jsg/1180135649)&rbrack;

On [[orbifolds]], [[orbifold cohomology]] and specifically on [[Chen-Ruan cohomology]] and [[orbifold K-theory]]:

* {#ALR07} [[Alejandro Adem]], [[Johann Leida]], [[Yongbin Ruan]], _Orbifolds and Stringy Topology_, Cambridge Tracts in Mathematics **171** (2007) &lbrack;[doi:10.1017/CBO9780511543081](https://doi.org/10.1017/CBO9780511543081), [pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf)&rbrack;


### As proper étale Lie groupoids
 {#ReferencesAsLieGroupoids}

The understanding of orbifolds as [[proper Lie groupoid|proper]] [[étale groupoid|étale]] [[Lie groupoids]]/[[differentiable stacks]] is due to

* {#MoerdijkPronk97} [[Ieke Moerdijk]], [[Dorette Pronk]], pp. 15 in: *Orbifolds, sheaves and groupoids*, K-theory **12** 1 (1997) 3-21 &lbrack;[doi:10.1023/A:1007767628271](http://dx.doi.org/10.1023/A:1007767628271), [[MoerdijkPronk-OrbifoldsAndGroupoids.pdf:file]]&rbrack;

* {#MoerdijkPronk99} [[Ieke Moerdijk]], [[Dorette Pronk]], section 4 of: *Simplicial cohomology of orbifolds*, Indagationes Mathematicae **10** 2 (1999) 269-293 \[<a href="https://doi.org/10.1016/S0019-3577(99)80021-4">doi:10.1016/S0019-3577(99)80021-4</a>\]

* {#Moerdijk02} [[Ieke Moerdijk]]: *Orbifolds as Groupoids: an Introduction*, in: [[Alejandro Adem]], [[Jack Morava]], [[Yongbin Ruan]] (eds.): _[[Orbifolds in Mathematics and Physics]]_, Contemporary Math **310**, AMS (2002) 205–222 &lbrack;[arXiv:math.DG/0203100](http://arxiv.org/abs/math.DG/0203100), [ISBN:978-0-8218-2990-5](https://bookstore.ams.org/conm-310)&rbrack;

See also:

* {#Lerman08} [[Eugene Lerman]], *Orbifolds as stacks?*, Enseign. Math. **56** 3-4 (2010) 315-363 &lbrack;[arXiv:0806.4160](http://arxiv.org/abs/0806.4160), [doi:10.4171/LEM/56-3-4](http://dx.doi.org/10.4171/LEM/56-3-4)&rbrack;

Review:

* Olivier Brahic: *Orbifolds via Lie Groupoids* (2009) &lbrack;[pdf](https://www.math.tecnico.ulisboa.pt/~martinez/files/Orbifolds.pdf)&rbrack;

and further details:

* {#Amenta12} Alexander Amenta: _The Geometry of Orbifolds via Lie Groupoids_, Honours Thesis, Australian National University (2012) &lbrack;[arXiv:1309.6367](https://arxiv.org/abs/1309.6367)&rbrack;

Analogous discussion for topological orbifolds as [[topological stacks]]:

* Vesta Coufal, [[Dorette Pronk]], [[Carmen Rovi]], [[Laura Scull]], Courtney Thatcher: _Orbispaces and their Mapping Spaces via Groupoids: A Categorical Approach_, in: *Women in Topology: Collaborations in Homotopy Theory*, Contemporary Mathematics **641** (2015) 135-166 &lbrack;[arXiv:1401.4772](https://arxiv.org/abs/1401.4772), [doi:10.1090/conm/641](https://doi.org/10.1090/conm/641)&rbrack;


Discussion of the corresponding perspective in [[algebraic geometry]], via [[Deligne-Mumford stacks]]:

* {#Kresch09} [[Andrew Kresch]], _On the geometry of Deligne-Mumford stacks_ ([doi:10.5167/uzh-21342](https://doi.org/10.5167/uzh-21342), [pdf](https://www.zora.uzh.ch/id/eprint/21342/1/geodm.pdf)), in:  D. Abramovich, A. Bertram, L. Katzarkov, R. Pandharipande, M. Thaddeus (eds.) _Algebraic Geometry: Seattle 2005_, Proceedings of Symposia in Pure Mathematics **80**, American Mathematical Society (2009) 259-271 &lbrack;[pspum-80-1](https://bookstore.ams.org/pspum-80-1)&rbrack;


On [[mapping stacks]] of orbifolds:

* [[Weimin Chen]], *On a notion of maps between orbifolds, I. Function spaces*, Commun. Contemp. Math. 8 (2006), no. 5, 569&#8211;620 ([arXiv:math/0603671](https://arxiv.org/abs/math/0603671), [doi:10.1142/S0219199706002246](https://doi.org/10.1142/S0219199706002246)).

* {#RobertsVozzo18} [[David Roberts]], [[Raymond Vozzo]], _The Smooth Hom-Stack of an Orbifold_, In : Wood D., de Gier J., Praeger C., Tao T. (eds) 2016 MATRIX Annals. MATRIX Book Series, vol 1. Springer, Cham (2018) ([arXiv:1610.05904](https://arxiv.org/abs/1610.05904), [doi:10.1007/978-3-319-72299-3_3](https://doi.org/10.1007/978-3-319-72299-3_3))

Discussion of [[principal bundles]] and [[fiber bundles]] over orbifolds:

* [[Camille Laurent-Gengoux]], [[Jean-Louis Tu]], [[Ping Xu]], _Chern-Weil map for principal bundles over groupoids_, Math. Z. 255, 451–491 (2007) ([arXiv:math/0401420](https://arxiv.org/abs/math/0401420), [doi:10.1007/s00209-006-0004-4](https://doi.org/10.1007/s00209-006-0004-4))

* Christopher Seaton: _Characteristic Classes of Bad Orbifold Vector Bundles_, Journal of Geometry and Physics **57** 11 (2007), 2365--2371 &lbrack;[arXiv:math/0606665](https://arxiv.org/abs/math/0606665), [doi:10.1016/j.geomphys.2007.08.001](https://doi.org/10.1016/j.geomphys.2007.08.001)&rbrack;


An expected relation of orbifolds ([[orbispaces]]) to [[global equivariant homotopy theory]]:

* [[Stefan Schwede]], _Orbispaces, orthogonal spaces, and the universal compact Lie group_ &lbrack;[arXiv:1711.06019](https://arxiv.org/abs/1711.06019)&rbrack;
  > (on the relation to [[orbispaces]]/[[topological stacks]])


### As diffeological spaces
  {#ReferencesAsDiffeologicalSpaces}

On [[orbifolds]] regarded as naive local [[quotient spaces]] (instead of [[homotopy quotients]]/[[Lie groupoids]]/[[differentiable stacks]]) but as such formed in [[diffeological spaces]]:

* {#IKZ10} [[Patrick Iglesias-Zemmour]], [[Yael Karshon]], Moshe Zadka: _Orbifolds as diffeologies_, Transactions of the American Mathematical Society **[362](https://www.ams.org/journals/tran/2010-362-06/)** (2010) 2811-2831 &lbrack;[arXiv:math/0501093](https://arxiv.org/abs/math/0501093), [doi:10.1090/S0002-9947-10-05006-3](https://www.ams.org/journals/tran/2010-362-06/S0002-9947-10-05006-3)&rbrack;

* {#Watts15} [[Jordan Watts]], _The Differential Structure of an Orbifold_, Rocky Mountain Journal of Mathematics, Vol. 47, No. 1 (2017), pp. 289-327 ([arXiv:1503.01740](https://arxiv.org/abs/1503.01740))

and as [[stratified space|stratified]] [[diffeological spaces]]:

* [[Serap Gürer]], [[Patrick Iglesias-Zemmour]], *Orbifolds as stratified diffeologies*, Differential Geometry and its Applications **86** (2023) 101969 &lbrack;[doi:10.1016/j.difgeo.2022.101969](https://doi.org/10.1016/j.difgeo.2022.101969)&rbrack;

On this approach seen in the broader context of [[cohesive homotopy theory|cohesive]] [[higher differential geometry]]:

* [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))

* [[David Jaz Myers]], *Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory* &lbrack;[arXiv:2205.15887](https://arxiv.org/abs/2205.15887)&rbrack;


### Orbifold cobordism

Orbifold [[cobordisms]] are discussed in 

* K. S. Druschel, _Oriented Orbifold Cobordism_, Pacific J. Math., 164(2) (1994), 299-319 ([doi:10.2140/pjm.1994.164.299](http://dx.doi.org/10.2140/pjm.1994.164.299), [pdf](https://msp.org/pjm/1994/164-2/pjm-v164-n2-p04-p.pdf))

* K. S. Druschel, _The Cobordism of Oriented Three Dimensional Orbifolds_, Pacific J. Math., bf 193(1) (2000), 45-55.

* Andres Angel, _Orbifold cobordism_ ([pdf](http://www.math.uni-bonn.de/people/aangel79/Orbifold%20cobordism.pdf)) 

See also at _[[orbifold cobordism]]_.

[[tangential structure]] on [[orbifolds]] (in the context of [[factorization homology]]):

* [[Tim Weelinck]], _Equivariant factorization homology of global quotient orbifolds_ ([arXiv:1810.12021](https://arxiv.org/abs/1810.12021), [talk pdf](https://www.maths.ed.ac.uk/~tweelinck/efhqsp.pdf))

* John Pardon: _Orbifold bordism and duality for finite orbispectra_, Geom. Topol. **27** (2023) 1747-1844 &lbrack;[arXiv:2006.12702](https://arxiv.org/abs/2006.12702), [doi:10.2140/gt.2023.27.1747](https://doi.org/10.2140/gt.2023.27.1747)&rbrack;



### In string theory
{#ReferencesInStringTheory}


\begin{imagefromfile}
  "file_name": "GreenStringOrbifold.jpg",
  "width": 700,
  "margin": {
    "top": -30,
    "right": 0,
    "bottom": 10,
    "left": 20,
    "unit": "px"
  },
  "caption": "(from [Green 86](string+theory#Green86))" 
\end{imagefromfile}




In [[perturbative string theory]], orbifolds as [[target spaces]] for a [[string]] [[sigma-model]] were first considered in 

* {#DixonHarveyVafaWitten85} [[Lance Dixon]], [[Jeff Harvey]], [[Cumrun Vafa]], [[Edward Witten]], _Strings on orbifolds_, Nuclear Physics B Volume 261, 1985, Pages 678-686 (<a href="https://doi.org/10.1016/0550-3213(85)90593-0">doi:10.1016/0550-3213(85)90593-0</a>)

* {#DixonHarveyVafaWitten86} [[Lance Dixon]], [[Jeff Harvey]], [[Cumrun Vafa]], [[Edward Witten]], _Strings on orbifolds (II)_, Nuclear Physics B Volume 274, Issue 2, 15 September 1986, Pages 285-314 (<a href="https://doi.org/10.1016/0550-3213(86)90287-7">doi:10.1016/0550-3213(86)90287-7</a>)

and then further developed notably in 

* {#DVVV89} [[Robbert Dijkgraaf]], [[Cumrun Vafa]], [[Erik Verlinde]], [[Herman Verlinde]], _The operator algebra of orbifold models_, Comm. Math. Phys. Volume 123, Number 3 (1989), 485-526 ([euclid:1104178892](https://projecteuclid.org/euclid.cmp/1104178892))

* [[Eric Zaslow]], _Topological orbifold models and quantum cohomology rings_, Comm. Math. Phys. 156 (1993), no. 2, 301&#8211;331.

See also:

* Stefano Giaccari, [[Roberto Volpato]], *A fresh view on string orbifolds* &lbrack;[arXiv:2210.10034](https://arxiv.org/abs/2210.10034)&rbrack;

For more references on orbifolds in [[string theory]] see also at

* _[[Riemannian orbifold]]_, _[[toroidal orbifold]]_

* _[[fractional D-brane]]_

* _[[Gepner model]]_

* _[[orientifold]]_

* _[[RR-field tadpole cancellation]]_


Review of [[heterotic string theory|heterotic]] [[string phenomenology]] on orbifolds:


* [[Saul Ramos-Sanchez]], [[Michael Ratz]], *Heterotic Orbifold Models*, in: *[[Handbook of Quantum Gravity]]*, Springer (2024) \[<a href="https://doi.org/10.1007/978-981-19-3079-9">doi:10.1007/978-981-19-3079-9</a>, 
[arXiv:2401.03125](https://arxiv.org/abs/2401.03125)\]


Discussion of [[blow-up]] of orbifold [[singularities]] in string theory:

* [[Paul Aspinwall]], _Resolution of Orbifold Singularities in String Theory_ ([arXiv:hep-th/9403123](https://arxiv.org/abs/hep-th/9403123))

In terms of [[vertex operator algebras]]:

* [[Yi-Zhi Huang]], _Representation theory of vertex operator algebras and orbifold conformal field theory_ ([arXiv:2004.01172](https://arxiv.org/abs/2004.01172))


Review of orbifolds in the context of string [[KK-compactifications]] and [[intersecting D-brane models]]:

* {#BailibLove99} D. Bailin, A. Love, _Orbifold compactifications of string theory_, Phys. Rept. 315 (1999) 285-408 (<a href="https://doi.org/10.1016/S0370-1573(98)00126-4">doi:10.1016/S0370-1573(98)00126-4</a>, [spire:504382](https://inspirehep.net/literature/504382))

* {#Wendland01} [[Katrin Wendland]], _Orbifold Constructions of K3: A Link between Conformal Field Theory and Geometry_, in _[[Orbifolds in Mathematics and Physics]]_ ([arXiv:hep-th/0112006](https://arxiv.org/abs/hep-th/0112006))

* {#Giedt02} Joel Giedt, _Heterotic Orbifolds_ ([arXiv:hep-ph/0204315](https://arxiv.org/abs/hep-ph/0204315))

* [[Dieter Lüst]], S. Reffert, E. Scheidegger, S. Stieberger, _Resolved Toroidal Orbifolds and their Orientifolds_, Adv.Theor.Math.Phys.12:67-183, 2008 ([arXiv:hep-th/0609014](https://arxiv.org/abs/hep-th/0609014))

* {#Reffert07} Susanne Reffert, _The Geometer's Toolkit to String Compactifications_, lectures at _[String and M theory approaches to particle physics and cosmology](https://www.ggi.infn.it/showevent.pl?id=11)_, 2007 ([arXiv:0706.1310](https://arxiv.org/abs/0706.1310))

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], Chapter 8 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012 ([doi:10.1017/CBO9781139018951](https://doi.org/10.1017/CBO9781139018951))



* {#BlumenhagenLustTheisen13} [[Ralph Blumenhagen]], [[Dieter Lüst]], [[Stefan Theisen]], Chapter 10.5 _Toroidal orbifolds_,  of _Basic Concepts of String Theory_ Part of the series Theoretical and Mathematical Physics pp 585-639 Springer 2013

and for orbifolds of [[G₂-manifolds]] for [[M-theory on G₂-manifolds]]:

* {#Acharya98} [[Bobby Acharya]], _M theory, Joyce Orbifolds and Super Yang-Mills_, Adv. Theor. Math. Phys. **3** (1999) 227-248 &lbrack;[arXiv:hep-th/9812205](http://arxiv.org/abs/hep-th/9812205)&rbrack;


* {#Reidegeld15} [[Frank Reidegeld]], _$G_2$-orbifolds from K3 surfaces with ADE-singularities_ &lbrack;[arXiv:1512.05114](http://arxiv.org/abs/1512.05114)&rbrack;

* [[Frank Reidegeld]], _$G_2$-orbifolds with ADE-singularities_ &lbrack;[pdf](https://core.ac.uk/download/pdf/159317626.pdf)&rbrack;

and for [[heterotic string theory|heterotic]] [[string phenomenology]]:

* [[Saul Ramos-Sanchez]], [[Michael Ratz]], *Heterotic Orbifold Models*, in *[[Handbook of Quantum Gravity]]*, Springer (2024) &lbrack;[arXiv:2401.03125](https://arxiv.org/abs/2401.03125), [doi:10.1007/978-981-19-3079-9](https://doi.org/10.1007/978-981-19-3079-9)&rbrack;


For [[topological strings]] the [[path integral as a pull-push transform]] for target orbifolds -- in analogy to what [[Gromov-Witten theory]] is for [[Deligne-Mumford stacks]] -- has first been considered in 

* {#ChenRuan01} [[Weimin Chen]], [[Yongbin Ruan]], _Orbifold Gromov-Witten Theory_, in _[[Orbifolds in Mathematics and Physics]]_ (Madison, WI, 2001), 25&#8211;85, Contemp. Math., 310, Amer. Math. Soc., Providence, RI, 2002 ([arXiv:math/0103156](http://arxiv.org/abs/math/0103156))

Review with further pointers:

* {#Abramovich05} [[Dan Abramovich]], _Lectures on Gromov-Witten invariants of orbifolds_ ([arXiv:math/0512372](http://arxiv.org/abs/math/0512372))

On non-supersymmetric [[flat orbifolds]] of [[supergravity]] theories:

* Anamaria Font, Alexis Hernandez, *Non-Supersymmetric Orbifolds*, Nucl. Phys. B **634** (2002) 51-70 &lbrack;[arXiv:hep-th/0202057](https://arxiv.org/abs/hep-th/0202057)&rbrack;

and specifically [[flux compactification|fluxed]] [[KK-compactification]] of [[D=6 supergravity]] on the [[pillowcase orbifold]]:

* Christoph Ludeling, *6D supergravity: Warped solution and gravity mediated supersymmetry breaking*, PhD thesis, Hamburg (2006) &lbrack;[doi:10.3204/DESY-THESIS-2006-020](https://doi.org/10.3204/DESY-THESIS-2006-020)&rbrack;


* Gero von Gersdorff, *Anomalies on Six Dimensional Orbifolds*, JHEP 0703:083 (2007) &lbrack;[arXiv:hep-th/0612212](https://arxiv.org/abs/hep-th/0612212)&rbrack;


* [[Markus Dierigl]], *Aspects of Six-Dimensional Flux Compactifications*, PhD thesis, Hamburg (2017) &lbrack;[doi:10.3204/PUBDB-2017-09253](https://doi.org/10.3204/PUBDB-2017-09253)&rbrack;


On [[supergravity]] [[KK-compactification|KK-compactified]] (and [[branes]] [[wrapped brane|wrapped]] on) [[spindle orbifolds]]:

* [[Pietro Ferrero]], [[Jerome P. Gauntlett]], Juan Manuel Pérez Ipiña, [[Dario Martelli]], [[James Sparks]], *D3-branes wrapped on a spindle*, Phys. Rev. Lett. **126** 111601 (2021) &lbrack;[arXiv:2204.02990](https://arxiv.org/abs/2204.02990), [doi:10.1103/PhysRevLett.126.111601](https://doi.org/10.1103/PhysRevLett.126.111601)&rbrack;

* [[Pietro Ferrero]], [[Jerome P. Gauntlett]], [[Dario Martelli]], [[James Sparks]], *M5-branes wrapped on a spindle*, J. High Energ. Phys. **2021** 2 (2021)
 &lbrack;[arXiv:2105.13344](https://arxiv.org/abs/2105.13344), <a href="https://doi.org/10.1007/JHEP11(2021)002">doi:10.1007/JHEP11(2021)002</a>&rbrack;
&rbrack;


* Federico Faedo, [[Dario Martelli]], *D4-branes wrapped on a spindle*, J. High Energ. Phys. **2022** 101 (2022) &lbrack;[arXiv:2111.13660](https://arxiv.org/abs/2111.13660), <a href="https://doi.org/10.1007/JHEP02(2022)101">doi:10.1007/JHEP02(2022)10</a>&rbrack;


* Christopher Couzens, *A tale of (M)2 twists*, J. High Energ. Phys. **2022** 78 (2022) &lbrack;[arXiv:2112.04462](https://arxiv.org/abs/2112.04462), <a href="https://doi.org/10.1007/JHEP03(2022)078">doi:10.1007/JHEP03(2022)078</a>&rbrack;

* K. C. Matthew Cheung, Jacob H. T. Fry, [[Jerome P. Gauntlett]], [[James Sparks]], *M5-branes wrapped on four-dimensional orbifolds*, J. High Energ. Phys. **2022** 82 (2022) &lbrack;[arXiv:2204.02990](https://arxiv.org/abs/2204.02990), <a href="https://doi.org/10.1007/JHEP08(2022)082">doi:10.1007/JHEP08(2022)082</a>&rbrack;

On orbifolds by [[2-groups]] in view of [[sigma-models]] inspired from [[string theory]]:

* [[Alonso Perez-Lona]], [[Eric Sharpe]], *Three-dimensional orbifolds by 2-groups* &lbrack;[arXiv:2303.16220](https://arxiv.org/abs/2303.16220)&rbrack;


### In condensed matter theory
 {#ReferencesInCondensedMatter}

In [[solid state physics]], the effective [[Brillouin torus]] of quasi-[[momenta]] of [[electrons]] in a [[crystal|crystalline material]] is generally an [[orbifold]], namely the [[quotient orbifold]] of [[Euclidean space]] (momentum space) by the corresponding [[crystallographic group]].

Explicit discussion of such *crystallographic orbifolds* for the purpose of [[crystallography]]:

* [[Carroll K. Johnson]], Michael N. Burnett, William D. Dunbar: *Crystallographic Topology and Its Applications*, in: *[Crystallographic Computing 7](https://www.iucr.org/resources/commissions/crystallographic-computing/schools/school96)* *Proceedings of the Macromolecular Crystallography Computing School* (1996) &lbrack;[pdf](https://www.iucr.org/__data/assets/pdf_file/0010/9001/cj.pdf), [[JohnsonEtAl-CrystallographicTopology.pdf:file]]&rbrack;

* [[Carroll K. Johnson]]: *Crystallographic Topology 2: Overview and Work in Progress*, in: *Trends in Mathematical Physics*, AMS/International Press (1999) &lbrack;[amsip:13](https://bookstore.ams.org/amsip-13), [[Johnson-CrystalTopology2.pdf:file]]&rbrack;

* [[Carroll K. Johnson]], Michael N. Burnett: *Crystallographic Topology -- The Topology of Crystallographic Groups and Simple Crystal Structures* &lbrack;[webpage](https://ornl-ndav.github.io/ortep/topology.html)&rbrack;

  * 2.2. [Euclidean 2-Orbifolds from Plane Groups](https://ornl-ndav.github.io/ortep/topology/orbfld2.html)

  * [Orbifold atlas](https://ornl-ndav.github.io/ortep/topology/atlas/atlas.html)

* [[Olaf Delgado Friedrichs]], [[Daniel H. Huson]]: *Orbifold Triangulations and Crystallographic Groups*, Periodica Mathematica Hungarica **34** (1997) 29–55 &lbrack;[doi:10.1023/A:1004220406857](https://doi.org/10.1023/A:1004220406857)&rbrack;
  > (relation to [[equivariant triangulations]])

In the [[physics]] literature this orbifold nature of the [[Brillouin torus]] is not often made explicit, but see articles in the context of crystalline [[topological phases of matter]]:

* [[Kiyonori Gomi]], [[Guo Chuan Thiang]]: *Crystallographic T-duality*, J. Geom. Phys **139** (2019) 50-77 &lbrack;[arXiv:1806.11385](https://arxiv.org/abs/1806.11385), [doi:10.1016/j.geomphys.2019.01.002](https://doi.org/10.1016/j.geomphys.2019.01.002)&rbrack;

* [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Anyonic topological order in TED K-theory]]*, Reviews in Mathematical Physics **35** 03 (2023) 2350001 &lbrack;[arXiv:2206.13563](https://arxiv.org/abs/2206.13563), [doi:10.1142/S0129055X23500010](https://doi.org/10.1142/S0129055X23500010)&rbrack;



category: Lie theory



[[!redirects orbifolds]]

[[!redirects effective orbifold]]
[[!redirects effective orbifolds]]

