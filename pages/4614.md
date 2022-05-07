
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $X_\bullet$ a [[simplicial object]] in [[Top]] --  a [[simplicial topological space]] -- its _[[geometric realization]]_ is a plain [[topological space]] ${|X_\bullet|} \in Top$ obtained by gluing all topological space $X_n$ together, as determined by the face and degeneracy maps.

The construction of ${|X_\bullet|}$ is a direct analog of the ordinary notion of [[geometric realization]] of a [[simplicial set]], but taking into account the [[topology]] on the spaces of $n$-simplices $X_n$.

The [[duality|dual]] concept is that of [[totalization]] of [[cosimplicial topological spaces]].


## Definition

Let [[Top]] in the following denote either

* the [[category]] of [[compactly generated space|compactly generated]] [[weakly Hausdorff space]]s, or

* the category of [[k-space]]s.

Let $\Delta$ denote the [[simplex category]], and write $\Delta_{Top} \colon \Delta \to Top \colon  [n] \mapsto \Delta^n_{Top}$ for the standard [[cosimplicial object|cosimplicial]] [[topological space]] of topological [[simplices]].

Write equivalently

$$
  Top^{\Delta^{op}} \coloneqq  sTop \coloneqq  [\Delta^{op}, Top]
$$

for the category of [[simplicial topological spaces]].

