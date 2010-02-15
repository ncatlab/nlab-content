
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

The [[model category]] structure on the [[category]] $SSet^+/S$ of [[marked simplicial set]]s sitting over a given [[simplicial set]] $S$ is a [[presentable (infinity,1)-category|presentation]] for the [[(∞,1)-category]] of [[cartesian fibration]]s over $S$.

Notably for $S = {*}$ this is a presentation of the [[(∞,1)-category of (∞,1)-categories]]: as a plain [[model category]] this is [[Quillen equivalence|Quillen equivalent]] to the [[model structure for quasi-categories]], but it is indeed an $sSet_{Quillen}$-[[enriched model category]] (i.e. enriched over the ordinary [[model structure on simplicial sets]] that models [[∞-groupoid]]s).


The $(\infty,1)$-categorical [[Grothendieck construction]] that exhibits the correspondence between [[Cartesian fibration]]s and [[(∞,1)-presheaf|(∞,1)-presheaves]] is in turn modeled by a [[Quillen equivalence]] between the model structure on marked simplicial over-sets and the projective [[global model structure on simplicial presheaves]].


## Definition 

### Marked simplicial over-sets 

Let $S$ be a fixed [[simplicial set]]. Recall from the notation at [[marked simplicial set]] that $S^#$ denotes the maximally marked simplicial set of $S$ where all edges are marked edges.
 
Write $SSet^+/S^#$ -- or $SSet^+/S$ for short -- for the [[over category]] of the category $Set^+$ of marked simplicial sets over $S^#$.

Recall the notation from [[marked simplicial set]]. For $X$ and $Y$ in $Set^+_S$ write $Map^\flat_S(X,Y) \subset Map^\flat(X,Y)$ and $Map^#_S(X,Y) \subset Map^#(X,Y)$ for the simplicial subsets of maps compatible with the maps to $S$.

+-- {: .un_remark }
###### Remark

For $X \in SSet^+/S$ abd $p : Y \to X$ a [[cartesian fibration]] we have

* $Map^\flat_S(X,Y^{cart})$ is a [[quasi-category]]

* $Map^#_S(X,Y^{cart})$ is the largest [[Kan complex]] in $Map^\flat_S(X,Y^{cart})$

=--



### The model structure 

The **model structure on marked simplicial over-sets** $Set^+/S$ over $S \in SSet$ -- also called the **Cartesian model structure** since it models [[cartesian fibration]]s -- is defined as follows.


A morphism $f : X \to X'$ in $SSet^+/S$ of [[marked simplicial set]]s is 

* a _cofibration_ if the underlying morphism of [[simplicial set]]s is a cofibration in the standard [[model structure on simplicial sets]] (i.e. a [[monomorphism]]).

  (def. 3.1.2.2 of [[Higher Topos Theory|HTT]])

* a weak equivalence if it is a **Cartesian fibration**, namely such that for every [[cartesian fibration]] $Z \to S$ we have that

* the induced morphism $Map_S^\flat(Y,Z^{cart}) \to Map_S^\flat(X,Z^{cart})$ is  an [[equivalence of quasi-categories]]

  * or equivalently: the induced morphism $Map_S^#(Y,Z^{cart}) \to Map_S^#(X,Z^{cart})$ is a [[model structure on simplicial sets|homotopy equivalence]] of [[Kan complex]]es.


* a fibration if it has the right [[lifting property]] with respect to all acyclic cofibrations.

(Recall that $Map_S^#(X,Z^{cart})$ is the maximal [[Kan complex]] in $Map_S^\flat(X,Z^{cart})$.)


+-- {: .un_prop }
###### Proposition

This defines a [[proper model category|proper]] [[combinatorial simplicial model category]].

=--

+-- {: .proof}
###### Proof

This is proposition 3.1.3.7 in [[Higher Topos Theory|HTT]].

=--


## References 

section 3.1.3 of

* [[Jacob Lurie]], [[Higher Topos Theory]]
