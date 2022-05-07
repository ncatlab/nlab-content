
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

[[Arne Strom|Arne Strøm]] proved that the [[category]] [[Top]] of *all* [[topological spaces]] has a structure of a Quillen [[model category]] where 

* fibrations are [[Hurewicz fibrations]], 

* cofibrations are *closed* [[Hurewicz cofibrations]] 

* and the role of weak equivalences is played by (strong) [[homotopy equivalences]]

  (as opposed to the [[weak homotopy equivalences]] of the "standard" [[Quillen model structure on topological spaces]]).

The theorem might have been a [[folklore]] at the time, but the paper ([Strøm 1972](#Strom72)) has a number of subtleties.

Strøm's proofs are not that well-known today and use techniques better known to the topologists of that time, and there is consequently a slight controversy among topologists now.  One of these is that there are modern reproofs, but these modern techniques essentially use [[compactly generated spaces]], while Strøm's proofs succeeded in avoiding that assumption. 

However, for many applications nowadays, one is mainly interested in the analogous model structure on the category of [[k-spaces]], or of [[compactly generated space]]s ([[weak Hausdorff space|weak Hausdorff]] [[k-spaces]]).  Note that any cofibration in the latter category is closed.


## Properties

### General

+-- {: .num_prop}
###### Observation

In the Strøm model structure, _every_ object is both a [[fibrant object]] and a [[cofibrant object]].

=--

This is a most rare property for a non-trivial model structure. 
 
### Monoidal structure

The Strøm model structure on the category of [[compactly generated spaces]] is a [[monoidal model category]].  This is proven in section 6.4 of [[A Concise Course in Algebraic Topology]] (without that language) using the fact that a subspace inclusion is a Hurewicz cofibration if and only if it is an [[NDR-pair]].

### Quillen adjunctions
 {#QuillenAdjunctions}

The [[identity functor]] $id \colon Top \to Top$ is [[Quillen adjunction|left Quillen]] from the [[classical model structure on topological spaces]] (or the mixed model structure) to the Strøm model structure, and of course right Quillen in the other direction.  

$$
  Top_{Strom}
    \stackrel{\overset{id}{\longleftarrow}}{\underset{id}{\longrightarrow}}
  Top_{Quillen}
  \,.
$$


This is just the observation that any [[Hurewicz fibration]] is a [[Serre fibration]], and any [[homotopy equivalence]] is a [[weak homotopy equivalence]]---or dually, that any [[retract]] of a [[relative cell complex]] inclusion is a Hurewicz cofibration.

It follows, by composition, that the ([[geometric realization]] $\dashv$ [[singular simplicial complex]])-[[adjunction]] $ {\vert-\vert} \colon sSet \leftrightarrows Top \colon Sing$ is a [[Quillen adjunction]] between the [[classical model structure on simplicial sets]] and the Strøm model structure.

$$
  Top_{Strom}
    \stackrel{\overset{id}{\longleftarrow}}{\underset{id}{\longrightarrow}}
  Top_{Quillen}
    \stackrel{\overset{{\vert-\vert}}{\longleftarrow}}{\underset{Sing}{\longrightarrow}}
  sSet_{Quillen}
  \,.
$$


### Simplicial structure

If $Top$ denotes the category of [[compactly generated space]]s, then [[geometric realization]] $ {|-|} \colon sSet \to Top$ preserves finite [[products]], and hence is a [[strong monoidal functor]].  Therefore, in this case the adjunction ${|-|} \dashv Sing$ is a [[strong monoidal Quillen adjunction]], and hence makes the Strøm model structure into a [[simplicial model category]].

### Geometric realization is a Reedy cofibrant replacement

Write $({\vert- \vert} \dashv Sing) : Top\stackrel{\overset{{|-|}}{\leftarrow}}{\underset{Sing}{\to}} $ [[sSet]] for the ordinary [[geometric realization]]/[[singular simplicial complex]] [[adjunction]] (see [[homotopy hypothesis]]).

For $S_{\bullet,\bullet} : \Delta^{op} \times \Delta^{op} \to Set$ a [[bisimplicial set]], write $d S$ for its [[diagonal]] $d X : \Delta^{op} \to \Delta^{op} \times \Delta^{op} \stackrel{S}{\to} Set$.

+-- {: .num_prop}
###### Proposition

For $X_\bullet$ any [[simplicial topological space]], there is a [[homeomorphism]] between the [[geometric realization of simplicial topological spaces|geometric realization]] of the 
[[simplicial topological space]] $[n] \mapsto |Sing(X_n)|$ and the ordinary [[geometric realization]] of the [[simplicial set]] that is the diagonal of the [[bisimplicial set]] $Sing(X_\bullet)_\bullet$

$$
  \left|[n] \mapsto |Sing(X_n)|\right|  \simeq_{iso} | d Sing(X_\bullet)_\bullet | 
  \,.
$$

Moreover, the degreewise $(|-| \dashv Sing)$-[[unit of an adjunction|counit]] yields a morphism

$$
 ([n] \mapsto |Sing(X_n)|) \to X_\bullet
$$

and this is a cofibrant [[resolution]] in the [[Reedy model structure]]  $[\Delta^{op}, Top_{Strom}]_{Reedy}$ relative to the Str&#248;m model structure. 

=--

See [[geometric realization of simplicial topological spaces]] for more details.

## Related concepts

* [[homotopy hypothesis]]

* [[model structure on topological spaces]]

  * [[classical model structure on topological spaces]]

    * [[classical model structure on pointed topological spaces]]

  * [[Strøm model structure]]

  * [[model structure on Delta-generated topological spaces]]


* [[model structure on simplicial sets]], [[model structure on topological spaces]]

* [[Thomason model structure]]

* [[Hurewicz model structure on chain complexes]]



## References

The model structure was originally established in

* {#Strom72} [[Arne Strøm]], _The homotopy category is a homotopy category_, Archiv der Mathematik 23 (1972) ([pdf](https://www.uio.no/studier/emner/matnat/math/MAT9580/v17/documents/strom-the-homotopy-category-is-a-homotopy-category-1972.pdf), [[Strom_HomotopyCategory.pdf:file]])

using results on [[Hurewicz cofibrations]] from:

* [[Arne Strøm]], _Note on cofibrations_,  Math. Scand.  **19** (1966) 11-14 ([jstor:24490229](https://www.jstor.org/stable/24490229), [dml:165952](https://eudml.org/doc/165952), MR0211403)

* [[Arne Strøm]], _Note on cofibrations II_,  Math. Scand.  **22** (1968) 130--142 (1969) ([jstor:24489730](https://www.jstor.org/stable/24489730), [dml:166037](https://eudml.org/doc/166037), MR0243525)

A new proof using [[algebraic weak factorization systems]], and  its generalization to any [[bicomplete category]] which is [[power|powered]], [[copower|copowered]] and [[enriched category|enriched]] in [[TopSp]] is due to:

* {#BarthelRiehl13} [[Tobias Barthel]], [[Emily Riehl]], _On the construction of functorial factorizations for model categories_, Algebr. Geom. Topol. 13 (2013) 1089-1124 ([arXiv:1204.5427](http://arxiv.org/abs/1204.5427), [doi:10.2140/agt.2013.13.1089](http://dx.doi.org/10.2140/agt.2013.13.1089), [euclid:agt/1513715550](https://projecteuclid.org/euclid.agt/1513715550))
 
Beware that a proof of the Strøm model structure was also claimed in 

* [[Peter May|May]], [[Johann Sigurdsson|Sigurdsson]], *[[Parametrized Homotopy Theory]]*, 

but relying on

* {#Cole06} [[Michael Cole]], Prop. 5.3 in *Many homotopy categories are homotopy categories*, Topology and its Applications 153 (2006) 1084–1099 ([doi:10.1016/j.topol.2005.02.006](https://doi.org/10.1016/j.topol.2005.02.006))

* {#MayPonto12} [[Peter May]], [[Kate Ponto]], Lemma 17.1.7 in: *[[More concise algebraic topology]] -- Localization, Completion, and Model Categories*, University of Chicago Press (2012) ([ISBN:9780226511795](https://press.uchicago.edu/ucp/books/book/chicago/M/bo12322308.html), [pdf](https://www.math.uchicago.edu/~may/TEAK/KateBookFinal.pdf))

which later was noticed to be false, by [[Richard Williamson]], see [Barthel & Riehl, p. 2 and Rem 5.12 and Sec. 6.1](#BarthelRiehl13) for details. 



[[!redirects Strøm's model category]]
[[!redirects Strom's model category]]
[[!redirects Strøm's model category]]
[[!redirects Strom's model category]]
[[!redirects Strøm model category]]
[[!redirects Strom model category]]
[[!redirects Strøm's model structure]]
[[!redirects Strom's model structure]]
[[!redirects Strøm's model structure]]
[[!redirects Strom's model structure]]
[[!redirects Strøm model structure]]
[[!redirects Strom model structure]]
[[!redirects Hurewicz model structure]]
[[!redirects h-model structure]]