+-- {: .num_defn #GeometricRealization}
###### Definition

For $X_\bullet \colon  \Delta^{op} \to Top$ a [[simplicial topological space]], its **geometric realization** is the [[coend]]

$$
  {|X_\bullet|} \coloneqq  \int^{n \in \Delta} X_n \times \Delta^n_{Top}
$$

formed in [[Top]].
=--

This operation naturally extends to a [[functor]]

$$
  {|-|} \colon sTop \to Top
  \,.
$$

More explicitly, $\vert X_\bullet \vert$ is the [[topological space]] given by the [[quotient]]

$$
  {\vert X_\bullet \vert} = \coprod_{n} X_n \times \Delta^n_{Top} /\sim
$$

where the [[equivalence relation]] "$\sim$" identifies, for every morphism $[k] \to [l]$ in $\Delta$, the points $(x,f_* p) \in X_l \times \Delta^l_{Top}$ and $(f^* x,p) \in X_k \times \Delta^k_{Top}$.

This form of geometric realization of simplicial topological spaces goes back to ([Segal68](#Segal68)). An early reference that realizes this construction as a [[coend]] is ([MacLane](#MacLane)).

One also considers geometric realization after [restricting](semi-simplicial+set#AdjunctionWithSimplicialSets) to the subcategory $\Delta_+ \overset{j^{op}}{\hookrightarrow} \Delta$ of the [[simplex category]] on the strictly increasing maps (that is, the coface maps only---no codegeneracies). (This yields the underlying *[[semi-simplicial set]]*).

+-- {: .num_defn #FatGeometricRealization}
###### Definition

The corresponding [[coend]] in [[Top]] is called the **fat geometric realization** 

$$
  {\Vert X_\bullet\Vert} \coloneqq   \int^{n \in \Delta_+} X_n \times \Delta^n_{Top}
  \,.
$$

=--

This is called _fat_ ,  because it does not [[quotient]] out the [[relation]]s induced by the degeneracy maps and hence is "bigger" than ordinary geometric realization.

Explicitly, this is the [[topological space]] given by the [[quotient]]

$$
  {\Vert X_\bullet \Vert} = \coprod_{n} X_n\times \Delta^n_{Top} /{\sim_+}
$$

where the [[equivalence relation]] "$\sim_+$" identifies $(x,f_* p) \in X_l\times \Delta^l_{Top}$ with $(f^* x,p) \in X_k\times \Delta^k_{Top}$ only when $[k] \to [l]$ is a coface map.

+-- {: .num_example #GeometricRealizationOfThePoint}
###### Example

The geometric realization of the point --- the [[simplicial topological space]] that is in each degree the 1-point topological space --- is [[homeomorphic]] to the point, but the fat geometric realization of the point is an "infinite dimensional topological ball": the [[terminal object|terminal]] morphism

$$
  {\vert * \vert} \stackrel{\simeq_{iso}}{\longrightarrow} *
$$

is an [[isomorphism]], but the morphism

$$
  {\Vert * \Vert} \stackrel{\simeq_{h.e.}}{\longrightarrow} *
$$

is just a [[homotopy equivalence]].

=--

+-- {: .num_remark}
###### Remark
The ordinary geometric realization can be described as the [[tensor product of functors]] ${|X_\bullet|}=\Delta^\bullet \otimes_{\Delta} X_\bullet$, and the fat geometric realization can likewise be described as ${\Vert X_\bullet\Vert} = i^* \Delta^\bullet \otimes_{\Delta_+} i^* X_\bullet$, where $i\colon \Delta_+ \hookrightarrow \Delta$ is the inclusion.  By general facts about tensor product of functors (essentially, the associativity of composition of [[profunctors]]), it follows that we can also write ${\Vert X_\bullet\Vert} \cong \Delta^\bullet \otimes_{\Delta} \Lan_i i^* X_\bullet \cong {| Lan_i i^* X_\bullet |} $.  In other words, the fat geometric realization of $X_\bullet$ is the ordinary geometric realization of a "fattened up" version of $X_\bullet$, which is obtained by forgetting the degeneracy maps of $X_\bullet$ and then "freely throwing in new ones."
=--


## Reminder on nice simplicial topological spaces

Simplicial topological spaces are in [[homotopy theory]] presentations for certain [[topological ∞-groupoid]]s . In this context what matters is not the operation of geometric realization itself, but its [[derived functor]]. This is obtained by evaluating ordinary geometric realization on "sufficiently nice" [[resolution]]s of simplicial topological spaces. These we discuss now.

Recall the following definitions and facts from [[nice simplicial topological space]].

+-- {: .num_defn #GoodAndProper}
###### Definition 

Let $X \colon  \Delta^{op} \to Top$ be a [[simplicial topological space]].

Such $X$ is called

* **good** if all the degeneracy maps $X_{n-1} \hookrightarrow X_n$ are all [[closed cofibrations]];

* **proper** if the inclusion $s X_n \hookrightarrow X_n$ of the degenerate simplices is a [[closed cofibration]], where $s X_n = \bigcup_i s_i(X_{n-1})$.

Noticing that the union of degenerate simplices appearing here is a [[Reedy model structure|latching object]] and that closed cofibrations are cofibrations in the [[Strøm model structure]] on [[Top]], the last condition equivalently says: 

* $X_\bullet$ is **proper** if it is cofibrant in the [[Reedy model structure]] $[\Delta^{op}, Top_{Strom}]_{Reedy}$ on [[simplicial object]]s in [[Top]] with respect to the [[Strøm model structure]] on [[Top]].

=--

The notion of good simplicial topological space goes back to ([Segal73](#Segal73)), that of proper simplicial topological space to ([May](#May)). 

+-- {: .num_prop #GoodImpliesProper}
###### Proposition

A good simplicial topological space is proper:

$$
  (X_\bullet \; good) \Rightarrow (X_\bullet\; proper)
  \,.
$$

=--

A proof appears as ([Lewis, corollary 2.4 (b)](#Lewis)). A generalization of this result to more general topological categories is ([RobertsStevenson, prop. 16](#RobertsStevenson)).

### Bisimplicial sets and good resolutions

We now discuss the [[resolution]] of any simplicial topological space by a good one.
Write 

$$
  ({\vert- \vert} \dashv Sing) 
   \colon  
  Top
    \stackrel{\overset{{|-|}}{\longleftarrow}}{\underset{Sing}{\longrightarrow}} 
  sSet
$$  

for the ordinary [[geometric realization]]/[[singular simplicial complex]] [[adjunction]] (see [[homotopy hypothesis]]).  Recall that the composite ${|Sing(-)|}\colon Top\to Top$ is a cofibrant replacement functor: for any space $X$, the space ${|Sing(X)|}$ is a CW complex and comes with a natural map ${|Sing X|} \to X$ (the [[unit of an adjunction|counit]] of the adjunction $({|-|} \dashv Sing)$) which is a [[weak homotopy equivalence]].

+-- {: .num_prop #GoodResolution}
###### Proposition

Let $X_\bullet$ be a simplicial topological space. 
Then the simplicial topological space 

$$
  {|Sing(X_\bullet)|} \in [\Delta^{op}, Top] \,,
$$ 

obtained by applying ${|Sing(-)|} \colon  Top \to Top$ degreewise, is good and hence proper.  Moreover, we have a natural morphism 
$$
{|Sing X_\bullet|} \to X_\bullet
$$
which is degreewise a weak homotopy equivalence.

=--

+-- {: .proof}
###### Proof

Each space $|Sing X_n|$ is a [[CW-complex]], hence in particular a [[locally equi-connected space]]. By ([Lewis, p. 153](#Lewis)) inclusions of [[retract]]s of locally equi-connected spaces are [[closed cofibration]]s, and since degeneracy maps are retracts, this means that the degeneracy maps in $|Sing X_\bullet|$ are closed cofibrations.

The second sentence follows directly by the remarks above.

=--

Note that there is nothing special about ${|Sing(-)|}$ in the proof; any functorial CW replacement would do just as well (such as that obtained by the [[small object argument]]).  However, ${|Sing(-)|}$ has the advantage that its geometric realization can be computed alternately in terms of diagonals of bisimplicial sets, as we now show.

If $S_{\bullet,\bullet} \colon  \Delta^{op} \times \Delta^{op} \to Set$ is a [[bisimplicial set]], we write $d S$ for its [[diagonal]], which is the composite
$$\Delta^{op} \to \Delta^{op} \times \Delta^{op} \stackrel{S}{\longrightarrow} Set.$$
On the other hand, we can also consider a bisimplicial set as a simplicial object in $sSet$ and take its "geometric realization":
$$ {|S_{\bullet,\bullet}|} \coloneqq \int^{n\in\Delta^{op}} S_{n,\bullet} \times \Delta^n_{sSet} $$
where $\Delta^n_{sSet}$ denotes the $n$-simplex as a simplicial set, i.e. the representable functor $\Delta(-,[n])\colon \Delta^{op}\to Set$.

+-- {: .num_lemma #DiagonalIsRealization}
###### Lemma
For a bisimplicial set $S_{\bullet,\bullet}$, there is a natural isomorphism of simplicial sets $d S \cong {|S|}$.
=--
+-- {: .proof}
###### Proof
Both functors $d$ and ${|-|}$ are [[cocontinuous functor|cocontinuous]] functors between [[presheaf categories]] $Set^{\Delta^{op}\times\Delta^{op}} \to Set^{\Delta^{op}}$, so it suffices to verify that they agree on representables.  The representable $(\Delta\times\Delta)(-,([n],[m]))$ is called a *bisimplex* $\Delta^{n,m}$; its diagonal is
$$(d \Delta^{n,m})(-) = \Delta(-,n) \times \Delta(-,m) = \Delta^n_{sSet} \times \Delta^m_{sSet}.$$
Now note that geometric realization of a bisimplicial set is left adjoint to the "singular complex" $Sing\colon sSet \to sSet^{\Delta^{op}}$ defined by
$$Sing(X_\bullet)(n,m) = \underline{Map}(\Delta^n_{sSet}, X_\bullet)_m = sSet(\Delta^n_{sSet} \times \Delta^m_{sSet}, X_\bullet) = sSet(d \Delta^{n,m}, X_\bullet)$$
where $\underline{Map}(-,-)$ denotes the simplicial mapping space between two simplicial sets.  But by the Yoneda lemma, $Sing(X_\bullet)(n,m) = sSet^{\Delta^{op}}(\Delta^{n,m},Sing(X_\bullet))$, so this shows that $d \Delta^{n,m}$ has the same universal property as ${|\Delta^{n,m}|}$; hence they are isomorphic.
=--

In particular, the lemma implies that for the two different ways of considering a bisimplicial set as a simplicial simplicial set ("vertically" or "horizontally"), the resulting "geometric realizations" as simplicial sets are isomorphic (since both are isomorphic to the diagonal, which is symmetrically defined).

Note that Lemma \ref{DiagonalIsRealization} can be interpreted as an isomorphism between two [[profunctors]] $\Delta &#8696; \Delta\times\Delta$, of which the first is [[representable functor|representable]] by the diagonal functor $\Delta \to \Delta\times\Delta$.  It follows that if $S_{\bullet,\bullet}$ is a bisimplicial object in any [[cocomplete category]], we also have
$$d S_{\bullet,\bullet} \cong \int^{n\in\Delta} S_{n,\bullet}\,\times \,(\Delta^n_{sSet})_{\bullet}$$
where the right-hand side is a "realization" functor from bisimplicial objects to simplicial objects in any cocomplete category.  On the other hand, if $S$ is a bisimplicial *space*, then we also have the *levelwise* realization
$$ \int^{n\in\Delta} S_{n,\bullet} \,\times\, \Delta^n_{Top} $$
which will not, in general, agree with the diagonal and the abstract realization considered above.  It does agree, however, after we pass to a further geometric realization as a single topological space.

+-- {: .num_prop #RealizationOfDiagonalIsRealizationOfRealization}
###### Proposition
For $S_{\bullet,\bullet}$ any bisimplicial space, there is a [[homeomorphism]] between the geometric realizations of the following two simplicial spaces: (1) the diagonal $d S_{\bullet,\bullet}$ of $S$, and (2) the levelwise realization $|S_{\bullet,\bullet}|$ of $S$.
=--
+-- {: .proof}
###### Proof
Applying Lemma \ref{DiagonalIsRealization} as above, we have
$$ d S_{\bullet,\bullet} \cong \int^{n\in \Delta} S_{n,\bullet} \times \Delta^n_{sSet}$$
If we then take the realization of these simplicial spaces, we find
$$
{| d S_{\bullet,\bullet} |}
\cong \left| \int^{n\in\Delta} S_{n,\bullet} \times \Delta^n_{sSet} \right|
\cong \int^{n\in\Delta} {|S_{\bullet,\bullet}|} \times \Delta^n_{Top}
\cong {\vert({\vert S_{\bullet,\bullet} \vert})\vert}
$$
using the fact that geometric realization of simplicial sets preserves colimits and products, and ${|\Delta^n_{sSet}|} = \Delta^n_{Top}$.
=--

This fact is attributed to Tornehave by Quillen on page 94 of his 'Higher Algebraic K-theory I'.

Finally, for any simplicial space $X_\bullet$, we have a bisimplicial set $Sing(X_\bullet)_\bullet$.  Applying the previous proposition to this bisimplicial set, regarded as a discrete bisimplicial space, we find a homeomorphism
$$
  {\vert({\vert Sing(X_\bullet) \vert})\vert}  \cong {| d Sing(X_\bullet)_\bullet |}
  \,.
$$
This also follows from results of ([Lewis](#Lewis)).  Thus, as a resolution of $X_\bullet$, the levelwise realization of the levelwise singular complex ${\vert Sing(X_\bullet) \vert}$ has the pleasant property that its geometric realization, as a simplicial *space*, can be calculated as the realization of a single simplicial *set* (the diagonal of $Sing(X_\bullet)_\bullet$).


## Properties


### General

+-- {: .num_remark}
###### Remark

We have the following degenerate case of geometric realization of simplicial topological spaces.

* If $X_\bullet \colon  \Delta^{op} \to Set \hookrightarrow Top$ is a degreewise [[discrete space]], hence just a [[simplicial set]], the notion of geometric realization above coincides with the notion of [[geometric realization|geometric realization of simplicial sets]].

* If $X_\bullet$ is simplicially constant on a topological space $X_0$, then its geometric realization is [[homeomorphic]] to that space:

  $$
    {\vert X_\bullet \vert} \simeq X_0
    \,.
  $$

  (This is not true for the fat geometric realization, only the ordinary one.  The fat geometric realization will be homotopy equivalent to $X$.)

=--


+-- {: .num_remark}
###### Remark

Geometric realization of simplicial topological spaces has a [[right adjoint|right]] [[adjoint functor]] $\underline{Sing}$:

$$
  ({\vert - \vert} \dashv \underline{Sing})  \colon 
   sTop
   \stackrel{\overset{{\vert - \vert}}{\longrightarrow}}{\underset{\underline{Sing}} {\longleftarrow}}
   Top
  \,,
$$

For $X \in $ [[Top]] a [[topological space]], we have by definition

$$
  \underline{Sing}(X) \colon  [n] \mapsto [\Delta^n_{Top}, X]
  \,,
$$

where on the right we have the [[internal hom]], or [[exponential law for spaces|exponential]], space from the standard topological $n$-simplex to $X$.

=--

+-- {: .num_prop #RealizationOfSingularComplexIsWHE}
###### Proposition

For every $X \in Top$ there is a [[weak homotopy equivalence]]

$$
  {|\underline{Sing}(X)|} \to X
  \,.
$$

=--

{#StricklandSeymour} The proof can be found in [[Neil Strickland]]'s answer to this [mathoverflow question](http://mathoverflow.net/q/171662/381). (An incorrect argument appears as ([Seymour, prop. 3.1](#Seymour)) where it is claimed that $\underline{Sing}(X)$ is proper. In fact, the first degeneracy map $X \to [\Delta^1_{Top}, X]$ is not in general a cofibration as explained in the linked question.)



Ordinary geometric realization has the following two disadvantages:


+-- {: .num_prop #RealizationDoesntPreserveMCofibrancyOrHEs}
###### Proposition

* If $X_\bullet$ has in each degree the [[homotopy type]] of a [[CW-complex]], its realization ${\vert X_\bullet \vert}$ in general need not.

* If a morphism $f \colon  X_\bullet \to Y_\bullet$ is degreewise a [[homotopy equivalence]], its geometric realization ${\vert f \vert}$ need not be a homotopy equivalence.

=--

See ([Segal74, appendix A](#Segal74))

This is different for the fat geometric realization.

+-- {: .num_prop #NicePropertiesOfFatRealization}
###### Proposition

* If $X_\bullet$ is degreewise of the [[homotopy type]] of a [[CW-complex]] (i.e. is degreewise [[m-cofibrant space|m-cofibrant]]), then so is ${\Vert X_\bullet \Vert}$.

* If $f \colon  X_\bullet \to Y_\bullet$ is degreewise a [[homotopy equivalence]], then also ${\Vert f \Vert}$ is a homotopy equivalence.

=--

This appears as ([Segal74, prop. A.1](#Segal)).


### Relation between fat and ordinary geometric realization

+-- {: .num_prop #FatRealizationOfGoodSimplicialSpaces}
###### Proposition

If the simplicial topological space $X_\bullet$ is [good](#GoodAndProper) then the natural morphism from its [fat geometric realization](#FatGeometricRealization) to its [ordinary geometric realization](#GeometricRealization) is a [[homotopy equivalence]]

$$
  {\Vert X_\bullet \Vert} \stackrel{\simeq}{\longrightarrow} {|X_\bullet|}
  \,.
$$

=--

A direct proof of this (not using that good implies proper) appears as ([Segal74, prop. A.1 (iv)](#Segal74)) and a more detailed proof has been given by [[Tammo tom Dieck]]. 

A recent paper treating the special case where $X_\bullet$ is the nerve of a [[topological category]], and each $X_n$ is of the [[homotopy type]] of a [[CW-complex]], is [Wang 2017](#Wang17), [Wang 18](#Wang18).

### Compatibility with limits

We discuss how geometric realization interacts with [[limit]]s of simplicial topological spaces.

#### Ordinary geometric realization

+-- {: .num_prop #RealizationPreservesPullbacks}
###### Proposition

Geometric realization preserves [[pullback]]s: for $X_\bullet \to Y_\bullet \leftarrow Z_\bullet$ a [[diagram]] in $Top^{\Delta^{op}}$ there are [[natural transformation|natural]] [[homeomorphism]]s

$$
  {|X_\bullet|} \,\times_{|Y_\bullet|}\, {|Z_\bullet|}
  \simeq
  {|X_\bullet \,\times_{Y_\bullet}\, Z_\bullet|}
  \,.
$$

=--

This appears for instance as ([May, corollary 11.6](#May)).  See also the proof that geometric realization of simplicial sets preserves pullbacks, at [[geometric realization]].

It is essential here that we are working in a category $Top$ such as compactly generated spaces or k-spaces: in the category of *all* topological spaces this would not be true.  It works in these cases because product and/or quotient topologies in these categories are slightly different from in the category of all topological spaces.


#### Fat geometric realization

The operation of [fat geometric realization](#FatGeometricRealization) does not preserve [[fiber product]]s on the nose, in general, but it does preserve all [[finite limit]]s up to [[homotopy]]. 

Write ${\Vert * \Vert}$ for the fat geometric realization of the point. Notice that due to the identification of $sTop$ with its [[overcategory]] over the point (the simplicial topological space constant on the point), $sTop\simeq sTop/*$, we may regard fat geometric gealization as a functor with values in the [[overcategory]] $Top/{\Vert*\Vert}$ over the 
[fat geometric realization of the point](#GeometricRealizationOfThePoint).

+-- {: .num_prop #FatRealizationPreservesConnectedFiniteLimits}
###### Claim

The functor

$$
  {\Vert - \Vert} \colon  Top^{\Delta^{op}} \to Top/{\Vert*\Vert}
$$

preserves all [[finite limit]]s.

=--

See ([Gepner-Henriques 07, Remark 2.23](#GepnerHenriques07)).


### Relation to the homotopy colimit
  {#RelationToHomotopyColimit}


#### For proper simplicial spaces

Recall that a simplicial topological space is proper if it is Reedy cofibrant relative to the [[Strøm model structure]] on [[Top]], in which the weak equivalences are the honest [[homotopy equivalences]].  Nevertheless, in certain cases geometric realisation computes the [[homotopy colimit]] of the [[diagram]] $X_\bullet \colon  \Delta^{op} \to Top$ given by the simplicial space, with respect to the standard [[Quillen model structure on topological spaces]] in which the weak equivalences are the [[weak homotopy equivalences]].

+-- {: .num_lemma #RealizPresWHE}
###### Lemma
If $X_\bullet \to Y_\bullet$ is an objectwise weak homotopy equivalence between proper simplicial spaces, then the induced map ${|X_\bullet|} \to {|Y_\bullet|}$ is a weak homotopy equivalence.
=--
+-- {: .proof}
###### Proof
The following proof is essentially from ([May74, A.4](#May_Einf)); see also ([Dugger, prop. 17.4, example 18.2](#Dugger)).  It relies on two facts relating [[Hurewicz cofibration]]s to [[weak homotopy equivalence]]s:

1. [[pushout|Pushouts]] along [[Hurewicz cofibration]]s preserve [[weak homotopy equivalence]]s, and

1. [[colimit|Colimits]] of sequences of Hurewicz cofibrations preserve weak homotopy equivalences.

Let $i_n \colon \Delta_{\le n} \hookrightarrow \Delta$ denote the inclusion of the objects $\le n$, and write ${|X_\bullet|}_n = i_n^* \Delta \otimes_{\Delta_{\le n}} i_n^* X_\bullet$.  Writing $L_n X$ for the $n$th [[latching object]] (the subspace of degeneracies in $X_n$), we have pushouts
$$\array{ (L_n X \times \Delta^n) \sqcup_{L_n X \times \partial\Delta^n} (X_n \times \partial\Delta^n) & \to &  {|X_\bullet|}_{n-1}\\
  \downarrow & & \downarrow\\
  X_n \times \Delta^n & \to &  {|X_\bullet|}_n }
$$
Since $X$ is proper, $L_n X \to X_n$ is a cofibration, and of course $\partial\Delta^n \to \Delta^n$ is a cofibration.  Thus, by the [[pushout-product axiom]] for the [[Strøm model structure]], the left-hand vertical map is a cofibration; hence so is the right-hand vertical map.

Now ${|X_\bullet|}$ is the [[colimit]] of the sequence of cofibrations
$$  {|X_\bullet|}_0 \to {|X_\bullet|}_1 \to {|X_\bullet|}_2 \to \cdots$$
and likewise for ${|Y_\bullet|}$.  In other words, the geometric realization is [[filtration|filtered]] by simplicial degree.  Thus, by point (2) above, it suffices to show that each map ${|X_\bullet|}_n \to {|Y_\bullet|}_n$ is a weak homotopy equivalence.

Since ${|X_\bullet|}_0 = X_0$, this is true for $n=0$.  Moreover, by the above pushout square, ${|X_\bullet|}_n$ is a pushout of ${|X_\bullet|}_{n-1}$ along a cofibration.  Thus, by point (1) above, since $X_n \times \Delta^n \to Y_n \times \Delta^n$ is certainly a weak homotopy equivalence, it will suffice for an induction step to prove that
$$(L_n X \times \Delta^n) \sqcup_{L_n X \times \partial\Delta^n} (X_n \times \partial\Delta^n) \to
(L_n Y \times \Delta^n) \sqcup_{L_n Y \times \partial\Delta^n} (Y_n \times \partial\Delta^n)
$$
is a weak homotopy equivalence.  However, by definition we have a pushout
$$ \array{
  L_n X \times \partial\Delta^n & \to & X_n \times \partial\Delta^n \\
  \downarrow & & \downarrow\\
  L_n X \times \Delta^n & \to &
  (L_n X \times \Delta^n) \sqcup_{L_n X \times \partial\Delta^n} (X_n \times \partial\Delta^n) }
$$
This is also a pushout along a Hurewicz cofibration, and cartesian product preserves weak homotopy equivalences, so it will suffice to show that $L_n X \to L_n Y$ is a weak homotopy equivalence.

Recall that $L_n X$ can be written as $\colim^{[n]\to [k]} X_{[k]}$, where the colimit is over all codegeneracy maps $[n]\to [k]$ in $\Delta$ *except* the identity $[n] \to [n]$.  For $0\le m \le n$, write $L^m_n X$ for the corresponding colimit over all codegeneracies which factor through $\sigma_{p}\colon [n]\to [n-1]$ for some $0\le p\le m$.  Then $L^0_n X = X_{n-1}$ and $L^n_n X = L_n X$, and for $0\lt m \le n$ we have a pushout square
$$ \array{ L^{m-1}_{n-1} X & \to & L^{m-1}_n X \\
  \downarrow & & \downarrow \\
  X_{n-1} & \to & L^m_n X. }
$$
We claim that $L^{m-1}_n X \to L^m_n X$ is a cofibration for all $0\le m \le n$, and we prove it by induction on $n$.  For $n=0$ it is obvious.  If it holds for $(n-1)$ (and all $m$ with $0\le m \le n-1$), then by composition and properness of $X$, each map $L^{m-1}_{n-1} X \to X_{n-1}$ is a cofibration.  Hence, by the above pushout square, so is $L^{m-1}_n X \to L^m_n X$.  This proves the claim.

Now, using the above pushout square again and point (1) above, we can prove by induction on $n$, and for fixed $n$, by induction on $m$, that each map $L^m_n X \to L^m_n Y$ is a weak homotopy equivalence.  In particular, taking $m=n$, we find that $L_n X \to L_n Y$ is a weak homotopy equivalence, as desired.
=--

Recall that one way to compute the homotopy colimit of a diagram $X\colon D^{op}\to Top$, with respect to the standard (Quillen) model structure, is as the tensor product
$$hocolim X \coloneqq N(D/ -) \otimes_D Q X,$$
where $(D/ -)\colon D \to Cat$ sends each object of $D$ to its [[overcategory]], $N$ denotes the [[nerve]] of a small category, and $Q$ denotes a functorial cofibrant replacement in the [[Quillen model structure on topological spaces]] (e.g. [[CW complex|CW]] replacement via singular [[nerve and realization]]).  When $D=\Delta$, there is a canonically defined map $N(\Delta / -) \to \Delta$ (where the second $\Delta$ denotes the canonical cosimplicial simplicial set) called the [[Bousfield-Kan map]].  This map induces, for each simplicial space $X$, a map
$$ N(D/ -) \otimes_D X_\bullet \to \Delta \otimes_{\Delta} X_\bullet = {|X_\bullet|} $$
which is also called the **Bousfield-Kan map**.

Since the Str&#248;m model structure is a [[simplicial model category]], standard arguments involving Reedy model structures imply that the Bousfield-Kan map is a Str&#248;m weak equivalence (i.e. a homotopy equivalence) whenever $X$ is Str&#248;m Reedy cofibrant (i.e. proper).  Thus we have:

+-- {: .num_prop #RealizationOfGoodSimplicialSpacesIsHomotopyColimit}
###### Proposition
Let $X_\bullet$ be a proper simplicial space.  Then the composite
$$ \hocolim X_\bullet = N(D/ -) \otimes_D Q X_\bullet \xrightarrow{Bousfield-Kan} {|Q X_\bullet|} \longrightarrow {|X_\bullet|} $$
is a weak homotopy equivalence.
=--
+-- {: .proof}
###### Proof
Since the definition of $\hocolim$ doesn't depend on the choice of an objectwise-cofibrant replacement of $X$, we may as well take $Q$ to be, instead of the composite with a functorial cofibrant replacement in $Top_{Quillen}$, rather a cofibrant replacement in the Reedy model structure on $Top^{\Delta^{op}}$ with respect to the Quillen model structure on $Top$.  (Any Reedy cofibrant diagram is in particular objectwise cofibrant.)  Then $Q X_\bullet$ is Quillen-Reedy cofibrant, hence also proper, and so the Bousfield-Kan map is a homotopy equivalence.  On the other hand, $Q X_\bullet \to X_\bullet$ is a levelwise weak homotopy equivalence, while $Q X_\bullet$ and $X_\bullet$ are proper, so by Lemma \ref{RealizPresWHE} its realization is a weak homotopy equivalence.
=--

By naturality, the above composite is also equal to the composite
$$ \hocolim X_\bullet = N(D/ -) \otimes_D Q X_\bullet \to N(D/ -) \otimes_D X_\bullet \xrightarrow{Bousfield-Kan} {|X_\bullet|}; $$
hence this composite is also a weak homotopy equivalence.

\linebreak

#### For degreewise cofibrant simplicial spaces
 {#RelationToHomotopyColimitForDegreewiseCofibrationSimplicialSpaces}

+-- {: .num_prop}
###### Proposition

Let $X_\bullet$ be a [[simplicial topological space]] which is degreewise a [[cofibrant object]] in the [[classical model structure on topological spaces]], hence which is degreewise a [[retract]] of a [[cell complex]] (for instance: degreewise a [[CW-complex]]). 

Then its [[fat geometric realization]] models the [[homotopy colimit]] over $X_\bullet \;\colon\; \Delta^{op} \longrightarrow Top_{Quillen}$ in the [[classical model structure on topological spaces]]:

$$
  \left\Vert X_\bullet \right\Vert
  \;\simeq_{whe}\;
  hocolim X_\bullet
  \,.
$$

=--

This is claimed in [Wang 18, Theorem 4.3, Remark 4.4](#Wang18).


## Examples and Applications


### Topological principal $\infty$-bundles
 {#TopologicalPrincipalInfinityBundle}

We discuss aspects of [[principal ∞-bundle]]s equipped with topological [[cohesive (∞,1)-topos|cohesion]] and their geometric realization to [[principal bundle]]s in [[Top]].
 
For $X,Y \in sTop$, write

$$
  sTop(X,Y) \coloneqq \int_{[k] \in \Delta} [X_k, Y_k] \;\; \in Top
$$

for the [[Top]]-[[hom-object]], where in the integrand of the [[end]] $[-,-] \colon  Top^{op} \times Top^{op} \to Top$ is the [[internal hom]] of topological spaces.


+-- {: .num_defn #GloballyKanSimplicialTopologicalSpace}
###### Definition

We say a morphism $f \colon  X \to Y$ of [[simplicial topological space]]s is a **global Kan fibration** if for all $n \in \mathbb{N}$ and $0 \leq i \leq n$ the canonical morphism

$$
  X_n \to Y_n \;\times_{sTop(\Lambda[n]_i, Y)}\; sTop(\Lambda[n]_i, X)
$$

in [[Top]] has a [[section]], where  $\Lambda[n]_i \in $ [[sSet]] $\hookrightarrow Top^{\Delta^{op}}$ is the $i$th $n$-[[horn]] regarded as a [[discrete space|discrete]] [[simplicial topological space]].

We say a [[simplicial topological space]] $X_\bullet \in Top^{\Delta^{op}}$ is **(global) Kan simplicial space** if the unique morphism $X_\bullet \to *$ is a global Kan fibration, hence if for all $n \in \mathbb{N}$ and all $0 \leq i \leq n$ the canonical [[continuous function]]

$$
  X_n \to sTop(\Lambda[n]_i, X)
$$

into the [[topological space]] of $i$th $n$-[[horn]]s admits a [[section]] (in [[Top]], hence a global, continuous section).

=--

+-- {: .num_remark}
###### Remark

This global notion of topological Kan fibration is considered in ([BrownSzczarba, def. 2.1, def. 6.1](#BrownSzczarba)). In fact there a stronger condition is imposed: a [[Kan complex]] in [[Set]] automatically has the lifting property not only against all full [[horn]] inclusions but also against sub-horns; and in ([BrownSzczarba](#BrownSzczarba)) all these fillers are required to be given by global sections. This ensures that with $X$ globally Kan also the [[internal hom]] $[Y,X] \in sTop$ is globally Kan, for any simplicial topological space $Y$. This is more than we need and want to impose here. For our purposes it is sufficient to observe that if $f$ is globally Kan in the sense of ([BrownSzczarba, def. 6.1](#BrownSzczarba)), then it is so also in the [above sense](#GloballyKanSimplicialTopologicalSpace).

=--


Recall from the discussion at [[universal principal ∞-bundle]] that for $G$ a [[simplicial topological group]] the [[universal simplicial principal bundle]] $\mathbf{E}G \to \mathbf{B}G$ is presented by the morphism of [[simplicial topological space]]s traditionally denoted $W G \to \bar W G$. 

+-- {: .num_prop #SimplicialTopologicalUniversalBundle}
###### Proposition

Let $G$ be a [[simplicial topological group]]. Then 

1. $G$ is a globally Kan simplicial topological space;

1. $\bar W G$ is a globally Kan simplicial topological space;

1. $W G \to \bar W G$ is a global Kan fibration.

=--

+-- {: .proof}
###### Proof

The first statement appears as ([BrownSzczarba, theorem 3.8](#BrownSzczarba)), the second is noted in ([RobertsStevenson](#RobertsStevenson)), the third appears as ([BrownSzczarba, lemma 6.7](#BrownSzczarba)).

=--

+-- {: .num_prop #BarWGIsGoodIfGIsWellSectioned}
###### Proposition

If $G$ is a [[well-pointed simplicial topological group]] then both $W G$ and $\bar W G$ are [good simplicial topological space](#GoodAndProper).

=--

For $\bar W G$  this is ([RobertsStevenson, prop. 19](#RobertsStevenson)). For $W G$ this follows with ([RobertsStevenson, lemma 10, lemma 11](#RobertsStevenson)) which says that $W G = Dec_0 \bar W G$ and the observations in the proof of ([RobertsStevenson, prop. 16](#RobertsStevenson)) that $Dec_0 X$ is good if $X$ is.

+-- {: .num_prop #RealizationSimplicialTopologicalUniversalBundle}
###### Proposition

For $G$ a [[well-pointed simplicial topological group]], the geometric realization of the [[universal simplicial principal bundle]] $W G \to \bar W G$

$$
  {\vert W G \vert} \to {\vert \bar W G \vert}
$$

is a fibration [[resolution]] in $Top_{Quillen}$ of the point inclusion 
$* \to B{|G|}$ into the [[classifying space]] of the geometric realization of $G$.

=--

This is ([RobertsStevenson, prop. 14](#RobertsStevenson)).

+-- {: .num_prop #SimplicialTopolgicalBundleIsGood}
###### Proposition

Let $X_\bullet$ be a [good](#GoodAndProper) [[simplicial topological space]] and $G$ a [[well-pointed simplicial topological group]]. Then for every morphism

$$
  \tau \colon  X \to \bar W G
$$

the corresponding topological [[simplicial principal bundle]] $P$ over $X$ is itself a good simplicial topological space.

=--

+-- {: .proof}
###### Proof

The bundle is the [[pullback]] $P = X \times_{\bar W G} W G$ in $sTop$

$$
  \array{
     P &\to& \bar W G
     \\
     \downarrow && \downarrow
     \\
     X &\stackrel{\tau}{\to}& \bar W G
  }
  \,.
$$

By assumption on $X$ and $G$ and using prop. \ref{BarWGIsGoodIfGIsWellSectioned} we have that $X$, $\bar W G$ and $W G$ are all good simplicial spaces.

This means that the degeneracy maps of $P_\bullet$ are induced degreewise by morphisms between pullbacks in [[Top]] that are degreewise [[closed cofibration]]s, where one of the morphisms in each pullback is a fibration. By the properties discussed at [[closed cofibration]], this implies that also these degeneracy maps of $P_\bullet$ are closed cofibrations.

=--

Let for the following $Top_s \hookrightarrow Top$ be any [[small category|small]] [[full subcategory]]. 


+-- {: .num_defn #SimpTopAsSimpPresheaves}
###### Definition

Under the degreewise [[Yoneda embedding]] $sTop_s \hookrightarrow [Top_s^{op}, sSet]$ simplicial topological spaces embed into the category of [[simplicial presheaves]] on $Top_s$.

We equip this with the projective [[model structure on simplicial presheaves]] $[Top_s^{op}, sSet]_{proj}$, and we speak of [[homotopy limit]]s in $sTop$ under this embedding.

=--

+-- {: .num_prop #GlobalKanFibImpliesProjectiveFib}
###### Proposition

Under this embedding a [global Kan fibration](#GloballyKanSimplicialTopologicalSpace) $f \colon  X \to Y$ in $sTop_s$ maps to a fibration in $[Top_s^{op}, sSet]_{proj}$.

=--

+-- {: .proof}
###### Proof

By definition, a morphism $f \colon  X \to Y$ in $[Top_s^{op}, sSet]_{proj}$ is a fibration if for all $U \in Top$ and all $n \in \mathbb{N}$ and $0 \leq i \leq n$ diagrams of the form

$$
  \array{
    \Lambda[n]_i \cdot U &\to& X
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    \Delta[n] \cdot U &\to& Y
  }
$$

have a lift. This is equivalent to saying that the [[function]]

$$
  Hom(\Delta[n]\cdot U, X)
   \to 
  Hom(\Delta[n]\cdot U,Y) 
    \times_{Hom(\Lambda[n]_i \cdot U, Y)}
  Hom(\Lambda[n]_i \cdot U, X)
$$

is surjective. Notice that we have

$$
  \begin{aligned}
    Hom_{[Top_s^{op}, sSet]}(\Delta[n]\cdot U, X)
    & = 
    Hom_{sTop}(\Delta[n]\cdot U, X)
    \\
     & = \int_{[k] \in \Delta} Hom_{Top}( \Delta[n]_k \times U, X_k)
   \\
    & = \int_{[k] \in \Delta} Hom_{Top}(U, [\Delta[n]_k, X_k])
   \\
    & = Hom_{Top}(U, \int_{[k] \in \Delta} [\Delta[n]_k, X_k])
   \\
    & = Hom_{Top}(U, sTop(\Delta[n], X))
   \\
    & = Hom_{Top}(U, X_n)
  \end{aligned}
$$

and analogously for the other factors in the above morphism. Therefore the lifting problem equivalently says that the function

$$
  Hom_{Top}(U, \; X_n \to Y_n \times_{sTop(\Lambda[n]_i, Y)} sTop(\Lambda[n]_i,X) \;)
$$

is surjective. But by the assumption that $f \colon  X \to Y$ is a global Kan fibration of simplicial topological spaces, def. \ref{GloballyKanSimplicialTopologicalSpace}, we have a section $\sigma \colon  Y_n \times_{sTop(\Lambda[n]_i), Y} sTop(\Lambda[n]_i,X) \to X_n$. Therefore $Hom_{Top}(U, \sigma)$ is a section of our function.

=--


+-- {: .num_prop #HocolimPreservesHomotopyFibers}
###### Proposition

The [[homotopy colimit]] operation

$$
  sTop \hookrightarrow [Top_s^{op}, sSet]_{proj} \stackrel{hocolim}{\to} Top_{Quillen}
$$

preserves [[homotopy fiber]]s of morphisms $\tau \colon  X \to \bar W G$ with $X$ good and globally Kan and $G$ well-pointed.

=--


+-- {: .proof}
###### Proof

By prop. \ref{SimplicialTopologicalUniversalBundle} 
and prop. \ref{GlobalKanFibImpliesProjectiveFib} we have that $W G \to \bar W G$ is a fibration [[resolution]] of the point inclusion $* \to \bar W G$ in $[Top^{op}, sSet]_{proj}$.
By the general discussion at [[homotopy limit]] this means that the [[homotopy fiber]] of a morphism $\tau \colon  X \to \bar W G$ is computed as the ordinary [[pullback]] $P$ in 

$$
  \array{
    P &\to& W G
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{\tau}{\to}& \bar W G
  }
$$

(since all objects $X$,  $\bar W G$ and $W G$ are fibrant and at least one of the two morphisms in the pullback diagram is a fibration) and hence

$$
  hofib(\tau) \simeq P
  \,.
$$

By prop. \ref{SimplicialTopologicalUniversalBundle} and prop. \ref{SimplicialTopolgicalBundleIsGood} it follows that all objects here 
are good simplicial topological spaces. Therefore by prop. \ref{RealizationOfGoodSimplicialSpacesIsHomotopyColimit} we have

$$
  hocolim P_\bullet \simeq {|P_\bullet|}
$$

in [[Ho(Top)]]. By prop. \ref{RealizationPreservesPullbacks} we have that 

$$
  \cdots = {|X_\bullet|} \times_{|\bar W G|} {|W G|}
  \,.
$$

But prop. \ref{RealizationSimplicialTopologicalUniversalBundle} says that this is again the presentation of a homotopy pullback/homotopy fiber by an ordinary pullback

$$
  \array{
    {|P|} &\to& {|W G|}
    \\
    \downarrow && \downarrow
    \\
    {|X|} &\stackrel{\tau}{\to}& {|\bar W G|}
  }
  \,,
$$

because $|W G| \to |\bar W G|$ is again a fibration resolution of the point inclusion. Therefore


$$
  hocolim P_\bullet \simeq hofib( {|\tau|} )
  \,.
$$

Finally by prop. \ref{RealizationOfGoodSimplicialSpacesIsHomotopyColimit} and using the assumption that $X$ and $\bar W G$ are both good, this is

$$
  \cdots \simeq hofib (hocolim \tau)
  \,.
$$

In total we have shown

$$
  hocolim (hofib \tau) \simeq hofib (hocolim \tau)
  \,.
$$

=--



### Classifying spaces
  {#ClassifyingSpaces}
For $G$ a [[topological group]], write $\mathbf{B}G$ for its [[delooping]] [[topological groupoid]]: the topological groupoid with a single object and $Mor_{\mathbf{B}G}(*,*) \coloneqq  G$, with composition given by the product on $G$.

The [[nerve]] $N \mathbf{B}G$ of this topological groupoid is naturally a [[simplicial topological space]], with

$$
  N \mathbf{B}G \colon  [n] \mapsto G^{\times_n}
  \,.
$$

+-- {: .num_prop #ClassifyingSpaceByGeometricRealization}
###### Proposition

The geometric realization of $N \mathbf{B}G$ is a model for the [[classifying space]] $B G$ of $G$-[[principal bundle]]s

$$
  {|N \mathbf{B}G|} \simeq B G
  \,.
$$

=--

An early reference for this classical fact is ([Segal68](#Segal68)).


+-- {: .num_cor #OmegaBGisaWHE}
###### Corollary

Let $G$ be a [[well-pointed simplicial topological group|well-pointed]] [[topological group]], $B G$ its [[classifying space]] and $\Omega B G$ the [[loop space]] of the classifying space. 

There is a [[weak homotopy equivalence]]

$$
  \Omega B G \stackrel{\simeq}{\to} G
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{ClassifyingSpaceByGeometricRealization} we have
that $B G \simeq |\mathbf{B}G|$ (we suppress the [[nerve]] operation notationally, which injects [[groupoid]]s into [[∞-groupoid]]s).

By standard facts about the $\bar W$-functor (see [[simplicial principal bundle]]) we have a [[pullback]] square of [[simplicial topological space]]s

$$
  \array{
    G &\to& W G
    \\
    \downarrow && \downarrow
    \\
    * &\to& \bar W G
  }
$$

exhibiting the [[homotopy pullback]]

$$
  \array{
    G &\to& *
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    * &\to& \mathbf{B}G
  }
  \,.
$$

Under geoemtric realization this maps to 

$$
  \array{
    G &\to& *
    \\
    \downarrow &\swArrow_{\simeq}& \downarrow
    \\
    * &\to& B G
  }
$$

in [[Top]]. By prop \ref{HocolimPreservesHomotopyFibers} this is still a homotopy pullback, and hence exhibits $G$ as the [[loop space]] of $B G$.

=--




### Cech nerves
 {#CechNerves}

+-- {: .num_prop #RealizationOfCechNerveIsWHE}
###### Proposition

Let $X,Y$ be  [[topological space]]s and $\pi \colon  Y \to X$ a [[continuous function]] that admits local [[section]]s. Write $C(\pi) \in sTop$ for the [[Cech nerve]].

Then the canonical map

$$
  {|C(\pi)|} \to X
$$

from the geometric realization of $X$ back to $X$ is a [[weak homotopy equivalence]]. If $X$ is a [[paracompact topological space]] then it is even a [[homotopy equivalence]].


=--

For paracompact $X$ this goes back to ([Segal68](#Segal68)). The general case is discussed in ([DuggerIsaksen](#DuggerIsaksen)). A generalization to parameterized spaces is in ([RobertsStevenson, lemma 22](#RobertsStevenson)).




## Related concepts

* [[simplicial topological space]], [[nice simplicial topological space]]

* [[simplicial topological group]]

* [[geometric realization]]

  * [[geometric realization of categories|of categories]], **of simplicial topological spaces**, [[geometric realization of cohesive ∞-groupoids|of cohesive ∞-groupoids]]



## References

### General

The first occurence of the definition of geometric realization of simplicial topological spaces seems to be

* {#Segal68} [[Graeme Segal]],  _Classifying spaces and spectral sequences_ Publications Math&#233;matiques de l'IH&#201;S, 34 (1968), p. 105-112  ([numdam](http://www.numdam.org/item?id=PMIHES_1968__34__105_0))

but the construction was implicit in earlier discussion of [[classifying space]]s. The observation that this is a [[coend]] was noted in

* {#MacLane} [[Saunders MacLane]], _The Milgram bar construction as a tensor product of functors_ SLNM Vol. 168 (1970)


The definition of _good_ simplicial topological spaces goes back to

* {#Segal73} [[Graeme Segal]], _Configuration-Spaces and Iterated Loop-Spaces_ , Inventiones math. 21,213-221 (1973)


An original reference on geometric realization of simplicial topological spaces is is appendix A of

* {#Segal74} [[Graeme Segal]], _[[SegalCategoriesAndCohomologyTheories.pdf:file]]_, Topology, 13:293&#8211;312, 1974 (<a href="https://doi.org/10.1016/0040-9383(74)90022-6">10.1016/0040-9383(74)90022-6</a>)


A proof that ordinary and fat geometric realisation give homotopic spaces, for the special case of the nerve of a topological category is in

* {#Wang17} Yi-Sheng Wang, _Fat realization and Segal's classifying space_ ([arXiv:1710.03796](https://arxiv.org/abs/1710.03796))

* {#Wang18} Yi-Sheng Wang, _Geometric realization and its variants_ ([arXiv:1804.00345](https://arxiv.org/abs/1804.00345))

A standard textbook reference is chapter 11 of

* {#May} [[Peter May]], _The geometry of iterated loop spaces_ ([pdf]())


A proof that good simplicial spaces are proper is implicit in the proof of lemma A.5 in ([Segal74](#Segal74)). Explicitly it appears in

* {#Lewis} L. Gaunce Lewis Jr., _When is the natural map $X\to \Omega \Sigma X$ a cofibration?_ , Trans. Amer. Math. Soc. **273** (1982) no. 1, 147--155 ([JSTOR](.org/pss/1999197))


A generalization of the statement that good implies proper to other [[topological concrete categories]] and a discussion of the geometric realization of $W G \to \bar W G$ for $G$ a [[simplicial topological group]] is in 

* {#RobertsStevenson} [[David Roberts]], [[Danny Stevenson]], _Simplicial principal bundle in parameterized spaces_ ([arXiv:1203.2460](http://arxiv.org/abs/1203.2460))
 

* {#Stevenson} [[Danny Stevenson]], _Classifying theory for simplicial parametrized groups_ ([arXiv:1203.2461](http://arxiv.org/abs/1203.2461))
 

Comments on the relation between properness and cofibrancy in the [[Reedy model structure]] on $[\Delta^{op}, Set]$ are made in 

* [[Paul Goerss]], [[Kristen Schemmerhorn]], _Model Categories and Simplicial Methods_ ([pdf](http://www.math.northwestern.edu/~pgoerss/papers/ucnotes.pdf)).

The relation between (fat) geometric realization and [[homotopy colimit]]s is considered as prop. 17.5 and example 18.2 of

* {#Dugger} [[Daniel Dugger]], _A primer on homotopy colimits_ ([pdf](http://pages.uoregon.edu/ddugger/hocolim.pdf))


The proof that geometric realization of proper simplicial spaces preserves weak equivalences is from

* {#May_Einf} [[Peter May]], *$E_\infty$-spaces, group completions, and permutative categories*.  London Math. Soc. Lecture Notes No. 11, 1974, 61-93.


A definition of the Bousfield-Kan map, and the Reedy model category theory necessary to show that it is a weak equivalence, can be found in

* Hirschhorn, *Model categories and their localizations*, AMS Mathematical Surveys and Monographs No. 99, 2003

On the (fat) geometric realization of ([[nerves]] of) [[topological groupoids]]:

* {#GepnerHenriques07} [[David Gepner]], [[André Henriques]], Section 2.3 in: _Homotopy theory of orbispaces_ ([arXiv:math/0701916](https://arxiv.org/abs/math/0701916))

See also

* [[David Carchedi]], section 3.2 of _On The Homotopy Type of Higher Orbifolds and Haefliger Classifying Spaces_ ([arXiv:1504.02394](http://arxiv.org/abs/1504.02394))


On globally Kan simplicial spaces:

* {#BrownSzczarba} E. H. Brown and R. H. Szczarba, _Continuous cohomology and real homotopy type_ , Trans. Amer. Math. Soc. 311 (1989), no. 1, 57 ([pdf](http://www.ams.org/journals/tran/1989-311-01/S0002-9947-1989-0929667-6/S0002-9947-1989-0929667-6.pdf))


On the [[right adjoint]] to geometric realization of simplicial topological spaces 

* {#Seymour} R. M. Seymour, _Kan fibrations in the category of simplicial spaces_ Fund. Math., 106(2):141-152, 1980. 

On geometric relatization of [[semi-simplicial topological spaces]]:

* [[Johannes Ebert]], [[Oscar Randal-Williams]], *Semi-simplicial spaces*, Algebr. Geom. Topol. 19 (2019) 2099-2150 ([arXiv:1705.03774](https://arxiv.org/abs/1705.03774))


On Geometric realization of general [[Cech nerves]]:

* {#DuggerIsaksen} [[Dan Dugger]], D. C. Isaksen, _Topological hypercovers and $\mathbb{A}^1$- realizations, Math. Z. 246 (2004) no. 4 

### (Non-)Compatibility with homotopy pullbacks
 {#ReferencesCompatibilityHomotopyPullback}

Discussion of sufficient conditions for geometric realization to be compatible with [[homotopy pullbacks]]:

* D. Anderson, _Fibrations and geometric realization_ , 
Bull. Amer. Math. Soc. Volume 84, Number 5 (1978), 765-788. ([euclid:1183541139](http://projecteuclid.org/euclid.bams/1183541139))

* {#Rezk14} [[Charles Rezk]], _When are homotopy colimits compatible with homotopy base change?_, 2014 ([pdf](https://faculty.math.illinois.edu/~rezk/i-hate-the-pi-star-kan-condition.pdf), [[RezkHomotopyColimitsBaseChange.pdf:file]])

* Edoardo Lanari, _Compatibility of homotopy colimits and homotopy pullbacks of simplicial presheaves_ ([pdf](http://algant.eu/documents/theses/lanari.pdf), [[LanariHomotopyColimitsBaseChange.pdf:file]])

  (expanded version of [Rezk 14](#Rezk14))


[[!redirects geometric realization of a simplicial space]]
[[!redirects geometric realization of a simplicial topological space]]
[[!redirects geometric realization of simplicial spaces]]
[[!redirects fat geometric realization of simplicial spaces]]
[[!redirects fat geometric realization of simplicial topological spaces]]
[[!redirects fat geometric realization of a simplicial space]]
[[!redirects fat geometric realization of a simplicial topological space]]
[[!redirects fat geometric realization]]
[[!redirects fat realization]]