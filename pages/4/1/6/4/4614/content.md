
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

For $X_\bullet$ a [[simplicial object]] in [[Top]] --  a [[simplicial topological space]] -- its _[[geometric realization]]_ is a plain [[topological space]] $|X_\bullet| \in Top$ whose construction is a direct analog of the ordinary notion of [[geometric realization]] of a [[simplicial set]], but taking into account the topology on the spaces of $n$-simplices $X_n$.

## Definition

Let [[Top]] in the following denote the [[category]] of [[compactly generated space|compactly generated]] [[weakly Hausdorff space]]s or the category of [[k-space]]s.

Write $\Delta_{Top} : \Delta \to Top : [n] \mapsto \Delta^n_{Top}$ for the standard [[cosimplicial object|cosimplicial]] [[topological space]] of topological [[simplices]].


+-- {: .un_def}
###### Definition

For $X_\bullet : \Delta^{op} \to Top$ [[simplicial topological space]], its **geometric realization** is the [[coend]]

$$
  |X_\bullet| :  \int^{n \in \Delta} X_n \times \Delta^n_{Top}
$$

formed in [[Top]].

=--

More explicitly, this is the [[topological space]] given by the [[quotient]]

$$
  |X_\bullet| = \coprod_{n} \Delta^n_{Top} \times X_n /\sim
$$

where the [[equivalence relation]] "$\sim$" identifies for every order-preserving [[function]] $[k] \to [l]$ the points $(f_* p,x ) \in \Delta^l_{Top} \times X_l$ and $(p,f^* x) \in \Delta^k_{Top} \times X_k$.

This naturally extends to a [[functor]]

$$
  |-| : Top^{\Delta^{op}} \to Top
  \,.
$$

One also considers geometric realization after restricting to the subcategory $\Delta_+ \hookrightarrow \Delta$ of the [[simplex category]] on the strictly increasing maps. 

+-- {: .un_def}
###### Definition

The corresponding [[coend]] is called the **fat geometric realization** 

$$
  \Vert X_\bullet\Vert :  \int^{n \in \Delta_+} X_n \times \Delta^n_{Top}
  \,.
$$

=--

(Fat, because it does not [[quotient]] out the [[relation]]s induced by the degeneracy maps and hence is "bigger" than ordinary geometric realization).

More explicitly, this is the [[topological space]] given by the [[quotient]]

$$
  |X_\bullet| = \coprod_{n} \Delta^n_{Top} \times X_n /\sim
$$

where the [[equivalence relation]] "$\sim$" identifies only for every _strictly increasing_ [[function]] $[k] \to [l]$ the points $(f_* p,x ) \in \Delta^l_{Top} \times X_l$ and $(p,f^* x) \in \Delta^k_{Top} \times X_k$.

+-- {: .un_prop}
###### Example

The geometric realization of the point -- the [[simplicial topological space]] that is in each degree the 1-point topological space -- is [[homeomorphic]] to the point, but the fat geometric realization of the point is the "infinite dimensional topological ball": the morphism

