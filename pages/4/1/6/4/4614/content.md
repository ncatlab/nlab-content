
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

## Definition

Let [[Top]] in the following denote either

* the [[category]] of [[compactly generated space|compactly generated]] [[weakly Hausdorff space]]s, or

* the category of [[k-space]]s.

Let $\Delta$ denote the [[simplex category]], and write $\Delta_{Top} \colon \Delta \to Top \colon  [n] \mapsto \Delta^n_{Top}$ for the standard [[cosimplicial object|cosimplicial]] [[topological space]] of topological [[simplices]].

Write equivalently

$$
  Top^{\Delta^{op}} \coloneqq  sSet \coloneqq  [\Delta^{op}, Top]
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

One also considers geometric realization after restricting to the subcategory $\Delta_+ \hookrightarrow \Delta$ of the [[simplex category]] on the strictly increasing maps (that is, the coface maps only---no codegeneracies).

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

where the [[equivalence relation]] "$\sim_+$" identifies $(x,f_* p) \in X_l\times \Delta^l_{Top}$ with $(p,f^* x) \in X_k\times \Delta^k_{Top}$ only when $[k] \to [l]$ is a coface map.

+-- {: .num_example #GeometricRealizationOfThePoint}
###### Example

The geometric realization of the point --- the [[simplicial topological space]] that is in each degree the 1-point topological space --- is [[homeomorphic]] to the point, but the fat geometric realization of the point is an "infinite dimensional topological ball": the [[terminal object|terminal]] morphism

$$
  {\vert * \vert} \stackrel{\simeq_{iso}}{\to} *
$$

is an [[isomorphism]], but the morphism

$$
  {\Vert * \Vert} \stackrel{\simeq_{h.e.}}{\to} *
$$

is just a [[homotopy equivalence]].

=--

## Reminder on nice simplicial topological spaces

Simplicial topological spaces are in [[homotopy theory]] presentations for certain [[topological ∞-groupoid]]s . In this context what matters is not the operation of geometric realization itself, but its [[derived functor]]. This is obtained by evaluating ordinary geometric realization on "sufficiently nice" [[resolution]]s of simplicial topological spaces. These we discuss now.

Recall the following definitions and facts from [[nice simplicial topological space]].

+-- {: .num_defn #GoodAndProper}
###### Definition 

Let $X \colon  \Delta^{op} \to Top$ be a [[simplicial topological space]].

Such $X$ is called

* **good** if all the degeneracy maps $X_{n-1} \hookrightarrow X_n$ are all [[closed cofibration]]s;

* **proper** if the inclusion $s X_n \hookrightarrow X_n$ of the degenerate simplices is a [[closed cofibration]], where $s X_n = \bigcup_i s_i(X_{n-1})$.

Noticing hat the union of degenerate simplices appearing here is a [[Reedy model structure|latching object]] and that closed cofibrations are cofibrations in the [[Strøm model structure]] on [[Top]], the last condition equivalently says: 

* $X_\bullet$ is **proper** if it is cofibrant in the [[Reedy model structure]] $[\Delta^{op}, Top_{Strom}]_{Reedy}$ on [[simplicial object]]s in [[Top]] with respect to the [[Strøm model structure]] on [[Top]].

=--

The notion of good simplicial topological space goes back to ([Segal73](#Segal73)), that of proper simplicial topological space to ([May](#May)). 

+-- {: .num_prop #RelationToDiagonalOfBisimplicialSets}
###### Proposition

A good simplicial topological space is proper:

$$
  (X_\bullet \; good) \Rightarrow (X_\bullet\; proper)
  \,.
$$

=--

A proof appears as ([Lewis, corollary 2.4 (b)](#Lewis)). A generalization of this result is in ([RobertsStevenson](#RobertsStevenson)).

We now discuss the [[resolution]] of any simplicial topological space by a good one.

Write 

$$
  ({\vert- \vert} \dashv Sing) 
   \colon  
  Top
    \stackrel{\overset{{|-|}}{\leftarrow}}{\underset{Sing}{\to}} 
  sSet
$$  

for the ordinary [[geometric realization]]/[[singular simplicial complex]] [[adjunction]] (see [[homotopy hypothesis]]).

For $S_{\bullet,\bullet} \colon  \Delta^{op} \times \Delta^{op} \to Set$ a [[bisimplicial set]], write $d S$ for its [[diagonal]] $d X \colon  \Delta^{op} \to \Delta^{op} \times \Delta^{op} \stackrel{S}{\to} Set$.

+-- {: .num_prop #GoodResolution}
###### Proposition

Let $X_\bullet$ be a simplicial topological space. 
Then the simplicial topological space 

$$
  {|Sing(X_\bullet)|} \in [\Delta^{op}, Top]
$$ 

obtained by applying degreewise ${|Sing(-)|} \colon  Top \to Top$ is good and hence proper. 

=--

+-- {: .proof}
###### Proof

Each space $|Sing X_n|$ is a [[CW-complex]], hence in particular a [[locally equi-connected space]]. By ([Lewis, p. 153](#Lewis)) inclusions of [[retract]]s of locally equi-connected spaces are [[closed cofibration]]s, and since degeneracy maps are retracts, this means that the degeneracy maps in $|Sing X_\bullet|$ are closed cofibrations.

=--

+-- {: .num_remark}
###### Remark


There is a natural morphism

$$
  {|Sing X_\bullet|} \to X_\bullet
$$

that is degreewise a [[weak homotopy equivalence]]: the degreewise 
[[unit of an adjunction|counit]] of the adjunction $({|-|} \dashv Sing)$.

=--


+-- {: .num_prop #HomeomorphismFromResolutionToDiagonal}
###### Proposition

For $X_\bullet$ any [[simplicial topological space]], there is a [[homeomorphism]] between the geometric realization of the simplicial space $|Sing(X_\bullet)|$ and the ordinary [[geometric realization]] of the [[simplicial set]] that is the diagonal of the [[bisimplicial set]] $Sing(X_\bullet)_\bullet$

$$
  {\vert({\vert Sing(X_\bullet) \vert})\vert}  \simeq_{iso} {| d Sing(X_\bullet)_\bullet |}
  \,.
$$

=--

This follows by results in ([Lewis](#Lewis)).  In fact, this is true for any bisimplicial set: the realization of its levelwise realization is the same as the realization of its diagonal.




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
   \stackrel{\overset{{\vert - \vert}}{\to}}{\underset{\underline{Sing}} {\leftarrow}}
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

+-- {: .num_prop}
###### Proposition

For every $X \in Top$ there is a [[weak homotopy equivalence]]

$$
  {|\underline{Sing}(X)|} \to X
  \,.
$$

=--

This appears as ([Seymour, prop. 3.1](#Seymour)).



Ordinary geometric realization has the following two disadvantages:


+-- {: .num_prop}
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
  {\Vert X_\bullet \Vert} \stackrel{\simeq}{\to} {|X_\bullet|}
  \,.
$$

=--

A direct proof of this (not using that good implies proper) appears as ([Segal74, prop. A.1 (iv)](#Segal74)) and a more detailed proof has been given by Tammo tom Dieck.

### Compatibility with limits

We discuss how geometric realization interacts with [[limit]]s of simplicial topological spaces.

#### Ordinary geometric realization

+-- {: .num_prop #RealizationPreservesPullbacks}
###### Proposition

Geometric realization preserves [[pullback]]s: for $X_\bullet \to Y_\bullet \leftarrow Z_\bullet$ a [[diagram]] in $Top^{\Delta^{op}}$ there are [[natural transformation|natural]] [[homeomorphism]]s

$$
  {|X_\bullet|} \times_{|Y_\bullet|} |Z_\bullet|
  \simeq
  |X_\bullet \times_{Y_\bullet} Z_\bullet|
  \,.
$$

=--

This appears for instance as ([May, corollary 11.6](#May)).  See also the proof that geometric realization of simplicial sets preserves pullbacks, at [[geometric realization]].

It is essential here that we are working in a category $Top$ such as compactly generated spaces or k-spaces: in the category of *all* topological spaces this would not be true.  It works in these cases because product and/or quotient topologies in these categories are slightly different from in the category of all topological spaces.


#### Fat geometric realization

The operation of [fat geometric realization](#FatGeometricRealization) does not preserve [[fiber product]]s on the nose, in general, but it does preserve all [[finite limit]]s up to [[homotopy]]. 

Write ${\Vert * \Vert}$ for the fat geometric realization of the point. Notice that due to the identification of $sTop$ with its [[overcategory]] over the point (the simplicial topological space constant on the point), $sTop\simeq sTop/*$, we may regard fat geometric gealization as a functor with values in the [[overcategory]] $Top/{\Vert*\Vert}$ over the 
[fat geometric realization of the point](#GeometricRealizationOfThePoint).

+-- {: .num_prop}
###### Proposition

The functor

$$
  {\Vert - \Vert} \colon  Top^{\Delta^{op}} \to Top/{\Vert*\Vert}
$$

preserves all [[finite limit]]s.

=--

See ([GepnerHenriques, remark 2.23](#GepnerHenriques)).


### Relation to the homotopy colimit
  {#RelationToHomotopyColimit}

In certain cases geometric realisation computes the [[homotopy colimit]] of the [[diagram]] $X_\bullet \colon  \Delta^{op} \to Top$ given by the simplicial space, with respect to the standard [[model structure on topological spaces]].


+-- {: .num_prop #RealizationOfGoodSimplicialSpacesIsHomotopyColimit}
###### Proposition

Let $X_\bullet$ be a [good](#GoodAndProper) [[simplicial topological space]] that is degreewise a [[CW-complex]]. 

Then in the [[homotopy category]] [[Ho(Top)]] there is an [[isomorphism]] between its geometric realization and the [[homotopy colimit]] over the simplicial [[diagram]] $X_\bullet \colon  \Delta^{op} \to Top_{Quillen}$ with respect to the standard [[model structure on topological spaces]].

$$
  \vert X_\bullet \vert 
  \simeq
  hocolim_n X_n
  \,.
$$

=--

+-- {: .proof}
###### Proof

We have the following zig-zag of [[homotopy equivalence]]s in [[Top]]

$$
  \array{
    \Vert X_\bullet \Vert &\stackrel{\simeq}{\leftarrow}& 
      \Vert (\vert Sing(X_\bullet)\vert) \Vert
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow^{\mathrlap{\simeq}}
    \\
    \vert X_\bullet \vert && 
      \vert (\vert Sing(X_\bullet) \vert) \vert
    &=_{iso}&
    \vert  d (Sing X_\bullet)_\bullet \vert 
    &\simeq&
    \vert  hocolim_n (Sing X_n )\vert
  }
  \,.
$$

The two vertical equivalences follows from prop. \ref{FatRealizationOfGoodSimplicialSpaces} by the assumption that $X_\bullet$ is good and the statement of prop. \ref{GoodResolution} that also $\vert Sing X_\bullet \vert$ is good. The top horizontal equivalence is due to prop. \ref{NicePropertiesOfFatRealization} and the fact that the $(\vert-\vert \dashv Sing)$-[[unit of an adjunction|counit]] is a [[weak homotopy equivalence]] in general and hence a [[homotopy equivalence]] on CW-complexes.
The homeomorphism on the right is that of prop. \ref{HomeomorphismFromResolutionToDiagonal}. Finally the rightmost equivalence uses that the [[diagonal]] of a bisimplicial set $S_{\bullet, \bullet}$ computes the [[homotopy colimit]] of $[n] \mapsto S_{\bullet, n}$ by 

1. the fact that the diagonal is isomorphic to the coend (see [[bisimplicial set]])

   $$
     d S = \int^{[n] \in \Delta} \Delta[n] \times S_{\bullet,n}
     \,,
   $$

1. this coend is a [[Quillen bifunctor]] (see there)

   $$
     \int^\Delta (-)\times (-) \colon  
      [\Delta, sSet_{Quillen}]_{Reedy} \times 
      [\Delta^{op}, sSet_{Quillen}]_{Reedy}
      \to
      sSet_{Quillen}
      \,,
   $$

1. the standard cosimplicial simplex $\Delta \colon  \Delta \to sSet$ is a cofibrant [[resolution]] of the point in the [[Reedy model structure]] (see there) and every simplicial simplicial set is Reedy cofibrant;

1. the general discussion of presentations of [[homotopy colimit]]s (see there) by such resolved [[coend]]s.

Finally since $\vert - \vert \colon  sSet_{Quillen} \to Top_{Quillen}$ is a [[Quillen adjunction|left]] [[Quillen equivalence]] (see [[homotopy hypothesis]]) we have

$$
  |hocolim_n Sing X_n| \simeq hocolim_n |Sing X_n| \simeq hocolim_n X_n
  \,.
$$

=-- 

See also ([Dugger, prop. 17.4, example 18.2](#Dugger)).

## Examples and Applications


### Classifying spaces

For $G$ a [[topological group]], write $\mathbf{B}G$ for its [[delooping]] [[topological groupoid]]: the topological groupoid with a single object and $Mor_{\mathbf{B}G}(*,*) \coloneqq  G$, with composition given by the product on $G$.

The [[nerve]] $N \mathbf{B}G$ of this topological groupoid is naturally a [[simplicial topological space]], with

$$
  N \mathbf{B}G \colon  [n] \mapsto G^{\times_n}
  \,.
$$

+-- {: .num_prop}
###### Proposition

The geometric realization of $N \mathbf{B}G$ is a model for the [[classifying space]] $B G$ of $G$-[[principal bundle]]s

$$
  {|N \mathbf{B}G|} \simeq B G
  \,.
$$

=--

An early reference for this classical fact is ([Segal68](#Segal68)).



### Topological principal $\infty$-bundles
 {#TopologicalPrincipalInfinityBundle}

We discuss aspects of [[principal ∞-bundle]]s equipped with topological [[cohesive (∞,1)-topos|cohesion]] and their geometric realization to [[principal bundle]]s in [[Top]].
 

Let $G$ be a [[simplicial topological group]]. 

Recall from the discussion at [[universal principal ∞-bundle]] that $\mathbf{E}G \to \mathbf{B}G$ is presented by the morphism of [[simplicial topological space]]s $W G \to \bar W G$. Recall also from [[simplicial topological group]] the following statement.

+-- {: .num_defn #GloballyKanSimplicialTopologicalSpace}
###### Definition

We say a morphism $f \colon  X \to Y$ of [[simplicial topological space]]s is a **global Kan fibration** if for all $n \in \mathbb{N}$ and $0 \leq k \leq n$ the canonical morphism

$$
  X_n \to Y_n \;\times_{sTop(\Lambda^n_k, Y)}\; sTop(\Lambda^n_k, X)
$$

in [[Top]] has a [[section]], where 

* $\Lambda^n_k \in $ [[sSet]] $\hookrightarrow Top^{\Delta^{op}}$ is the $k$th $n$-[[horn]] regarded as a [[discrete space|discrete]] [[simplicial topological space]]:

* $sTop(-,-) \colon  sTop^{op} \times sTop \to Top$ is the [[Top]]-valued [[hom object]], which may be regarded as a hom-object in the Top-[[enriched category|enriched]] [[functor category]] $sTop = [\Delta^{op},Top]$.

We say a [[simplicial topological space]] $X_\bullet \in Top^{\Delta^{op}}$ is **(global) Kan simplicial space** if the unique morphism $X_\bullet \to *$ is a global Kan fibration, hence if for all $n \in \mathbb{N}$ and all $0 \leq i \leq n$ the canonical [[continuous function]]

$$
  X_n \to sTop(\Lambda^n_k, X)
$$

into the [[topological space]] of $k$th $n$-[[horn]]s admits a [[section]] (in [[Top]], hence a global, continuous section).

=--

+-- {: .num_remark}
###### Remark

This global notion of Kan simplicial spaces is considered for instance in ([BrownSzczarba, def. 2.1](#BrownSzczarba)). In fact there a stronger condition is imposed: a [[Kan complex]] in [[Set]] automatically has the lifting property not only against all full [[horn]] inclusions but also aghainst sub-horns; and in ([BrownSzczarba](#BrownSzczarba)) all these fillers are required to be given by global sections. This ensures that with $X$ globally Kan also the [[internal hom]] $[Y,X] \in sTop$ is globally Kan, for any simplicial topological space $Y$. This is more than we need and want to impose here. For our purposes it is sufficient to observe that if $f$ is globally Kan in the sense of ([BrownSzczarba](#BrownSzczarba)), then it is so also in the [above sense](#GloballyKanSimplicialTopologicalSpace).

=--

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

+-- {: .num_prop #RealizationSimplicialTopologicalUniversalBundle}
###### Proposition

For $G$ a [[well-pointed simplicial topological group]], the geometric realization of the simplicial universal $G$-bundle

$$
  {\vert W G \vert} \to {\vert \bar W G \vert}
$$

is a global fibration [[resolution]] in $Top_{Quillen}$ of the point inclusion 
$* \to B{|G|}$.

=--

This is one of the central theorems proven in ([RobertsStevenson](#RobertsStevenson)).

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

This means that the degeneracy maps of $P_\bullet$ are induced degreewise by morphisms between pullbacks in [[Top]] that are degreewise [[closed cofibration]]s, where one of the morphisms in each pullback is a fibration. By the properties discussed at [[closed cofibration]], this implies that also these degeneracy maps of $P_\bullet$ are closed cofibrations.

=--

+-- {: .num_def}
###### Definition


Under the degreewise [[Yoneda embedding]] $sTop \hookrightarrow [Top^{op}, sSet]$ simplicial topological spaces embed into the category of [[simplicial presheaves]] on [[Top]].

We equip this with the projective [[model structure on simplicial presheaves]] $[Top^{op}, sSet]_{proj}$, and we speak of [[homotopy limit]]s in $sTop$ under this embedding.

=--

+-- {: .num_prop}
###### Proposition

The [[homotopy colimit]] operation

$$
  hocolim \colon  sTop \to Top
$$

preserves [[homotopy fiber]]s of morphisms $\tau \colon  X \to \bar W G$ with $X$ good and globally Kan and $G$ well-pointed.

=--


+-- {: .proof}
###### Proof

By prop. \ref{SimplicialTopologicalUniversalBundle} we have that $W G \to \bar W G$ is a fibration [[resolution]] of the point inclusion $* \to \bar W G$ in $[Top^{op}, sSet]_{proj}$.

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

By prop. \ref{SimplicialTopologicalUniversalBundle} and prop. \ref{SimplicialTopolgicalBundleIsGood} we have that all objects here 
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



## Related concepts

* [[simplicial topological space]], [[nice simplicial topological space]]

* [[simplicial topological group]]

* **geometric realization of simplicial spaces**



## References

The first occurence of the definition of geometric realization of simplicial topological spaces seems to be

* [[Graeme Segal]],  _Classifying spaces and spectral sequences_ Publications Math&#233;matiques de l'IH&#201;S, 34 (1968), p. 105-112  ([numdam](http://www.numdam.org/item?id=PMIHES_1968__34__105_0))
{#Segal68}

but the construction was implicit in earlier discussion of [[classifying space]]s. The observation that this is a [[coend]] was noted in

* [[Saunders MacLane]], _The Milgram bar construction as a tensor product of
functors_ SLNM Vol. 168 (1970)
{#MacLane}

The definition of _good_ simplicial topological spaces goes back to

* [[Graeme Segal]], _Configuration-Spaces and Iterated Loop-Spaces_ , 
  Inventiones math. 21,213-221 (1973)
{#Segal73}

An original reference on geometric realization of simplicial topological spaces is is appendix A of

* [[Graeme Segal]], _[[SegalCategoriesAndCohomologyTheories.pdf:file]]_ Topology, 13:293&#8211;312, 1974 
{#Segal74}

A standard textbook reference is chapter 11 of

* [[Peter May]], _The geometry of iterated loop spaces_ ([pdf](http://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))
{#May}

A proof that good simplicial spaces are proper is implicit in the proof of lemma A.5 in ([Segal74](#Segal74)). Explicitly it appears in

* L. Gaunce Lewis Jr., _When is the natural map $X\to \Omega \Sigma X$ a cofibration?_ , Trans. Amer. Math. Soc. **273** (1982) no. 1, 147--155 ([JSTOR](http://www.jstor.org/pss/1999197))
{#Lewis}

A generalization of the statement that good implies proper to other [[topological concrete categories]] and a discussion of the geometric realization of $W G \to \bar W G$ for $G$ a [[simplicial topological group]]  is in 

* [[David Roberts]], [[Danny Stevenson]], _Simplicial principal bundles in parametrized spaces_ (<a href="http://nlab.mathforge.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#RobertsStevenson">web</a>)
{#RobertsStevenson}

Comments on the relation between properness and cofibrancy in the [[Reedy model structure]] on $[\Delta^{op}, Set]$ are made in 

* [[Paul Goerss]], [[Kristen Schemmerhorn]], _Model Categories and Simplicial Methods_ ([arXiv:math.AT/0609537](http://arxiv.org/abs/math.AT/0609537)).

The relation between (fat) geometric realization and [[homotopy colimit]]s is considered as prop. 17.5 and example 18.2 of

* [[Daniel Dugger]], _A primer on homotopy colimits_ ([pdf](http://pages.uoregon.edu/ddugger/hocolim.pdf))
{#Dugger}

The (fat) geometric realization of ([[nerve]]s of) [[topological groupoid]]s is discussed in section 2.3 of

* [[David Gepner]], [[André Henriques]], _Homotopy theory of orbispaces_ ([pdf](http://www.math.uni-muenster.de/sfb/about/publ/heft448.pdf))
{#GepnerHenriques}



Globally Kan simplicial spaces are considered in 

* E. H. Brown and R. H. Szczarba, _Continuous cohomology and real homotopy
type_ , Trans. Amer. Math. Soc. 311 (1989), no. 1, 57 ([pdf](http://www.ams.org/journals/tran/1989-311-01/S0002-9947-1989-0929667-6/S0002-9947-1989-0929667-6.pdf))
{#BrownSzczarba}

The right adjoint to geometric realization of simplicial topological spaces is discussed in 

* R. M. Seymour, _Kan fibrations in the category of simplicial spaces_
Fund. Math., 106(2):141-152, 1980. 
{#Seymour}

## Refereeing

This entry is under review. See <a href="http://ncatlab.org/nlabreviewed/published/geometric+realization+of+simplicial+topological+spaces">geometric realization of simplicial topological spaces</a> at [[nlabreviewed:HomePage|nLab (reviewed)]].


[[!redirects geometric realization of a simplicial space]]
[[!redirects geometric realization of simplicial spaces]]

[[!redirects fat geometric realization of simplicial spaces]]
[[!redirects fat geometric realization of simplicial topological spaces]]

[[!redirects fat realization]]