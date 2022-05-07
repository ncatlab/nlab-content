
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[simplicial group]], there is a [[reduced simplicial set|reduced]] [[simplicial set]], traditionally denoted $\overline W G$ and called the *[[classifying space]]* or *classifying complex* of $G$, which is a model for the [[delooping]] of $G$ and such that the [[functor]] $\overline{W}(-)$ is [[right adjoint]] to the standard [[simplicial loop space]]-construction $G$ (here denoted by $L$ to avoid a clash of notations).

This pair of [[adjoint functors]] 
$$
  SimplicialGroups
    \underoverset
      {\;\;\;\underset{\overline{W}}{\longrightarrow}\;\;\;}
      {\;\;\;\overset{L}{\longleftarrow}\;\;\;}
      {\bot}
  SimplicialSets_{red}
$$
is a [[Quillen equivalence]] between the [[model structure on simplicial groups]] and the [[model structure on reduced simplicial sets]], modelling [[looping and delooping]] of [[homotopy types]] in [[simplicial homotopy theory]].

## Definition

### In components

\begin{definition}\label{WGAndBarWGInComponents}
  For $G$ a [[simplicial group]], 
  one writes
  $$
    W G
    \;\in\;
    SimplicialSets
  $$
  for the the [[simplicial set]] whose

  * underlying sets are
    $$
      (W G)_n
      \;\coloneqq\;
      G_{n} \times G_{n-1} \times \cdots \times G_0
    $$
 
  * face maps are given by

    $$
      d_i
      \big(
        g_n, g_{n-1}, \cdots, g_0
      \big)
      \;\coloneqq\;
      \left\{
      \array{
        \big(
          d_i(g_n), 
          \,
          d_{i-1}(g_{n-1}),
          \,
          \cdots
          ,\,
          d_0(g_{n-i}) \cdot g_{n-i-1},
          \,
          g_{n -  i - 2}, 
          \,
          \cdots,
          \,
          g_0
        \big)
        & \text{if} &
        i \lt n
        \\
        \big(
          d_n(g_n),
          \,
          d_{n-1}(g_{n-1}),
          \,
          \cdots,
          \,
          d_1(g_1)
        \big)
        & \text{if} &
        i = n
      }
      \right.
    $$

* degeneracy maps are given by

  $$
    s_i(g_n, g_{n-1}, \cdots, g_0)
    \;\coloneqq\;
    \big(
      s_i(g_n),
      \,
      s_{i - 1}(g_{n-1}),
      \,
      \cdots,
      \,
      s_0(g_{n-1}),
      \,
      e,
      \,
      g_{n-i-1},
      \,
      \cdots,
      \,
      g_0
    \big)
    \,,
  $$

  where $e$ denotes the respective [[neutral element]].

This carries a $G$-[[action]] by left multiplication on the first factor:

\[
  \label{GActionOnWG}
  \array{
    G \times W G &\overset{}{\longrightarrow}& W G
    \\
    \big(h_n, (g_n, g_{n-1}, \cdots, g_0)\big)
     &\mapsto&
    (h_n \cdot g_n, \, g_{n-1}, \cdots, g_0)
    \mathrlap{\,.}
  }
\]

The [[quotient]] of $W G$ by this $G$-action (eq:GActionOnWG) is denoted

\[
  \label{OverlineWGAsQuotientOfWG}
  \overline{W} G
  \;\coloneqq\;
  W G / G
\]

and the quotient [[coprojection]]

$$
  W G \longrightarrow \overline{W} G
$$

is known as the standard model for the simplicial $G$-[[universal principal bundle]] (see [below](#ClassificationOfSimplicialPrincipalBundles)).

\end{definition}

(due to [MacLane 54, p. 3](#MacLane54), [Kan 58, Def. 10.3](#Kan58), see also [Goerss & Jardine 09, p. 269](#GoerssJardine09))


\begin{example}
  In the special case that 
  $$
    G \in Groups \overset{const}{\hookrightarrow} SimplicialGroups
  $$
  is an ordinary [[discrete group]] regarded as a [[simplicial group]] (which is [[constant functor|constant]] as a [[functor]] on the [[opposite category|opposite]] [[simplex category]]) the definitions in Def. \ref{WGAndBarWGInComponents} reduce as follows:

The simplicial set $W G$ is that whose

  * underlying sets are
    $$
      (W G)_n
      \;\coloneqq\;
      G^{\times_{n + 1}}
    $$
 
  * face maps are given by

    $$
      d_i
      \big(
        g_n, g_{n-1}, \cdots, g_0
      \big)
      \;\coloneqq\;
      \left\{
      \array{
        \big(
          g_n, 
          \,
          g_{n-1},
          \,
          \cdots
          ,\,
          g_{n-i} \cdot g_{n-i-1},
          \,
          g_{n -  i - 2}, 
          \,
          \cdots,
          \,
          g_0
        \big)
        & \text{if} &
        i \lt n
        \\
        \big(
          g_n,
          \,
          g_{n-1},
          \,
          \cdots,
          \,
          g_1
        \big)
        & \text{if} &
        i = n
      }
      \right.
    $$

* degeneracy maps are given by

  $$
    s_i(g_n, g_{n-1}, \cdots, g_1)
    \;\coloneqq\;
    \big(
      g_n,
      \,
      g_{n-1},
      \,
      \cdots,
      \,
      g_{n-1},
      \,
      e,
      \,
      g_{n-i-1},
      \,
      \cdots,
      \,
      g_0
    \big)
    \,,
  $$

This identifies

$$
  W G 
  \;=\;
  N
  \big( 
    G \times G
      \rightrightarrows
    G
  \big)
$$

with the [[nerve]] of the [[action groupoid]] of $G$ acting on itself by right multiplication ([[isomorphism|isomorphic]] to the [[pair groupoid]] on the underlying set of $G$):

\begin{tikzcd}
  & g_2 g_1
  \ar[
    dr,
    "{(g_2 g_1, g_0)}"{sloped, near start},
    ""{name=s, below, pos=0.01}
  ]
  \\
  g_2
  \ar[
    ur,
    "{(g_2, g_1)}"{sloped, near end}
  ]
  \ar[
    rr,
    "{(g_2, g_1 g_0)}"{below},
    ""{name=t, above}
  ]
  &
  {}
  &
  g_2 g_1 g_0
  \ar[
    from=s, to=t,
    Rightarrow,
    "{(g_2, g_1, g_0)}"{description}
  ]
\end{tikzcd}

Finally this means that the simplicial classifying complex (eq:OverlineWGAsQuotientOfWG) of an ordinary group is isomorphic to the [[nerve]] of its [[delooping groupoid]]:

$$
  \overline{W}G
  \;\simeq\;
  N
  \big(
    G \rightrightarrows \ast
  \big)
  \,.
$$

\end{example}



### Via total simplicial sets
 {#ViaTotalSimplicialSets}

Equivalently, $\overline{W}(-)$ is the following [[composition|composite]] [[functor]]:

$$
  \overline{W}
  \;\colon\;
  [\Delta^{op}, Groups]
  \overset
    {\;\;[\Delta^{op}, \mathbf{B}]\;\;}
    {\longrightarrow}
  [\Delta^{op}, Groupoids]
  \overset
    {\;\;[\Delta^{op}, N]\;\;}
    {\longrightarrow}
  [\Delta^{op}, SimplicialSets]  
  \overset
    {\;\;\sigma_\ast\;\;}
    {\longrightarrow}
  SimplicialSets
  \,.
$$

([Stevenson 11, Lemma 15](#Stevenson11) following [[John Duskin]], see also [NSS 12, Def. 3.26](#NSS12))

Here:

* $\mathbf{B} \;\colon\; Groups \to Groupoids$ forms the one-object groupoid with [[hom-set]] the given group (the *[[delooping groupoid]]*);

* $N \;\colon\; Groupoids \longrightarrow SimplicialSets $ is the [[nerve]] construction;

* $\sigma_\ast$ is the [[total simplicial set]]-functor ([[right adjoint]] to pre-composition with [[ordinal sum]]).


## Properties

In all of the following, $G$ is any simplicial group.


### Basic properties
 {#KanFibrancy}

\begin{prop}
  The simplicial set $\overline{W}G$ is a [[Kan complex]].
\end{prop}
(e.g. [Goerss & Jardine 09, Sec. V Cor. 6.8 (p. 287)](#GoerssJardine09))

\begin{prop}
  The coprojection $W G \overset{}{\longrightarrow} \overline{W}G$
  is a [[Kan fibration]].
\end{prop}
(e.g [Goerss & Jardine 09, Sec. V Lemma 4.1 (p. 270)](#GoerssJardine09))

\begin{prop}
  The simplicial set $W G$ is [[contractible]].
\end{prop}
(e.g [Goerss & Jardine 09, Sec. V Lemma 4.6 (p. 270)](#GoerssJardine09))

### Classification of simplicial principal bundles 
 {#ClassificationOfSimplicialPrincipalBundles}

The object $\overline{W}G$ serves as the [[classifying space]] for [[simplicial principal bundles]] ([May 67, §21](#May67), [Goerss & Jardine 09, Section V, Thm. 3.9](#GoerssJardine09), see also [NSS 12, Section 4.1](#NSS12)).

### Slice model structure
 {#SliceModelStructure}

The [[slice model category]] of the [[classical model structure on simplicial sets]] over the simplicial classifying complex $\overline{W}G$ is [[Quillen equivalence|Quillen equivalent]] to the [[Borel model structure]] for $G$-[[equivariant homotopy theory]]:

$$
  \big(
    SimplicialSets_{Qu}
  \big)_{/\overline{W} G}
  \;\simeq_{Qu}\;
  G Actions(SimplicialSets)_{proj}
  \,.
$$

([Dror, Dwyer & Kan 1980](#DDK80)) See [there](Borel+model+structure#RelationToSliceOverSimplicialClassifyingSpace) for details. This is a model for the general abstract situation discussed at *[[∞-action]]*.


## Related concepts

* [[simplicial loop functor]]

* [[simplicial homotopy theory]]

* [[Borel model structure]]


## References

The idea of constructing $\overline{W}$ using the [[bar construction]]
is due to [[Eilenberg]] and [[MacLane]], who apply it to [[simplicial rings]] with the usual [[tensor product]] operation:

* {#EilenbergMacLane53I} [[Samuel Eilenberg]], [[Saunders Mac Lane]], _On the Groups $H(\Pi,n)$, I_, Annals of Mathematics Second Series, Vol. 58, No. 1 (Jul., 1953), pp. 55-106 ([jstor:1969820](https://www.jstor.org/stable/1969820)) (See, in particular, §17.)

This was also later discussed in

* {#MacLane54} [[Saunders MacLane]], *Constructions simpliciales acycliques*, Colloque Henri Poincar&eacute; 1954 ([[MacLaneConstructionsSimplicialesAcycliques.pdf:file]])  (See, in particular, §3.)

The first reference where $\bar W$ is defined explicitly for [[simplicial groups]] and the adjunction between [[simplicial groups]] and [[reduced simplicial sets]] is explicitly spelled out is

* {#Kan58} [[Daniel Kan]], Sections 10-11 in: _On homotopy theory and c.s.s. groups_, Ann. of Math. 68 (1958), 38-53 ([jstor:1970042](https://www.jstor.org/stable/1970042))

The [[left adjoint]] [[simplicial loop space]] functor $L$ is also discussed by [[Kan]] (there denoted "$G$") in 

* [[Daniel M. Kan]], §7 of: _A combinatorial definition of homotopy groups_, Annals of Mathematics 67:2 (1958), 282–312.  [doi](https://doi.org/10.2307/1970006).

The [[Quillen equivalence]] was established in

* {#Quillen69} [[Dan Quillen]], Section 2 of: _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([jstor:1970725](http://www.jstor.org/stable/1970725))

Textbook accounts:

* {#May67} [[Peter May]], p. 87-88 in: _Simplicial objects in algebraic topology_, University of Chicago Press 1967 ([ISBN:9780226511818](https://press.uchicago.edu/ucp/books/book/chicago/S/bo5956688.html), [djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu), [[May_SimplicialObjectsInAlgebraicTopology.pdf:file]])

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section V.4 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))

Streamlining:

* {#Stevenson11} [[Danny Stevenson]], around Lemma 15 of: *Décalage and Kan's simplicial loop group functor*, Theory and Applications of Categories, Vol. 26, 2012, No. 28, pp 768-787 ([arXiv:1112.0474](https://arxiv.org/abs/1112.0474), [tac:26-28](http://www.tac.mta.ca/tac/volumes/26/28/26-28abs.html))

Identification of the [[slice model structure]] over $\overline{W}G$ with the [[Borel model structure]]:

* {#DDK80} [[Emmanuel Dror]], [[William Dwyer]], [[Daniel Kan]], _Equivariant maps which are self homotopy equivalences_, Proc. Amer. Math. Soc. 80 (1980), no. 4, 670&#8211;672 ([jstor:2043448](http://www.jstor.org/stable/2043448))

Generalization to [[simplicial presheaves]]:

* {#NSS12} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], Section 3.5 of: _Principal $\infty$-bundles -- _Presentations_, Journal of Homotopy and Related Structures, Volume 10, Issue 3 (2015), pages 565-622 ([doi:10.1007/s40062-014-0077-4](http://link.springer.com/article/10.1007/s40062-014-0077-4), [arXiv:1207.0249](http://arxiv.org/abs/1207.0249))

[[!redirects simplicial classifying spaces]]

[[!redirects simplicial classifying complex]]
[[!redirects simplicial classifying complexes]]

[[!redirects simplicial delooping]]
[[!redirects simplicial deloopings]]

[[!redirects simplicial delooping functor]]
[[!redirects simplicial delooping functors]]
