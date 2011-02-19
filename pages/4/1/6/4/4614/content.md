
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

For $X_\bullet$ a [[simplicial object]] in [[Top]] --  a [[simplicial topological space]] -- its _[[geometric realization]]_ is a plain [[topological space]] $|X_\bullet| \in Top$ obtained by gluing all topological space $X_n$ together, as determined by the face and degeneracy maps.

The construction of $|X_\bullet|$ is a direct analog of the ordinary notion of [[geometric realization]] of a [[simplicial set]], but taking into account the [[topology]] on the spaces of $n$-simplices $X_n$.

## Definition

Let [[Top]] in the following denote the [[category]] 

* of [[compactly generated space|compactly generated]] [[weakly Hausdorff space]]s 

* or the category of [[k-space]]s.

Write $\Delta_{Top} : \Delta \to Top : [n] \mapsto \Delta^n_{Top}$ for the standard [[cosimplicial object|cosimplicial]] [[topological space]] of topological [[simplices]].

Write equivalently

$$
  Top^{\Delta^{op}} := sSet := [\Delta^{op}, Top]
$$

for the category of [[simplicial topological space]]s.

+-- {: .num_defn #GeometricRealization}
###### Definition

For $X_\bullet : \Delta^{op} \to Top$ [[simplicial topological space]], its **geometric realization** is the [[coend]]

$$
  |X_\bullet| :  \int^{n \in \Delta} X_n \times \Delta^n_{Top}
$$

formed in [[Top]].

=--

More explicitly, this is the [[topological space]] given by the [[quotient]]

$$
  \vert X_\bullet \vert = \coprod_{n} \Delta^n_{Top} \times X_n /\sim
$$

where the [[equivalence relation]] "$\sim$" identifies for every order-preserving [[function]] $[k] \to [l]$ the points $(f_* p,x ) \in \Delta^l_{Top} \times X_l$ and $(p,f^* x) \in \Delta^k_{Top} \times X_k$.

This naturally extends to a [[functor]]

$$
  \vert - \vert : sTop \to Top
  \,.
$$

One also considers geometric realization after restricting to the subcategory $\Delta_+ \hookrightarrow \Delta$ of the [[simplex category]] on the strictly increasing maps. 

+-- {: .num_defn #FatGeometricRealization}
###### Definition

The corresponding [[coend]] in [[Top]] is called the **fat geometric realization** 

$$
  \Vert X_\bullet\Vert :=  \int^{n \in \Delta_+} X_n \times \Delta^n_{Top}
  \,.
$$

=--

This is called _fat_ ,  because it does not [[quotient]] out the [[relation]]s induced by the degeneracy maps and hence is "bigger" than ordinary geometric realization.

Explicitly, this is the [[topological space]] given by the [[quotient]]

$$
  \Vert X_\bullet \Vert = \coprod_{n} \Delta^n_{Top} \times X_n /{\sim_+}
$$

where the [[equivalence relation]] "$\sim_+$" identifies only for every _strictly increasing_ [[function]] $[k] \to [l]$ the points $(f_* p,x ) \in \Delta^l_{Top} \times X_l$ and $(p,f^* x) \in \Delta^k_{Top} \times X_k$.

+-- {: .num_example #GeometricRealizationOfThePoint}
###### Example

The geometric realization of the point -- the [[simplicial topological space]] that is in each degree the 1-point topological space -- is [[homeomorphic]] to the point, but the fat geometric realization of the point is an "infinite dimensional topological ball": the [[terminal object|terminal]] morphism

$$
  \vert * \vert \stackrel{\simeq_{iso}}{\to} *
$$

is an [[isomorphism]], but the morphism

$$
  \Vert * \Vert \stackrel{\simeq_{wh}}{\to} *
$$

is just a [[weak homotopy equivalence]].

=--

## Reminder on nice simplicial topological spaces

Simplicial topological spaces and their geometric realization are in [[homotopy theory]] presentations for certain [[topological ∞-groupoid]]s and intrinsic realization constructions on these. In this context what matters is not the operation of geometric realization itself, but its [[derived functor]]. This is obtained by evaluating ordinary geometric realization on "sufficiently nice" [[resolution]]s of simplicial topological spaces. These we discuss now.

Recall the following definitions and facts from [[nice simplicial topological space]].

+-- {: .num_defn #GoodAndProper}
###### Definition 

Let $X : \Delta^{op} \to Top$ be a [[simplicial topological space]].

Such $X$ is called

* **good** if all the degeneracy maps $X_{n-1} \hookrightarrow X_n$ are all [[closed cofibration]]s;

* **proper** if the inclusion $s X_n \hookrightarrow X_n$ of the degenerate simplices is a [[closed cofibration]], where $s X_n = \bigcup_i s_i(X_{n-1})$.

The last condition equivalently says: 

* $X_\bullet$ is **proper** if it is cofibrant in the [[Reedy model structure]] $[\Delta^{op}, Top_{Strom}]_{Reedy}$ on [[simplicial object]]s in [[Top]] with respect to the [[Strøm model structure]] on [[Top]].

=--

The notion of good simplicial topological space goes back to ([Segal73](#Segal73)), that of proper simplicial topological space to ([May](#May)). 

+-- {: .num_prop}
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
   : 
  Top
    \stackrel{\overset{{|-|}}{\leftarrow}}{\underset{Sing}{\to}} 
  sSet
$$  

for the ordinary [[geometric realization]]/[[singular simplicial complex]] [[adjunction]] (see [[homotopy hypothesis]]).

For $S_{\bullet,\bullet} : \Delta^{op} \times \Delta^{op} \to Set$ a [[bisimplicial set]], write $d S$ for its [[diagonal]] $d X : \Delta^{op} \to \Delta^{op} \times \Delta^{op} \stackrel{S}{\to} Set$.

+-- {: .num_prop}
###### Proposition

Let $X_\bullet$ be a simplicial topological space. 
Then the simplicial topological space 

$$
  |Sing(X_\bullet)| \in [\Delta^{op}, Top]
$$ 

obtained by applying degreewise $|Sing(-)| : Top \to Top$ is good and hence proper. 

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
$(|-| \dashv Sing)$-[[unit of an adjunction|counit]].

=--


+-- {: .num_prop}
###### Proposition

For $X_\bullet$ any [[simplicial topological space]], there is a [[homeomorphism]] between the geometric realization of the simplicial space $|Sing(X_\bullet)|$ and the ordinary [[geometric realization]] of the [[simplicial set]] that is the diagonal of the [[bisimplicial set]] $Sing(X_\bullet)_\bullet$

$$
  \vert(\vert Sing(X_\bullet) \vert)\vert  \simeq_{iso} | d Sing(X_\bullet)_\bullet | 
  \,.
$$

=--

This follows by results in ([Lewis](#Lewis)).




## Properties


### General

+-- {: .num_remark}
###### Remark

We have the following degenerate case of geometric realization of simplicial topological spaces

* If $X_\bullet : \Delta^{op} \to Set \hookrightarrow Top$ is a degreewise [[discrete space]], hence just a [[simplicial set]], the notion of geometric realization above coincides with the notion of [[geometric realization|geometric realization of simplicial sets]].

* If $X_\bulet$ is simplicially constant on a topological space $X_0$, then its geometric realization is [[homeomorphic]] to $X_0$

  $$
    \vert X_\bullet \vert \simeq X_0
    \,.
  $$

=--

Ordinary geometric realization has the following two disadvantages


+-- {: .num_prop}
###### Proposition

* If $X_\bullet$ has in each degree the [[homotopy type]] of a [[CW-complex]], its realization $\vert X_\bullet \vert$ in general need not.

* If a morphism $f : X_\bullet \to Y_\bullet$ is degreewise a [[homotopy equivalence]], its geometric realization $\vert f \vert$ need not be a homotopy equivalence.

=--

See ([Segal74, appendix A](#Segal74))

This is different for the fat geometric realization.

+-- {: .num_prop}
###### Proposition

* If $X_\bullet$ is degreewise of the [[homotopy type]] of a [[CW-complex]], then so is $\Vert X_\bullet \Vert$.

* If $f : X_\bullet \to Y_\bullet$ is degreewise a [[homotopy equivalence]], then also $\Vert f \Vert$ is a homotopy equivalence.

=--

This appears as ([Segal74, prop. A.1](#Segal)).


### Relation between fat and ordinary geometric realization

+-- {: .num_prop}
###### Proposition

If the simplicial topological space $X_\bullet$ is [good](#GoodAndProper) then the natural morphism from its [fat geometric realization](#FatGeometricRealization) to its [ordinary geometric realization](#GeometricRealization) is a [[homotopy equivalence]]

$$
  \Vert X_\bullet \Vert X_\bullet \stackrel{\simeq}{\to} X_\bullet
  \,.
$$

=--

A direct proof of this (not using that good implies proper) appears as ([Segal74, prop. A.1 (iv)](#Segal74)) and a more detailed proof has been given by Tammo tom Dieck.

### Compatibility with limits

We discuss how geometric realization interacts with [[limit]]s of simplicial topological spaces.

#### Ordinary geometric realization

+-- {: .num_prop}
###### Proposition

Geometric realization preserves [[pullback]]s: for $X_\bullet \to Y_\bullet \leftarrow Z_\bullet$ a [[diagram]] in $Top^{\Delta^{op}}$ there are [[natural transformation|natural]] [[homeomorphism]]s

$$
  |X_\bullet| \times_{|Y_\bullet|} |Z_\bullet|
  \simeq
  |X_\bullet \times_{Y_\bullet} Z_\bullet|
  \,.
$$

=--

This appears for instance as ([May, corollary 11.6](#May)). See also the proof that geometric realization of simplicial stes preserves pullbacks, at [[geometric realization]].


#### Fat geometric realization

The operation of [fat geometric realization](#FatGeometricRealization) does not preserve [[fiber product]]s on the nose, in general, but it does preserve all [[finite limit]]s up to [[homotopy]]. 

Write $\Vert * \Vert$ for the fat geometric realization of the point. Notice that due to the identification of $sTop$ with its [[overcategory]] over the point (the simplicial topological space constant on the point), $sTop\simeq sTop/*$, we may regard fat geometric gealization as a functor with values in the [[overcategory]] $Top/\Vert*\Vert$ over the 
[fat geometric realization of the point](#GeometricRealizationOfThePoint).

+-- {: .num_prop}
###### Proposition

The functor

$$
  \Vert - \Vert : Top^{\Delta^{op}} \to Top/\Vert*\Vert
$$

preserves all [[finite limit]]s.

=--

See ([GepnerHenriques, remark 2.23](#GepnerHenriques)).


### Relation to the homotopy colimit

In certain cases geometric realisation computes the [[homotopy colimit]] of the [[diagram9] $X_\bullet : \Delta^{op} \to Top$ given by the simplicial space, with respect to the standard [[model structure on topological spaces]].


+-- {: .num_prop}
###### Proposition

Let $X_\bullet$ be a [[simplicial topological space]]. Then there is a [[natural transformation|natural]] [[weak homotopy equivalence]] 

$$
 \Vert X_\bullet\Vert \simeq hocolim_{n \in \Delta} X_n
$$

from its fat geometric realization to the [[homotopy colimit]] over the simplicial diagram $X : \Delta^{op} \to Top$.

If moreover $X_\bullet$ is [proper](#ProperSimplicialSpace), then the [[natural transformation|natural morphism]]  $ {\Vert X\Vert} \to {|X|}$ is a [[weak homotopy equivalence]], and hence also the ordinary geometric realization is a model for the homotopy colimit.

=-- 

+-- {: .proof}
###### Proof


That the geometric realization of a proper simplicial space is is homotopy colimit follows from the [above fact](#ProperIsReedyCofibrant) that proper spaces are Reedy cofibrant, and using the general statement discussed at [[homotopy colimit]] about description of homotopy colimits by [[coend]]s.

=--

## Related concepts

* [[simplicial topological space]], [[nice simplicial topological space]]

* [[simplicial topological group]]

* **geometric realization of simplicial spaces**



## References

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

A proof that good simplicial spaces are proper is in

* L. Gaunce Lewis Jr., _When is the natural map $X\to \Omega \Sigma X$ a cofibration?_ , Trans. Amer. Math. Soc. **273** (1982) no. 1, 147--155 ([JSTOR](http://www.jstor.org/pss/1999197))
{#Lewis}

A generalization of the statement that good implies proper to other [[topological concrete categories]] and a discussion of the geometric realization of $W G \to \bar W G$ for $G$ a [[simplicial topological group]]  is in 

* [[David Roberts]], [[Danny Stevenson]], _Simplicial principal bundles in parametrized spaces_
{#RobertsStevenson}

Comments on the relation between properness and cofibrancy in the [[Reedy model structure]] on $[\Delta^{op}, Set]$ are made in 

* [[Paul Goerss]], [[Kristen Schemmerhorn]], _Model Categories and Simplicial Methods_ ([arXiv:math.AT/0609537](http://arxiv.org/abs/math.AT/0609537)).

The geometric realization of ([[nerve]]s of) [[topological groupoid]] is discussed in section 2.3 of

* [[David Gepner]], [[André Henriques]], _Homotopy theory of orbispaces_ ([pdf](http://www.math.uni-muenster.de/sfb/about/publ/heft448.pdf))
{#GepnerHenriques}


## Refereeing

This entry is under review. See <a href="http://ncatlab.org/nlabreviewed/published/geometric+realization+of+simplicial+topological+spaces">geometric realization of simplicial topological spaces</a> at [[nlabreviewed:HomePage|nLab (reviewed)]].


[[!redirects geometric realization of a simplicial space]]
[[!redirects geometric realization of simplicial spaces]]

[[!redirects fat geometric realization of simplicial spaces]]
[[!redirects fat geometric realization of simplicial topological spaces]]

[[!redirects fat realization]]