$$
  \vert * \vert \stackrel{\simeq_{iso}{\to} *
$$

is an [[isomorphism]], but the morphism

$$
  \Vert * \Vert \stackrel{\simeq_{wh}}{\to} *
$$

is just a [[weak homotopy equivalence]].

=--

## Properties


### General

+-- {: .un_lemma}
###### Observation

If $X_\bullet : \Delta^{op} \to Set \hookrightarrow Top$ is a degreewise [[discrete space]], hence just a [[simplicial set]], the notion of geometric realization above coincided with the notion of [[geometric realization|geometric realization of simplicial sets]].

=--

### Compatibility with limits

#### Ordinary geometric realization

+-- {: .un_prop}
###### Proposition

Geometric realization preserves [[pullback]]s: for $X_\bullet \to Y_\bullet \leftarrow Z_\bullet$ a [[diagram]] in $Top^{\Delta^{op}}$ there are [[natural transformation|natural]] [[homeomorphism]]s

$$
  |X_\bullet| \times_{|Y_\bullet|} |Z_\bullet|
  \simeq
  |X_\bullet \times_{Y_\bullet} Z_\bullet|
  \,.
$$

=--

For instance ([May, corollary 11.6](#May)).

Write $({\vert- \vert} \dashv Sing) : Top\stackrel{\overset{{|-|}}{\leftarrow}}{\underset{Sing}{\to}} sSet$ for the ordinary [[geometric realization]]/[[singular simplicial complex]] adjunction (see [[homotopy hypothesis]]).

For $S_{\bullet,\bullet} : \Delta^{op} \times \Delta^{op} \to Set$ a [[bisimplicial set]], write $d S$ for its [[diagonal]] $d X : \Delta^{op} \to \Delta^{op} \times \Delta^{op} \stackrel{S}{\to} Set$.

+-- {: .un_prop}
###### Proposition

For $X_\bullet$ any [[simplicial topological space]], there is a [[homeomorphism]] between the geometric realization of the simplicial space $|Sing(X_\bullet)|$ and the ordinary [[geometric realization]] of the [[simplicial set]] that is the diagonal of the [[bisimplicial set]] $Sing(X_\bullet)_\bullet$

$$
  |Sing(X_\bullet)|  \simeq_{iso} | d Sing(X_\bullet)_\bullet | 
  \,.
$$

=--

#### Fat geometric realization

The fat geometric realization does not preserve fiber products on the nose, in general, but it does preserve all [[finite limit]]s up to [[homotopy]]. 

Write $\Vert * \Vert$ for the fat geometric realization of the point. Notice that due to the identification of [[Top]]${\Delta}^{op}$ with its [[overcategory]] over the point (the simplicial topological space constant on the point), $Top^{\Delta^{op}} \simeq Top^{\Delta^{op}}/*$, we may regard fat geometric gealization as a functor

$$
  \Vert - \Vert : Top^{\Delta^{op}} \to Top/\Vert*\Vert
  \,.
$$

+-- {: .un_prop}
###### Proposition

The functor

$$
  \Vert - \Vert : Top^{\Delta^{op}} \to Top/\Vert*\Vert
$$

preserves all [[finite limit]]s.

=--

See ([GepnerHenriques, remark 2.23]).

### Relation to the homotopy colimit

In certain cases geometric realisation computes the [[homotopy colimit]] of the diagram $X_\bullet : \Delta^{op} \to Top$ given by the simplicial space, with respect to the standard [[model structure on topological spaces]].

#### Nice simplicial topological spaces

Recall the following definitions and facts from [[nice simplicial topological space]].

+-- {: .un_defn #GoodSimplicialSpace}
###### Definition 

A [[simplicial topological space]] $X_\bullet$ is **good** in the sense of [[Graeme Segal|Segal]] if all the degeneracy maps $X_{n-1} \hookrightarrow X_n$ are closed cofibrations.

=--

+-- {: .un_defn #ProperSimplicialSpace}
###### Definition

A simplicial topological space $X_\bullet$ is **proper** in the sense of [May,def. 11.2](#May) if the inclusion $s X_n \hookrightarrow X_n$ of the degenerate simplices is a [[Hurewicz cofibration|closed cofibration]], where $s X_n := \bigcup_i s_i(X_{n-1})$.

=--


For more on these conditions see [[nice simplicial topological space]].

+-- {: .un_prop}
###### Proposition

A good simplicial topological space is proper.

=--

A proof appears as [Lewis, corollary 2.4 (b)](#Lewis). A generalization of this result is in [RobertsStevenson](#RobertsStevenson).

+-- {: .un_prop #ProperIsReedyCofibrant}
###### Proposition

The proper simplicial topological spaces are precisely those that are cofibrant in the [[Reedy model structure]] $[\Delta^{op}, Top_{Str}]_{Reedy}$ on simplicial topological spaces, where [[Top]] is equipped with the [[Strøm model structure]] $Top_{Strm}$.

=--

+-- {: .un_prop}
###### Proposition

For $X_\bullet$ any simplicial topological space, then ${|Sing X_\bullet|}$ is proper and the natural morphism

$$
  {|Sing X_\bullet|} \to X_\bullet
$$

is a cofibrant [[resolution]] of $X_\bullet$ in $[\Delta^{op},Top_{Strm}]_{Reedy}$.


=--

This follows by results in ([Lewis](#Lewis)).


#### Models for the homotopy colimit

+-- {: .un_prop}

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

+-- {: .un_remark}
###### Remark

In the case $X_\bullet$ that is a [good](#GoodSimplicialSpace) [[simplicial topological space]], a direct (i.e., not using the fact that goodness implies properness) a proof that $ \Vert X\Vert  \to |X|$ is a weak homotopy equivalence has been sketched by [[Graeme Segal]] and then refined by Tammo tom Dieck.

=--

## Related concepts

* [[simplicial topological space]], [[nice simplicial topological space]]

* [[simplicial topological group]]

* **geometric realization of simplicial spaces**



## References

An original reference is

* [[Graeme Segal]], _Categories and cohomology theories_ Topology, 13:293&#8211;312, 1974

A standard textbook reference is chapter 11 of

* [[Peter May]], _The geometry of iterated loop spaces_ ([pdf](http://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))
{#May}

A proof that good simplicial spaces are proper is in

* L. Gaunce Lewis Jr., _When is the natural map $X\to \Omega \Sigma X$ a cofibration?_ , Trans. Amer. Math. Soc. **273** (1982) no. 1, 147--155 ([JSTOR](http://www.jstor.org/pss/1999197))
{#Lewis}

A generalization of the statement that good implies proper to other [[topological concrete categories]] is in 

* [[David Roberts]], [[Danny Stevenson]], unpublished notes
{#RobertsStevenson}

Comments on the relation between properness and cofibrancy in the [[Reedy model structure]] on $[\Delta^{op}, Set]$ are made in 

* [[Paul Goerss]], [[Kristen Schemmerhorn]], _Model Categories and Simplicial Methods_ ([arXiv:math.AT/0609537](http://arxiv.org/abs/math.AT/0609537)).

The geometric realization of ([[nerve]]s of) [[topological groupoid]] is discussed in section 2.3 of

* [[David Gepner]], [[Andre Henriques]], _Homotopy theory of orbispaces_ ([pdf](http://www.math.uni-muenster.de/sfb/about/publ/heft448.pdf))
{#GepnerHenriques}


## Refereeing

This entry is under review. See <a href="http://ncatlab.org/nlabreviewed/published/geometric+realization+of+simplicial+topological+spaces">geometric realization of simplicial topological spaces</a> at [[nlabreviewed:HomePage|nLab (reviewed)]].


[[!redirects geometric realization of a simplicial space]]
[[!redirects geometric realization of simplicial spaces]]

[[!redirects fat geometric realization of simplicial spaces]]
[[!redirects fat geometric realization of simplicial topological spaces]]

[[!redirects fat realization]]