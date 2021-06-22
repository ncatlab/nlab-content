
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
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

Given a [[simplicial group]] $G_\bullet$, the _Borel model structure_ is a [[model category]] structure on the [[category]] of [[simplicial sets]] equipped with $G$-[[action]] which presents the [[(∞,1)-category]] of [[∞-actions]] of the [[∞-group]] (see there) presented by $G$.

In the context of [[equivariant homotopy theory]] this is also called the "coarse model structure" (e.g. [Guillou, section 5](#Guillou)), since it is not equivalent to the "fine" homotopy theory of [[G-spaces]] which enters [[Elmendorf's theorem]].


## Definition


\begin{defn}\label{BorelModelStructure}

For $G_\bullet$ a [[simplicial group]] write 

* $\mathbf{B}G_\bullet$ for the one-object [[sSet-enriched category]] (here: a [[simplicial groupoid]]) whose [[hom-object]] is $G_\bullet$. 

* $G_\bullet Actions(sSet) \;\coloneqq\; sSetCat\big(\mathbf{B}G_\bullet, sSet\big)$ for the [[sSet]]-[[enriched functor category]] to [[SimplicialSets]].

* $G_\bullet Actions(sSet)_{proj} \coloneqq sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ for the projective [[model structure on functors]] (projective [[model structure on simplicial presheaves]]). 

This is the $G_\bullet$ *Borel model structure*, naturally a [[simplicial model category]] ([DDK 80, Prop. 2.4](#DDK80), [Goerss & Jardine 09, Chapter V, Thm. 2.3](#GoerssJardine09)).

\end{defn}

## Properties

### Cofibrant replacement and homotopy quotients/fixed points
 {#CofibrantReplacementAndHomotopyQuotientsFixedPoints}

\begin{prop}\label{CofibrationsOfSimplicialActions}
**(cofibrations of simplicial actions)** \linebreak
The cofibrations $i \colon X \to Y$ in $sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ (Def. \ref{BorelModelStructure}) are precisely those morphisms such that

1. the underlying morphism of [[simplicial sets]] is a [[monomorphism]];

1. the $G_\bullet$-[[action]] is a relatively [[free action]], i.e. [[free action|free]] on all [[simplices]] not in the [[image]] of $i$.

\end{prop}

This is ([DDK 80, Prop. 2.2. (ii)](#DDK80), [Guillou, Prop. 5.3](#Guillou)).



\begin{remark}
In particular this means that an object is [[cofibrant object|cofibrant]] 
in $sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ if the $G_\bullet$-[[action]] on it is [[free action|free]]. 

Hence [[cofibrant replacement]] is obtained by forming the [[Cartesian product|product]] with the model $W G_\bullet$ for the total space of the [[universal principal bundle]] over $G_\bullet$ (see at _[[simplicial group]]_ for notation and more details).
\end{remark}

\begin{remark}
It follows that for $X, A \in sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}$ the [[derived hom space]]

$$
  R Hom_G(X,A)
$$

models the Borel $G$-[[equivariant cohomology]] of $X$ with [[coefficients]] in $A$. 

In particular,if $A$ is [[fibrant object|fibrant]] (the underlying simplicial set is a [[Kan complex]]) then 

1. if the $G_\bullet$-action on $A$ is trivial, then 

   $$
     R Hom_G(X,A) 
       \simeq 
     Hom_G(W G \times X , A) 
       \simeq 
     Hom(W G \times_G X, A)
   $$

   is equivalently maps of [[simplicial sets]] out of the [[Borel construction]] on $X$;

1. if $X = \ast $ is the [[point]] then 

   $$
     R Hom_G(X,A) 
       \simeq 
     Hom_G(W G, A) 
       \simeq 
     Hom(\overline{W} G , A)  
       \simeq 
     A^{h G}
   $$

   is the [[homotopy fixed points]] of $A$.

\end{remark}


### Relation to the slice over the simplicial classifying space
 {#RelationToSliceOverSimplicialClassifyingSpace}

\begin{prop}\label{QuillenEquivalenceToSliceOverSimplicialClassifyingSpace}
  For $G$ a [[simplicial group]], there is a pair of [[adjoint functors]]
  \[
    \label{QuillenAdjunctionWithSliceOverSimplicialClassifyingSpace}
    sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj}
      \underoverset
        {\underset{ \big((-) \times W G\big)/G }{\longrightarrow}}
        {\overset{ (-) \times_{\overline{W}G} W G  }{\longleftarrow}}
        {\bot}
    sSet_{/\overline{W}G}
  \]
  which constitute a [[simplicial Quillen adjunction|simplicial]] [[Quillen equivalence]] between the Borel model structure (Def. \ref{BorelModelStructure}) and the [[slice model structure]] of the [[classical model structure on simplicial sets]] slices over the [[simplicial classifying space]] $\overline{W}G$.,
  
\end{prop}

([DDK 80, Prop. 2.3, Prop. 2.4](#DDK80)) Here:

* the [[right adjoint]] forms [[associated bundles]] to [[universal principal bundles]] 

* the [[left adjoint]] forms [[homotopy fibers]].

In fact, these are [[sSet]]-[[enriched functors]] which induced an [[equivalence of (infinity,1)-categories]] between the [[simplicial localizations]]  $L_W sSetCat\big(\mathbf{B}G_\bullet, sSet\big)_{proj} \simeq L_W sSet_{/\overline{W}H}$ ([DDK 80, Prop. 2.5](#DDK80)).

This kind of relation is discussed in more detail at _[[∞-action]]_.


\begin{remark}\label{sSetEnrichmentOfAdjunctionToSliceOverSimpClassSpace}
**(sSet-enrichement of the adjunction)** \linebreak
The statement that (eq:QuillenAdjunctionWithSliceOverSimplicialClassifyingSpace) is an [[sSet]]-*[[enriched adjunction]]* is not made explicit in [DDK 80](#DDK80); there it only says that the functors form a plain [[adjoint functors|adjunction]] ([DDK 80, Prop. 2.3](#DDK80)) and that they are each [[sSet]]-[[enriched functors]] ([DDK 80, Prop. 2.4](#DDK80)). 

The remaining observation that we have a [[natural isomorphism]] of [[sSet]]-[[hom-objects]]

$$
  \big[
    X \times_{\overline{W}G} W G,
    \,
    V
  \big]
  \;\simeq\;
  \big[
    X,
    \,
    (V \times W G)/G
  \big]
$$

hence

$$
  Hom
  \Big(
    \big( X \times_{\overline{W}G} W G \big) \times \Delta[\bullet],
    \,
    V
  \Big)
  \;\simeq\;
  Hom
  \big(
    X \times \Delta[\bullet],
    \,
    (V \times W G)/G
  \big)
$$

follows from the plain adjunction and the natural isomorphism

$$
  (X \times_{\overline{W}G} W G) \times \Delta[\bullet] 
  \;\simeq\;
  (X \times \Delta[\bullet]) \times_{\overline{W}G} W G  
  \,,
$$

which, in turn, follows, for instance, via the [[pasting law]]:

\begin{tikzcd}
  {
    { (X \times_{\overline{W}G} W G) \times \Delta[k] } 
    \atop
    { \mathllap{\simeq} (X \times \Delta[k]) \times_{\overline{W}G} W G  } 
  }
  \ar[r]
  \ar[d]
  \ar[dr,phantom,"\mbox{\tiny\rm(pb)}"]
  & 
  X \times \Delta[k]
  \ar[
    d,
    "\mathrm{pr}_1"
  ]
  \\
  X \times_{\overline{W}G} W G
  \ar[r]
  \ar[d]
  \ar[dr,phantom,"\mbox{\tiny\rm(pb)}"]
  & 
  X 
  \ar[
    d
  ]
  \\
  W G
  \ar[r]
  &
  \overline{W}G
  \,.
\end{tikzcd}

\end{remark}

### Relation to the model structure on plain simplicial sets
 {#RelationToModelStructureOnPlainSimplicialSets}

> under construction

For $\mathcal{G} \,\in\, Groups(sSets)$ a [[simplicial group]], write $\mathcal{G}Actions(sSets)$ for the [[category]] of $\mathcal{G}$-[[actions]] on [[simplicial sets]].

\begin{proposition}\label{CofreeAction}
**(underlying simplicial sets and cofree simplicial action)** \linebreak
  The [[forgetful functor]] $undrl$ from $\mathcal{G}Actions$ to underlying simplicial sets is a [[left Quillen functor]] from the Borel model structure (Def. \ref{BorelModelStructure}) to the [[classical model structure on simplicial sets]].

Its [[right adjoint]]

$$
  sSet
  \underoverset
    {\underset{ \;\;\; [\mathcal{G},-] \;\;\; }{\longrightarrow}}
    {\overset{ \;\;\; undrl \;\;\; }{\longleftarrow}}
    {\bot}
  \mathcal{G}Actions(sSet)
$$

sends $X \in sSet$ to 

* the simplicial set 

  $$
    [\mathcal{G},X] 
    \;\coloneqq\;
    Hom_{sSet}\big( \mathcal{G} \times \Delta[\bullet], X\big) 
    \;\;\;
    \in
    sSet
  $$

* equipped with the $\mathcal{G}$-action

  $$
    \mathcal{G} \times [\mathcal{G},X]
    \longrightarrow 
    \mathcal{G}
  $$

  which in degree $n \in \mathbb{N}$ is the [[function]] 

  $$
    Hom(\Delta[n], \mathcal{G})
    \,\times\,
    Hom
    \big(
      \mathcal{G} \times \Delta[n],
      \,
      X
    \big)
    \longrightarrow
    Hom
    \big(
      \mathcal{G} \times \Delta[n],
      \,
      X
    \big)    
  $$

  that sends

  \[
  \label{CofreeSimplicialActionInComponents}
  \begin{aligned}
  &
  \Big(
    \mathcal{G}\times \Delta[n]
    \overset{\phi}{\to}
    X,
    \;
    \Delta[n] \overset{g_n}{\to} \mathcal{G}
  \Big)
  \\
  \;\;\mapsto\;\;
  &
  \Big(
  \mathcal{G} \times \Delta[n]
  \overset{id \times diag}{\longrightarrow}
  \mathcal{G} \times \Delta[n] \times \Delta[n]
  \overset{ id \times g_n \times id }{\longrightarrow}
  \mathcal{G} \times \mathcal{G} \times \Delta[n]
  \overset{(-)\cdot(-) \times id}{\to}
  \mathcal{G} \times \Delta[n]
  \overset{\phi}{\to}
   X
  \Big)
  \end{aligned}
  \]

\end{proposition} 

\begin{proof}

We already know from Def. \ref{BorelModelStructure} that $underl$ preserves all [[weak equivalences]] and from Prop. \ref{CofibrationsOfSimplicialActions} that it preserves all [[cofibrations]]. Therefore it is a left Quillen functor as soon as it is a [[left adjoint]].

The idea of the existence of the cofree right adjoint is familiar from [[topological G-space]] (see the section on [coinduced actions](topological+G-space#CoinducedActions) there).

For $P \in \mathcal{G}Actions(sSet)$, and $X \in sSet$, we check the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism)

$$
  \big\{
    P \overset{\;\;\phi_{(-)}\;\;}{\longrightarrow} [G,X]
  \big\}
  \;\;\;\overset{ \;\; \widetilde{(-)} \;\; }{\leftrightarrow}\;\;\;
  \big\{
    undrl(P) \overset{\;\; {\widetilde \phi}_{(-)} \;\; }{\longrightarrow} X
  \big\}
  \,.
$$

Given

$$
  \phi_{(-)}
  \;\colon\;
  p_n 
  \mapsto 
  \big(
    \phi_{p_n}
    \;\colon\;
    \mathcal{G} \times \Delta[n] \to X
  \big)
$$

define

\[
  \label{AdjunctOfHomomorphismToCofreeSimplicialAction}
  \widetilde \phi_{(-)}
  \;\colon\;
  p_n 
  \mapsto
  \phi_{p_n}(e_n, \sigma_n)
  \,,
\]

where $e_n \in \mathcal{G}_n$ denotes the [[neutral element]] in degree $n \in \mathbb{N}$ and where $\sigma_n \in (\Delta[n])_n$ denotes the unique non-degenerate element $n$-cell in the [[n-simplex]].

We need to show that ${\widetilde \phi}_{(-)} \colon undrl(P) \to X$ already determines all of $\phi_{(-)}$.

Write $\sigma_n \in (\Delta[n])_n$ for the unique non-degenerate simplex in that degree, and observe that $\phi_{p_n}$ is uniquely fixed by its values  $\phi_{p_n}( -, \sigma_n )$ on this simplex. Now for any $g_n \in \mathcal{G}_n$ observe the following sequence of identifications:

$$
  \begin{aligned} 
    \phi_{p_n}(g_n, \sigma_n)
    & \;=\;
    \phi_{p_n}( e_n \cdot g_n, \sigma_n )
    \\
    & \;=\;
    \big(
      g_n \cdot \phi_{p_n}
    \big)
    ( e_n, \sigma_n )
    \\
    & \;=\;
    \phi_{ g_n \cdot p_n }
    (e_n, \sigma_n)
    \\
    & \;=\;
    {\widetilde \phi}_{g_n \cdot p_n}
  \end{aligned}
$$

Here

* the first step is the unit law in the component group $\mathcal{G}_n$;

* the second step uses the definition (eq:CofreeSimplicialActionInComponents) of the cofree action;

* the third step is the assumption that $\phi_{(-)}$ is a homomorphism of $\mathcal{G}$-actions ([[equivariant function|equivariance]]);

* the fourth step is the definition (eq:AdjunctOfHomomorphismToCofreeSimplicialAction).


\end{proof}



### Relation to the fine model structure of equivariant homotopy theory

The [[identity functor]] goves a [[Quillen adjunction]] between the Borel model structure and [[equivariant homotopy theory]] ([Guillou, section 5](#Guillou)).

The left adjoint is

$$
  L = id 
    \;\colon\; 
  G_\bullet Act_{coarse} 
    \longrightarrow 
  G_\bullet Act_{fine}
$$

from the Borel model structure to the genuine [[equivariant homotopy theory]].

Because:

First of all, by ([Guillou, theorem 3.12, example 4.2](#Guillou)) $sSet^{\mathbf{B}G_\bullet}$ does carry a fine model structure. By ([Guillou, last line of page 3](#Guillou)) the fibrations and weak equivalences here are those maps which are ordinary fibrations and weak equivalences, respectively, on $H$-[[fixed point]] simplicial sets, for all subgroups $H$. This includes in particular the trivial subgroup and hence the identity functor

$$
  R = id \;\colon\; G_\bullet Act_{fine} \longrightarrow G_\bullet Act_{coarse}
$$

is right Quillen.

## References


The model structure, the characterization of its cofibrations, and its equivalence to the [[slice model structure]] of $sSet$ over $\bar W G$ is due to

* {#DDK80} [[Emmanuel Dror]], [[William Dwyer]], [[Daniel Kan]], _Equivariant maps which are self homotopy equivalences_, Proc. Amer. Math. Soc. 80 (1980), no. 4, 670&#8211;672 ([jstor:2043448](http://www.jstor.org/stable/2043448))

This Quillen equivalence also mentioned as:

* {#Dwyer2008} [[William Dwyer]], Exercise 4.2 in: _Homotopy theory of classifying spaces_, Lecture notes, Copenhagen 2008, ([pdf](http://www.math.ku.dk/~jg/homotopical2008/Dwyer.CopenhagenNotes.pdf), [[Dwyer_HomotopyTheoryOfClassifyingSpaces.pdf:file]])

Discussion in relation to the "fine" model structure of [[equivariant homotopy theory]] which appears in [[Elmendorf's theorem]] is in 

* {#Guillou} [[Bert Guillou]], _A short note on models for equivariant homotopy theory_, 2006 ([pdf](http://www.math.uiuc.edu/~bertg/EquivModels.pdf), [[GuillouModelsForEquivariantHomotopyTheory.pdf:file]])

Textbook account of (just) the Borel model structure:

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section V.2 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) ([doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/))


Discussion with the model of [[∞-groups]] by [[simplicial groups]] replaced by groupal [[Segal spaces]] is in 

* [[Matan Prasma]], _Segal Group Actions_ ([arXiv:1311.4749](http://arxiv.org/abs/1311.4749))

Discussion of a [[global equivariant homotopy theory|globalized]] model structure for actions of all simplicial groups is in

* [[Yonatan Harpaz]], [[Matan Prasma]], section 6.2 of _The Grothendieck construction for model categories_ ([arXiv:1404.1852](http://arxiv.org/abs/1404.1852))


[[!redirects Borel model structures]]

