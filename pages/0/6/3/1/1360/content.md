
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The term _simplicial model category_ is short for _[[model structure on simplicial sets|sSet]]${}_{Quillen}$-[[enriched model category]]_.

A simplicial model category is a model or presentation for an [[(∞,1)-category]] that is half way in between a bare [[model category]] and a [[Kan complex]]-[[enriched category]].

Specifically, a simplicial model category is an [[sSet]]-[[enriched category]] $C$ together with the structure of a [[model category]] on its underlying [[category]] $C_0$ such that both structures are compatible in a reasonable way.

One important use of simplicial model categories comes from the fact that the full [[sSet]]-subcategory $C^\circ \hookrightarrow C$ on the fibrant-cofibrant objects -- which is not just [[sSet]]-enriched but actually [[Kan complex]]-enriched -- is the [[(∞,1)-category]]-enhancement of the [[homotopy category]] of the [[model category]] $C_0$.

For generalizations of this construction with [[sSet]] replaced by another [[monoidal model category]] see [[enriched homotopical category]].

+-- {: .num_remark}
###### Remark

The term _simplicial model category_ for the notion described here is entirely standard, but in itself a bit suboptimal. More properly one would speak of [[simplicially enriched category]], which is a proper special case of a [[simplicial object]] in [[Cat]] (that for which the simplicial set of objects is discrete). 

The other caveat is that there are different model category structures on [[sSet]] and hence even the term $sSet$-[[enriched model category]] is ambiguous.

For instance the [[model structure for quasi-categories]] is an $sSet$-[[enriched model category]], but not for the standard Quillen model structure on the enriching category: since $sSet_{Joyal}$ is a [[closed monoidal category|closed]] [[monoidal model category]] it is enriched over itself, hence is a $sSet_{Joyal}$-enriched model category, not an $sSet_{Quillen}$-enriched one. So in the standard terminology, $sSet_{Joyal}$ is _not_ a "simplicial model category".
 
=--


## Definition

+-- {: .num_defn}
###### Definition

A **simplicial model category** is an [[enriched model category]] which is enriched over $sSet_{Quillen}$: the category [[sSet]] equipped with its standard [[model structure on simplicial sets]].

=--


Spelled out, this means that a simplicial model category is

* an [[sSet]]-[[enriched category]]

  * which is [[power|powered]] and [[tensoring|tensored]] over [[sSet]]

* with the structure of a [[model category]] on the underlying category $C_0$

* such that for every cofibration $i : A \to B$ and every fibration $p : X \to Y$ in $C_0$ the [[pullback powering]] of [[simplicial sets]] $C(B,X) \stackrel{i^* \times p_*}{\to} C(A,X) \times_{C(A,Y)} C(B,Y)$ is a [[Kan fibration]];

  * and such that this fibration is an acyclic fibration whenever either $i$ or $p$ are acyclic.

## Properties

