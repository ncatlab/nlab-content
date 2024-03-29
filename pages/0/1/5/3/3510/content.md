
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The notion of _[[complete Segal space]]_ is a model for the notion of [[(∞,1)-category]] regarded as an [[internal category in an (∞,1)-category]] in [[∞Grpd]]. 

The _[[model category]] structure_ on the collection of all [[bisimplicial sets]] is a [[presentable (∞,1)-category|presentation]] the [[(∞,1)-category]] of all complete Segal spaces, hence for the [[(∞,1)-category of (∞,1)-categories]].

## Definition

We first discuss the model structure

* [for complete Segal spaces](#ForCompleteSegalSpaces)

as such, and then more generally model structures 

* [for complete Segal space objects](#ForCompleteSegalSpaceObjects)

in a suitable ambient model category $\mathcal{C}$, which reproduce
the previous case when $\mathcal{C} = sSet_{Quillen}$.

### For complete Segal spaces
 {#ForCompleteSegalSpaces}

Write [[sSet]] for the [[category]] of [[simplicial sets]], which here we always think of as equipped with the standard [[model structure on simplicial sets]]  that is a [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-category]] [[∞Grpd]].

Write $[\Delta^{op}, sSet]$ for the category of [[simplicial objects]] in $sSet$, hence for the category of [[bisimplicial sets]]. This inherits from $sSet$ in particular the 

* [[Reedy model structure]] $[\Delta^{op}, sSet]_{Reedy}$, 

which is a [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-category]] of [[simplicial objects]] in [[∞Grpd]]. In all of the following in its place one can also use the 

* projective or injective [[model structure on functors]] $[\Delta^{op}, sSet]_{proj}$, $[\Delta^{op}, sSet]_{inj}$.


Write $c : Set \to sSet$ for the inclusion of sets as [[discrete objects]] into [[simplicial sets]]. Write 

$$
   [\Delta^{op}, c] : sSet \to [\Delta^{op}, sSet]
$$ 

for the corresponding inclusion of simplicial sets into bisimplicial sets.

When we think in the following of a simplicial set in the context of $[\Delta^{op}, sSet]$, we always do so via this inclusion (and not via the _other_ natural such inclusion!).


+-- {: .num_defn #RezkModelStructure}
###### Definition

The _model structure for complete Segal spaces_ is the [[Bousfield localization of model categories|left Bousfield localization]] of $[\Delta^{op}, sSet]_{Reedy}$ at the set of morphisms

$$
  W 
  :=
  \{
     Sp[n] \hookrightarrow \Delta[n]
  \}_{n \in \mathbb{N}}
  \cup
  \{
    N(\{a \stackrel{\simeq}{\to} b\}) \to *
  \}
  \,,
$$

where the first summand is the set of [[spine]] inclusions, while the second summand is the singleton containing the morphism from the [[nerve]] of the [[groupoid]] with two objects and precisely one non-identity morphism (and its inverse) from one to the other.

=--


This appears originally in section 12 of ([Rezk](#Rezk)).

+-- {: .num_remark}
###### Remark

Equivalently one can replace here the [[spine]] inclusions with the 
[[inner Kan fibration|inner]] [[horn]] inclusions.

=--

+-- {: .num_remark}
###### Remark

An object $X \in [\Delta^{op}, sSet]$ being a [[local object]] with respect to the $n$th [[spine]] inclusion says that the morphism

$$
  X_n \to X_1 \times_{X_0} \cdots \times_{X_0} X_1
$$

(with $n$ factors on the right) is a [[weak homotopy equivalence]] of simplicial sets. Therefore the objects which are local with respect to all spine inclusions are precisely the [[Segal spaces]].

Accordingly, an object is furthermore local also with respect to $J \to *$ if it is a [[complete Segal space]].

=--
The model category structure thus obtained is characterized as follows.

+-- {: .num_prop}
###### Proposition

The category $[\Delta^{op}, sSet] = [\Delta^{op}\times \Delta^{op}, Set]$ of [[bisimplicial sets]] carries the structure of an [[sSet]]-[[enriched category]] with [[hom-object]] for two bisimplicial sets $X$ and $Y$ given by

$$
  hom(X,Y) := i_2^*(Y^X)
  \,,
$$

where

* $Y^X$ is the [[internal hom]] in the standard [[closed monoidal structure on presheaves]];

* $i_2 : \Delta \to \Delta \times \Delta$ is the [[right adjoint]] to the projection $\Delta \times \Delta \to \Delta$ on the second factor, given by $i_2 : [n] \mapsto ([0],[n])$.

This refines to the structure of a

* [[left proper model category|left proper]]

* [[cartesian monoidal category|cartesian]] [[closed monoidal category|closed]] [[monoidal model category|monoidal]]

* [[simplicial model category]] 

by setting

* cofibrations are the [[monomorphisms]]

* weak equivalences are the **Rezk weak equivalences**:. those morphisms $u : A \to B$ such that for all [[complete Segal space]]s $X$ the morphism $hom(u,X) : hom(B,X) \to hom(A,X)$ is a weak equivalence in the standard [[model structure on simplicial sets]].

The fibrant objects in the structure are precisely the [[complete Segal spaces]].

=--

This is essentially ([Rezk, theorem 7.2](#Rezk)).
See also ([Joyal-Tierney, theorem 4.1](#JoyalTierney)). 

### For complete Segal space objects
 {#ForCompleteSegalSpaceObjects}

We may generalize from complete Segal spaces to complete Segal space objects in an ambient context other tham [[∞Grpd]] $\simeq (sSet_{Quillen})^\circ$: 

Let $C$ be a [[simplicial combinatorial model category]]. Write $C^\circ$ for the [[(∞,1)-category]] [[presentable (∞,1)-category|presented]] by it. Write $[\Delta^{op}, C]$ for the [[functor category]]/category of [[simplicial objects]] in $C$. 

+-- {: .num_prop}
###### Proposition

There is the structure of a  [[simplicial model category]] on $[\Delta^{op}, C]$ such that

1. is is a [[Bousfield localization of model categories|left Bousfield localization]] of the injective [[model structure on functors]] $[\Delta^{op}, C]_{inj}$;

1. such that the [[fibrant objects]] $X \colon \Delta^{op} \to C$ are precisely the injectively fibrant objects such that furthermore there image under $[\Delta^{op}, C] \to ([\Delta^{op},C])^\circ$ is an [[internal (∞,1)-category]] in $C^\circ$.

=--

([Lurie, prop. 1.5.4, remark 1.5.6](#Lurie))

## Properties

### Cartesian monoidal model structure
 {#CartesianMonoidalModelStructure}

+-- {: .num_prop}
###### Proposition

The category $[\Delta^{op}, sSet]$ is a [[cartesian closed category]]. This [[closed monoidal category]]-structure is compatible with the model category structure in that it makes $[\Delta^{op}, sSet]_{cSegal}$ into a [[monoidal model category]].

=--

This is the last clause of ([Rezk, theorem 7.2](#Rezk)). The key lemma for establishing this clause is ([Rezk, prop. 9.2](#Rezk)).

### Relation to other model structures

#### Model structure for quasi-categories 
  {#RelQCat}

We discuss the relation to the [[model structure for quasi-categories]]. 

(See also at _[[model structure for dendroidal complete Segal spaces]]_ the section _[Relation to quasi-operads](/model+structure+for+dendroidal+complete+Segal+spaces#RelationToDendroidalSets)_ .)

A quick way to say the following turns out to be to say that the model structure for complete Segal spaces is the [simplicial completion of Cisinski model structures](Cisinski+model+structure#SimplicialCompletion) of the [[model structure for quasi-categories]] (see ([Ara](#Ara))).

+-- {: .num_defn #GroupoidalSimplices}
###### Definition

For $n \in \mathbb{N}$, write 

$$
  \Delta_J[n] := N(0 \stackrel{\simeq}{\to} \cdots \stackrel{\simeq}{\to} n)
  \in sSet
$$

for the [[nerve]] of the [[free construction|free]] [[groupoid]] on $\Delta[n]$
(the [[codiscrete groupoid]] in $(n+1)$ objects.) This extends to a functor

$$
  \Delta_J : \Delta \to sSet
  \,.
$$

=--

+-- {: .num_prop #ComparisonAdjunctions}
###### Proposition


We have the following pair of [[adjoint functors]] between [[simplicial sets]] and [[bisimplicial sets]].

The first is

$$
  (p_1^* \dashv i_1^*)
  :
  [\Delta^{op}, Set]
  \stackrel{\overset{i_1^*}{\leftarrow}}{\underset{p_1^*}{\to}}
  [\Delta^{op} \times \Delta^{op}, Set]
$$

where $i_1^*$ sends a bisimplicial set to the simplicial set of its first row

$$
  i_1^* : X_{\bullet,\bullet} \mapsto X_{\bullet, 0}
  \,.
$$

The other is

$$
  (t_! \dashv t^!)
  :
  [\Delta^{op} \times \Delta^{op}, Set]
  \stackrel{\overset{t^!}{\leftarrow}}{\underset{t_!}{\to}}
  [\Delta^{op}, Set]
$$

where 

* $t_!$ assigns the [[total simplicial set]] to a [[bisimplicial set]]: it is the left [[Kan extension]] of the functor $t : \Delta \times \Delta \to ssSet$ given by $([k],[l]) \mapsto \Delta[k]\times \Delta_J[l]$ (with $J$ from def. \ref{GroupoidalSimplices}) along the [[Yoneda embedding]]

  $$
    t_!(X_{\bullet,\bullet})
    =
    \int^{[k],[l]}
      X_{k,l} \cdot \Delta[k] \times \Delta_J[l]
      \,;
  $$

* and where $t^!$ forms in each degree the mapping space

  $$
    t^! : X_\bullet \mapsto 
    \left(
     [m,n] \mapsto 
      Hom_{sSet}( \Delta[m] \times \Delta_J[n], X)
    \right)
    \,.
  $$

=--

+-- {: .num_prop}
###### Proposition

The composite of the two adjunctions from prop. \ref{ComparisonAdjunctions}

$$
  sSet
    \stackrel{\overset{i_1^* t^!}{\leftarrow}}{\underset{t_! p_1^*}{\to}}
  sSet
$$

is the identity adjunction: both functors are [[isomorphic]] to the identity functor.

=--


This appears at the end of the proof of ([Joyal-Tierney, theorem 4.12](#JoyalTierney)). 



+-- {: .num_prop}
###### Proposition

Both adjunctions of prop. \ref{ComparisonAdjunctions} are [[Quillen equivalences]] between the [[model structure for quasi-categories]] on simplicial sets and the Rezk model structure for complete Segal spaces on bisimplicial sets, def. \ref{RezkModelStructure}.

=--


This appears ([Joyal-Tierney, theorem 4.11, 4.12](#JoyalTierney)). 


#### Model structure for dendroidal complete Segal spaces

The [[operad|operadic]] analog of [[simplicial sets]] / [[bisimplicial sets]] are [[dendroidal sets]] / dendroidal spaces, parameterized over the [[tree category]] $\Omega$

$$
  dsSet := [\Omega^{op}, sSet]
  \,.
$$

Write $\eta \in \Omega \hookrightarrow dSet \hookrightarrow dsSet$ for the [[tree]] with a single edge and no non-trivial vertex. 

Then [[slice category]] of $dsSet$ over $\eta$ is evidently equivalent to that of [[bisimplicial sets]]

$$
  ssSet \simeq dsSet_{/\eta} 
  \hookrightarrow
  dsSet
  \,.
$$

By restriction along this inclusion, the 
[[model structure for dendroidal complete Segal spaces]] reproduces the above model structure. See there for more details.

## Related concepts

* [[model structure for dendroidal complete Segal spaces]]

* [[table - models for (infinity,1)-operads]]

## References

Complete Segal spaces were originally defined in 

* {#Rezk} [[Charles Rezk]], _A model for the homotopy theory of homotopy theory_ , Trans. Amer. Math. Soc., 353(3), 973-1007 ([pdf](http://www.math.uiuc.edu/~rezk/rezk-ho-models-final-changes.pdf))
 

The [[Quillen equivalence]] with the [[model structure for quasi-categories]] is discussed in 

* {#JoyalTierney} [[André Joyal]], [[Myles Tierney]], _Quasi-categories vs Segal spaces_ ([arXiv:0607820](http://arxiv.org/abs/math/0607820))
 

A survey of the model structures and their relations is in 

* {#Bergner} [[Julia Bergner]], _A survey of $(\infty, 1)$-categories_ ([arXiv](http://arxiv.org/abs/math.AT/0610239)).
 

The generalization to _complete Segal objects_ in model categories other than $sSet$ was considered in 

* {#Lurie} [[Jacob Lurie]], _$(\infty,2)$-Categories and the Goodwillie calculus_ ([arXiv:0905.0462](http://arxiv.org/abs/0905.0462))
 

Discussion in terms of [[Cisinski model structures]] is in 

* {#Ara}[[Dimitri Ara]], _Higher quasi-categories vs higher Rezk spaces_ ([arXiv:1206.4354](http://arxiv.org/abs/1206.4354))

A model structure for [[(infinity,2)-sheaves]] of complete Segal spaces is discussed in
 

* [[Nicholas Meadows]], _Local Complete Segal Spaces_ ([arXiv:1607.05794](http://arxiv.org/abs/1607.05794))