### Enrichment, tensoring, and cotensoring 
 {#EnrichmentTensoringCotensoring}

Let $\mathcal{C}$ be a category equipped with the structure of a [[model category]] and with that of an [[sSet]]-[[enriched category]], i.e., which is [[tensoring|tensored]] and [[cotensoring|cotensored]] over [[sSet]].

+-- {: .num_prop #EquivalenceOfConditions}
###### Proposition

The following conditions -- that each make $\mathcal{C}$ into a _simplicial model category_ -- are equivalent:

1. the [[tensoring]] $\otimes : \mathcal{C} \times sSet \to \mathcal{C}$ is a left [[Quillen bifunctor]];

1. for any cofibration $X \to Y$ and fibration $A \to B$ in $\mathcal{C}$, the induced morphism 

   $$
     \mathcal{C}(Y, A) \to \mathcal{C}(X, A) \times_{\mathcal{C}(X,B)} \mathcal{C}(Y,B)
   $$

   is a fibration, and is in addition a weak equivalence if either of the two morphisms is;


1. for any cofibration $X \to Y$ in $sSet$ and fibration $A \to B$ in $\mathcal{C}$, the induced morphism 

   $$
     A^Y \to A^X \times_{B^X} B^Y
   $$

   is a fibration, and is in addition a weak equivalence if either of the two morphisms is.

=--

This follows directly from the defining properties of [[tensoring]] and [[cotensoring]].

We list in the following some implications of these equivalent conditions.

Let $\mathcal{C}$ now be a simplicial model category. 

+-- {: .num_cor}
###### Corollary

If $A \in \mathcal{C}$ is fibrant, and $X \hookrightarrow Y$ is a cofibration in [[sSet]], then 

$$
  A^{Y} \to A^{X}
$$

is a fibration in $\mathcal{C}$.

=--

+-- {: .proof}
###### Proof

Apply prop. \ref{EquivalenceOfConditions} to the case
of the cofibration $X \to Y$ and the fibration $A \to *$, where "$*$" denotes the [[terminal object]]. This yields that

$$
  A^Y \to A^X \times_{{*}^X} {*}^Y
$$

is a fibration. But ${*}^Y = {*}^X =  {*}$ and hence the claim follows.

=--

Similarly we have

+-- {: .num_cor}
###### Corollary

If $X \in \mathcal{C}$ is cofibrant and $A \in \mathcal{C}$ is fibrant, then $\mathcal{C}(X,A)$ is fibrant in [[sSet]], hence is a [[Kan complex]].

=--

+-- {: .proof}
###### Proof

Apply prop. \ref{EquivalenceOfConditions} to the cofibration $\emptyset \to X$, where "$\emptyset$" denotes the [[initial object]], and to the fibration $A \to *$ to find that 

$$
  \mathcal{C}(X, A) \to \mathcal{C}(\emptyset, A) \times_{\mathcal{C}(\emptyset,*)} \mathcal{C}(X,*)
$$

is a fibration. But since $\emptyset$ is initial and $*$ is terminal, all three simplicial sets in the fiber product on the right are the point, hence this is a fibration

$$
  \mathcal{C}(X,A) \to *
  \,.
$$

=--

### Derived hom-spaces

+-- {: .num_prop #DerivedHomSpaceBySimplicialFunctionComplex}
###### Proposition

For $X$ and $A$ any two objects and $Q X $ and $P A$ a cofibrant and fibrant replacement, respectively, $\mathcal{C}(Q X, P A)$ is the correct [[derived hom-space]] between $X$ and $A$ (see the discussion there). In particular the full $sSet$-enriched [[subcategory]] on cofibrant fibrant objects is therefore an [[simplicially enriched category|sSet-enriched category]] which is fibrant in the [[model structure on simplicially enriched categories]]. Its [[homotopy coherent nerve]] is a [[quasi-category]]. All this are intrinsic incarnatons of the [[(∞,1)-category]] that is [[presentable (∞,1)-category|presented]] by $C$.

=--

Although $\mathcal{C}(X,A)$ need not have the correct homotopy type for the mapping space if $X$ is not cofibrant or $A$ is not fibrant, simplicial notions of homotopy are still *sufficient* to detect the model-categorical ones.

+-- {: .num_prop #SimplicialHomotopyImpliesHomotopy}
###### Proposition
If $f,g:X\to A$ are simplicially homotopic (i.e. in the same connected component of the simplicial set $\mathcal{C}(X,A)$), then they represent the same map in the [[homotopy category]] of $\mathcal{C}$.  Therefore, any [[simplicial homotopy equivalence]] in $\mathcal{C}$ is a weak equivalence.
=--
+-- {: .proof}
###### Proof
This is Lemma 9.5.15 and Proposition 9.5.16 of [Hirschhorn](#Hirschhorn).
=--


## Examples

### General

* The  [[classical model structure on simplicial sets]] $sSet_{Quillen}$ is a [[closed monoidal category|closed]] [[monoidal model category]] and is hence naturally enriched, as a model category, over itself. This is the archetypical simplicial model category.

* The [[classical model structure on topological spaces]] for [[compactly generated topological spaces]] ([here](classical+model+structure+on+topological+spaces#ModelStructureOnCompactlyGeneratedTopologicalSpaces)) is similarly enriched over itself. Under [[geometric realization]] this also makes it a simplicial model category. 

  (See also for instance [Goerss-Schemmerhorn 06, p. 26](#GoerssSchemmerhorn06))

* For $C$ any small [[sSet]]-[[enriched category]] and $A$ [[simplicial combinatorial model category]], the [[global model structure on functors]] $[C^{op}, A]_{proj}$ and $[C^{op},A]_{inj}$ are themselved simplicial combinatorial model categories. See _[[model structure on simplicial presheaves]]_.

* The [[Bousfield localization of model categories|left Bousfield localization]] of a [[combinatorial simplicial model category]] at any set of morphisms is again a combinatorial simplicial model category. Large classes of examples arise this way. 

### Simplicial Quillen equivalent models 
  {#SimpEquivMods}

While many model categories do not admit an $sSet_{Quillen}$-enrichment, for large classes of model categories one can find a [[Quillen equivalence]] to a model category that does have an $sSet_{Quillen}$-enrichment.

These are constructed as [[Bousfield localization of model categories|Bousfield localization]] of [[Reedy model structures]] on the [[category of simplicial objects]] in the given model category. 


+-- {: .num_defn #LocalizationOfStructureOnSimplicalObjects}
###### Definition

Let $C$ be a 

* [[left proper model category|left proper]]

* [[combinatorial model category]].

By the discussion at _[[cofibrantly generated model category]]_ in the section _[Presentation and generation](http://ncatlab.org/nlab/show/cofibrantly+generated+model+category#PresentationAndGeneration)_ there exists a [[small set]] $E \subset Obj(C)$ of objects that detect weak equivalences. For some such choice of $E$, let 

$$
  S 
   := 
  \{ \; e \cdot (\Delta[k] \to \Delta[l]) \; \}_{e \in E, ([k] \to [l]) \in \Delta}
 \subset Mor([\Delta^{op}, sSet])
$$

where $e \cdot \Delta[k] : [n] \mapsto \coprod_{\Delta([n],[k])} e$.

Write

$$
  [\Delta^{op}, C]_{proj, S}
  \stackrel{\longleftarrow}{\longrightarrow}
  [\Delta^{op}, C]_{proj}
$$

for the [[Bousfield localization of model categories|left Bousfield localization]] of the projective [[model structure on functors]] at this set $S$ of morphisms.

Similarly, write 

$$
  [\Delta^{op}, C]_{Reedy, S}
  \stackrel{\leftarrow}{\longrightarrow}
  [\Delta^{op}, C]_{Reedy}
$$

for the left Bousfield localization of the [[Reedy model structure]] at $S$.


=--

+-- {: .num_lemma #HocolimOverHomotopyConstantSimplicialDiagram}
###### Lemma

Let $C$ be a [[cofibrantly generated model category]].

If $X \in [\Delta^{op}, C]$ is degreewise cofibrant and has all structure maps being weak equivalences, then all $X_i \to hocolim X$ are weak equivalences.

Hence $X \to const\,hocolim X$ is a weak equivalence.

=--


This appears as ([Dugger, prop. 5.4 corollary 5.5](#Dugger)). 

+-- {: .num_theorem #LocalizationOfReedyOnSimplicialObjects}
###### Theorem

The model structures from def. \ref{LocalizationOfStructureOnSimplicalObjects} have the following properties.

1. The weak equivalences in both are precisely those morphisms which become weak equivalences under [[homotopy colimit]] over $\Delta^{op}$.

1. The fibrant objects in both are precisely those objects that are fibrant in the corresponding unlocalized structures, and such that all the face and degeneracy maps are weak equivalences in $C$.


1. The [[colimit]]/constant [[adjoint functors]]

   $$
     (\lim_{\to} \dashv const)
     \colon
     C
     \stackrel{\overset{\lim_\to}{\longleftarrow}}{\underset{const}{\longrightarrow}}
     [\Delta^{op}, C]_{proj, S}
   $$

   constitute a [[Quillen equivalence]], the identity functors constitute a Quillen equivalence

   $$
     [\Delta^{op}, C]_{Reedy, S}
     \stackrel{\overset{id}{\longleftarrow}}{\underset{id}{\longrightarrow}}
     [\Delta^{op}, C]_{proj, S}
     \,,
   $$

   and the constant/[[limit]] [[adjoint functors]] (since $\Delta^{op}$ has an [[initial object]] the limit is evaluation in degree 0) constitute a Quillen equivalence

   $$
     (const \dashv ev_0) 
      : 
     [\Delta^{op}, C]_{Reedy,S}
      \stackrel{\overset{const}{\longleftarrow}}{\underset{ev_0}{\longrightarrow}}
     C
     \,;
   $$

1. The canonical [[sSet]]-[[enriched category|enrichment]]/[[tensoring]]/[[powering]] of the [[category of simplicial objects]] $[\Delta^{op}, C]$ makes $[\Delta^{op}, C]_{Reedy,S}$ (but _not_ in general $[\Delta^{op}, C]_{proj,S}$) into a simplicial model category.

=--

This is ([Dugger, theorem 5.2, theorem 5.7, theorem 6.1](#Dugger)). 

So in particular every [[proper model category|left proper]] [[combinatorial model category]] is [[Quillen equivalence|Quillen equivalent]] to a simplicial model category.

+-- {: .proof}
###### Proof

We first show that the fibrant objects in $[\Delta^{op}, C]_{proj,S}$ are the objectwise fibrant objects all whose structure maps are weak equivalences in $C$. The argument for the fibrant objects in $[\Delta^{op}, C]_{Reedy,S}$ is directly analogous.

By general properties of [[Bousfield localization of model categories|left Bousfield localization]], the 
fibrant objects in $[\Delta^{op}, C]_{proj,S}$ are the projective fibrant objects $X$ for which all induced morphisms on [[derived hom spaces]]

$$
  \mathbb{R}Hom_{[\Delta^{op}, C]_{proj}}(s \cdot(\Delta[k] \to \Delta[l]), X)
$$ 

are weak equivalences. Since $s$ is cofibrant in $C$ by definition, also  $s \cdot \Delta[k]$ is cofibrant in 
$[\Delta^{op}, C]_{proj}$. 

So for $X \in [\Delta^{op}, C]_{proj}$ fibrant, 
let $X_\bullet \in [\Delta^{op}, [\Delta^{op}, C]]$ 
be a [simplicial framing](derived+hom+space#Framings) for it. 
Notice that this means that for all $n \in \mathbb{N}$
also $X_\bullet([n])$ is a simplicial framing for $X([n])$.
This is because

1. $const X \to X_\bullet$ being a weak equivalence means that for all $n$ the morphism $X \to X_n$ is a weak equivalence, which means that for all $k$ the morphism $X([k]) \to X_n([k])$ is a weak equivalence.

1. $X_\bullet$ being fibrant in $[\Delta^{op}, [\Delta^{op}, C]_{proj}]_{Reedy}$ means that for all $n\in \mathbb{N}$ the morphism $X_{\Delta[n]} \to X_{\partial \Delta[n]}$ is a fibration in $[\Delta^{op}, C]_{proj}$, hence that for all $k \in \mathbb{N}$ the morphism $X_{\Delta[n]}([k]) \to X_{\partial \Delta[n]}([k])$ is a fibration in $C$, hence that $X([k])$ is Reedy fibrant.

Then we find

$$
  \begin{aligned}
    \mathbb{R}Hom_{[\Delta^{op}, C]_{proj}}( s \cdot(\Delta[k] \to \Delta[l]), X)
	& \simeq
	Hom_{[\Delta^{op}, C]}(s \cdot(\Delta[k] \to \Delta[l]), X_\bullet)
	\\
	& \simeq
	Hom_{C}(s , X_\bullet([l]) \to X_\bullet([k]))	
	\\
	& \simeq
	\mathbb{R}Hom_C(s, X([l]) \to X([k]))
	\,.
  \end{aligned}
$$

By assumption on the set $S$, this implies the claim.


$\,$


Now we show that the weak equivalences in $[\Delta^{op}, C]_{proj,S}$ are precisely
those morphisms that become weak equivalences under 
the [[homotopy colimit]].

By functorial [[cofibrant resolution]] and [[two-out-of-three]], it is sufficient to  show that this holds for morphisms between cofibrant objects. 

By lemma \ref{HocolimOverHomotopyConstantSimplicialDiagram}, we have weak equivalences

$$
  \mathbb{R}Hom_{[\Delta^{op}, C]}(A,X)
  \stackrel{\simeq}{\to}
  \mathbb{R}Hom_{[\Delta^{op}, C]}(A, const Z)
  \stackrel{\simeq}{\to}
  \mathbb{R}Hom_{C}(\lim_\to A , Z)
$$

seen by computing the derived homs by [simplicial framings](derived+hom+space#Framings).

Now, by properties of left [[nLab:Bousfield localization of model categories|Bousfield localization]], 
$A \to B$ is a weak equivalence if for all $S$-[[local objects]] $X$ the morphism $\mathbb{R}Hom(A \to B, X)$ is a weak equivalence. Looking at the diagram

$$
  \array{
    \mathbb{R}Hom_{[\Delta^{op}, C]}(A,X)
    &\stackrel{\simeq}{\to}&
    \mathbb{R}Hom_{[\Delta^{op}, C]}(A, const Z)
    &\stackrel{\simeq}{\to}&
    \mathbb{R}Hom_{C}(\lim_\to A , Z)
   \\
   \uparrow && \uparrow && \uparrow
   \\
    \mathbb{R}Hom_{[\Delta^{op}, C]}(B,X)
    &\stackrel{\simeq}{\to}&
    \mathbb{R}Hom_{[\Delta^{op}, C]}(B, const Z)
    &\stackrel{\simeq}{\to}&
    \mathbb{R}Hom_{C}(\lim_\to B , Z)
  }
$$

we see that this is the case precisely if the vertical morphism on the right is a weak equivalence for all fibrant $Z \in C$, which is the case if $\lim_\to A \to \lim_\to B$ is a weak equivalence. Since $A$ and $B$ here are cofibrant in $[\Delta^{op}, C]_{proj}$, the colimits here are indeed [[homotopy colimits]] (as discussed there). 

$\,$


Now we discuss that $(\lim_\to \dashv const): C \to [\Delta^{op}, C]_{proj,S}$ 
is a [[Quillen equivalence]].
First observe that on the global model structure $const : C \to [\Delta^{op}, C]_{proj}$ is clearly a right Quillen functor, hence we have a Quillen adjunction on the unlocalized structure. Moreover, by definition and by the above discussion, the [[derived functor]] of the [[left adjoint]] $\lim_\to$, namely the [[homotopy colimit]], takes the localizing set $S$ to weak equivalences in $C$. Therefore the assumptions of the discussion at _[Quillen equivalence - Behaviour under localization](http://ncatlab.org/nlab/show/Quillen+adjunction#BehaviourUnderLocalization)_ are met, and hence it follows that $(\lim_\to \dashv const)$ descends as a Quillen adjunction also to the localization.

To see that this is a Quillen equivalence,
it is sufficient to show that for $A \in [\Delta^{op}, C]_{proj}$ cofibrant
and $Z \in C$ fibrant, a morphism $\lim_\to A \to Z$ is a weak equivalence in $C$
precisely if the [[adjunct]] $A \to const Z$ becomes a weak equivalence under the homotopy colimit.


For this notice that we have a commuting diagram

$$
  \array{  
     hocolim A &\to& hocolim(const Z)
     \\
     \downarrow && \downarrow
     \\
     colim A &\to& colim (const Z) & \simeq Z
  }
$$

and so our statement follows (by 2-out-of-3) once we know that the vertical morphisms here are weak equivalences. The left one is because $A$ is cofibrant, by assumption, as before.  To see that the right one is, too, consider the factorization

$$
  Z \to (const Z)_i \to hocolim (const Z) \to Z
$$

of the identity on $Z$, for any $i \in \mathbb{N}$. By lemma \ref{HocolimOverHomotopyConstantSimplicialDiagram} the first morphism is a weak equivalence, and hence so is the morphism in question.

$\,$

Now we show that the weak equivalences in $[\Delta^{op}, C]_{Reedy,S}$ are the hocolim-equivalences. 

By a general result on [functoriality of localization](Bousfield+localization+of+model+categories#FunctorialityOfLocalization), we have that the $(id \dashv id ) : [\Delta^{op}, C]_{Reedy,S} \stackrel{\leftarrow}{\to} [\Delta^{op}, C]_{proj,S}$ is at least a [[Quillen adjunction]]. 

Let then $A \to B$ be a morphism in $[\Delta^{op}, C]$ and consider two fibrant replacements

$$
  \array{
    A &\to& \bar A &\to & \hat A
    \\
    \downarrow && \downarrow && \downarrow
    \\
    B &\to& \bar B &\to& \hat B
  }
  \,,
$$

where the first one ($\bar A \to \bar B$) is taken in $[\Delta^{op}, C]_{proj,S}$ and the second ($\hat A \to \hat B$) in $[\Delta^{op}, C]_{Reedy}$. 

Assume first that $A \to B$ is a hocolim-equivalence. Then so is $\hat A \to \hat B$, because the horizontal morphisms are all objectwise weak equivalences. But $\hat A$ and $\hat B$ are fibrant in $[\Delta^{op}, C]_{Reedy}$, hence in $[\Delta^{op}, C]_{proj}$ by construction and at the same time all their structure maps are weak equivalences (use 2-out-of-3), so that they are in fact fibrant in $[\Delta^{op}, C]_{proj,S}$. By general properties of left Bousfield localization, weak equivalences between local fibrant objects are already weak equivalences in the unlocalized structure -- so $\hat A \to \hat B$ is indeed even an objectwise weak equivalence. It follows then that so is $\bar A \to \bar B$, which is therefore in partiular a weak equivalence in $[\Delta^{op}, C]_{Reedy, S}$. Finally the left horizontal morphisms are also weak equivalences in $[\Delta^{op}, C]_{Reedy,S}$, by the above Quillen adjunction. So finally by 2-out-of-3 in $[\Delta^{op}, C]_{Reedy,S}$ it follows that also $A \to B$ is a weak equivalence there.

By an analogous diagram chase, one shows the converse implication holds, that $A \to B$ being a weak equivalence in $[\Delta^{op}, C]_{Reedy,S}$ implies that it is a hocolim-equivalence.

With this now it is clear that the identity adjunction above is in fact a Quillen equivalence.

$\,$

Finally we show that $(const \dashv ev_0) : [\Delta^{op}, C]_{Reedy,S}
\stackrel{\overset{const}{\leftarrow}}{\underset{ev_0}{\to}} C$ is a Quillen equivalence. 

First, it is immediate to check that $const : C \to [\Delta^{op}, C]_{Reedy}$ is left Quillen, and since $id : [\Delta^{op}, C]_{Reedy} \to [\Delta^{op}, C]_{Reedy,S}$ is left Quillen by definition of Bousfield localization, the above is at least a Quillen adjunction.

To see that it is a Quillen equivalence, let $A \in C$ be cofibrant and $X \in [\Delta^{op}, C]_{Reedy,S}$ be fibrant -- which by the above means that it is a simplicial resolution -- and consider a morphism $const A \to X$. We need to show that this is a weak equivalence, hence, by the above, that its hocolim is a weak equivalence, precisely if $A \to X_0$ is a weak equivalence in $C$.

To that end, find a cofibrant resolution $const \tilde A \to \tilde X$ of $const A \to X$ in $[\Delta^{op}, C]_{proj}$ and consider the diagram

$$
  \array{
    A &\stackrel{\simeq}{\leftarrow}&  \tilde A &\stackrel{\simeq}{\to}&
    colim(const \tilde A)
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X_0 &\stackrel{\simeq}{\leftarrow}& \tilde X_0
    &\stackrel{\simeq}{\to}& colim \tilde X
  }
  \,.
$$

The colimits on the right compute the homotopy colimit. By 2-out-of-3 it 
follows that the right vertical morphism is a weak equivalence precisely
if the left vertical morphisms is.

$\,,$

Finally it remains to show that $[\Delta^{op}, C]_{Reedy,S}$ is a simplicially enriched model category. (...)

=--

+-- {: .num_theorem #AUniquenessTheorem}
###### Remark
**(uniqueness)**

Let $C$ be a [[model category]]. Then there is a unique model category 
structure on $s C = [\Delta^{op}, C]$ such that

* every morphism that is degreewise a weak equivalence in $C$ is a weak equivalence;

* the cofibrations are those of the [[Reedy model structure]];

* the fibrant objects are the Reedy-fibrant objects whose face and
  degeneracy maps are weak equivalences in $C$.

=--

This is ([Rezk-Schwede-Shipley, theorem 3.1](#RezkSchwedeShipley)).

+-- {: .proof}
###### Proof

By theorem \ref{LocalizationOfReedyOnSimplicialObjects}
at least one such model structure exists.
By the discussion at _[model category -- Redundancy of the axioms](model%20category#RedundancyInTheAxioms)_, the classes of cofibrations and fibrant objects already determine a model category structure.

=--

+-- {: .num_cor #DerivedHomBySimplicialReplacement}
###### Corollary

For $C$ any [[proper model category|left proper]] 
[[combinatorial model category]], the [[derived hom-space]]
between two objects $X, A$ may be computed by

* choosing a cofibrant replacement $\hat X$ of $X$ in $C$;

* choosing a Reedy fibrant replacement $\hat A$ of $const A$ in $[\Delta^{op}, C]$ such that all face and degeneracy maps are weak equivalences,

setting

$$
  Maps(X,A) : [n] \mapsto Hom_C(\hat X, \hat A_n)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By theorem \ref{LocalizationOfReedyOnSimplicialObjects} we may compute the
[[derived hom space]] in $[\Delta^{op}, C]_{Reedy,S}$ after the inclusion $const : C \to [\Delta^{op}, C]$. Since by that theorem $[\Delta^{op}, C]_{Reedy,S}$ is a simplicial model category, by prop. \ref{DerivedHomSpaceBySimplicialFunctionComplex}
the derived hom space is given by the simplicial function complex between a cofibrant replacement of $const X$ and a fibrant replacement of $const A$. If $\hat X$ is cofibrant, then $const \hat X$ is already Reedy cofibrant, and by the theorem $\hat A$ as stated is a a fibrant resolution of $const A$. Finally, the theorem says that the simplicial function complex is given by

$$
  \begin{aligned}
    [\Delta^{op}, C](const \hat X, \hat A)_n
    & =
    Hom_{[\Delta^{op}, C]}((const \hat X) \cdot \Delta[n], \hat A)
    \\
    &  \simeq
    Hom_{[\Delta^{op}, C]}((const \hat X) , \hat A^{\Delta[n]})
    \\
    & \simeq
    Hom_C(\hat X, \hat A_n)
  \end{aligned}
  \,.
$$

=--


There is also a version for stable model categories:

+-- {: .num_theorem }
###### Theorem

Every [[proper model category|proper]] [[cofibrantly generated model category|cofibrantly generated]] [[stable model category]] is [[Quillen equivalence|Quillen equivalent]] to a simplicial model category

=--

This is ([Rezk-Schwede-Shipley, prop 1.3](#RezkSchwedeShipley)).


### Combinatorial simplicial model categories

A particularly important type of simplicial model categories are those that are also [[combinatorial model category|combinatorial model categories]].

A [[combinatorial simplicial model category]] is precisely a _presentation_ for a [[locally presentable (∞,1)-category]]. See there for more details.




## References

The definition appears in 

* {#Quillen67} [[Dan Quillen]], chapter II, section 2 of: _Homotopical algebra_, Lecture Notes in Mathematics __43__, Springer-Verlag 1967 ([doi:10.1007/BFb0097438](https://link.springer.com/book/10.1007/BFb0097438))

Textbook references include

* {#Hirschhorn} [[Philip Hirschhorn]], section 9.1.5 of _Model categories and their localizations_, volume 99 of Mathematical Surveys and Monographs , American Mathematical Society, 2009.

* [[Jacob Lurie]], section A.3 in _[[Higher Topos Theory]]_

Further review includes

* {#GoerssSchemmerhorn06} [[Paul Goerss]], [[Kristen Schemmerhorn]], _Model categories and simplicial methods_ ([arXiv:math/0609537](http://arxiv.org/abs/math/0609537))
 
Further developments include

* {#RezkSchwedeShipley} [[Charles Rezk]], [[Stefan Schwede]], [[Brooke Shipley]], _Simplicial structures on model categories and functors_, American Journal of Mathematics, Vol. 123, No. 3 (Jun., 2001), pp. 551-575  ([arXiv:0101162](http://arxiv.org/abs/math/0101162), [jstor](http://www.jstor.org/stable/pdfplus/25099071.pdf))
 

* {#Dugger} [[Dan Dugger]], _Replacing model categories with simplicial ones_, Trans. Amer. Math. Soc. vol. 353, number 12 (2001), 5003-5027. ([pdf](http://hopf.math.purdue.edu/Dugger/smod.pdf)) 
  



[[!redirects simplicial model categories]]
[[!redirects sSet-model category]]
[[!redirects sSet-model categories]]

[[!redirects simplicial model structure]]
[[!redirects simplicial model structures]]