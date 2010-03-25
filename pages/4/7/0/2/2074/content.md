
<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

The [[model category]] structure on the [[category]] $SSet^+/S$ of [[marked simplicial set]]s over a given [[simplicial set]] $S$ is a [[presentable (infinity,1)-category|presentation]] for the [[(∞,1)-category]] of [[Cartesian fibration]]s over $S$.
Every object is cofibrant and the fibrant objects of $SSet^+/S$ are precisely the [[Cartesian fibration]]s over $S$.

Notably for $S = {*}$ this is a presentation of the [[(∞,1)-category of (∞,1)-categories]]: as a plain [[model category]] this is [[Quillen equivalence|Quillen equivalent]] to the [[model structure for quasi-categories]], but it is indeed an $sSet_{Quillen}$-[[enriched model category]] (i.e. enriched over the ordinary [[model structure on simplicial sets]] that models [[∞-groupoid]]s).


The $(\infty,1)$-categorical [[Grothendieck construction]] that exhibits the correspondence between [[Cartesian fibration]]s and [[(∞,1)-presheaf|(∞,1)-presheaves]] is in turn modeled by a [[Quillen equivalence]] between the model structure on marked simplicial over-sets and the projective [[global model structure on simplicial presheaves]].















## Marked simplicial sets



Marked simplicial sets are [[simplicial set]]s with a little bit of extra [[stuff, structure, property|structure]]: a marking that remembers which edges are supposed to be [[Cartesian morphism]]s. 


### Definition 

+-- {: .un_def }
###### Definition 


A **marked simplicial set** is 

* a pair $(S,E)$ consisting of 

  * a [[simplicial set]] $S$ 

  * and a subset $E \subset S_1$ of edges of $S$, called the _marked edges_, 

* such that

  * all degenerate edges are marked edges.

A morphism $(S,E) \to (S',E')$ of marked simplicial sets is a morphism $f : S \to S'$ of [[simplicial set]]s that carries marked edges to marked edges in that $f(E) \subset E'$.

=--

+-- {: .un_def }
###### Notation

* The category of marked simplicial sets is denoted $sSet^+$.

* for $S$ a [[simplicial set]] let

  * $S^\flat$ or $S^{min}$ be the minimally marked simplicial set: only the degenerate edges are marked;

  * $S^#$ or $S^{max}$ be the maximally marked simplicial set: every edges is marked.

* for $p : X \to S$ a [[Cartesian fibration]] of [[simplicial set]]s let

  * $X^\sharp$ or $X^{cart}$ be the cartesian marked simplicial set: precisely the $p$-[[cartesian morphism]]s are marked

* For $X$ and $Y$ marked simplicial sets let

  * $Map^\flat(X,Y)$ be the [[simplicial set]] underlying the [[cartesian closed category|cartesian]] [[internal hom]] $Y^X$

  * $Map^#(X,Y)$ the simplicial set consisting of all simplices $ \sigma \in Map^\flat(X,Y)$ such that every edge of $\sigma$ is a marked edge of $Y^X$.

  Equivalently these mapping complexes are characterized by the
  fact that we have natural bijections

  $$
    Hom_{sSet}(K, Map^\flat(X,Y)) \simeq 
    Hom_{sSet^+}(K^\flat \times X, Y)
  $$

  $$
    Hom_{sSet}(K, Map^#(X,Y)) \simeq Hom_{sSet^+}(K^# \times X, Y)
    \,.
  $$

=--

### Properties

+-- {: .un_prop }
###### Proposition

The category of marked simplicial sets is [[cartesian closed]]. 

* The $n$-simplices of the internal hom $Y^X$ are simplicial maps $X \times \Delta^n \rightarrow Y$ such that when you restrict $X_1 \times \Delta_1^n \rightarrow Y_1$ to $E \times \Delta_0^n$ (where $E$ is the set of marked edges of $X$), this morphism factors through the marked edges of $Y$.

* The marked edges of $Y^X$ are those simplicial maps $X \times \Delta^1 \rightarrow Y$ such that the restriction of $X_1 \times \Delta_1^1 \rightarrow Y_1$ to $E \times \Delta^1_1$ factors though the marked edges of $Y$. In the presence of the previous condition, this says that when you apply the homotopy $X \times \Delta^1 \rightarrow Y$ to a marked edge of $X$ paired with the identity at $[1]$, the result should be marked.

There are functors 
$$
  \array{ 
    & \stackrel{(-)^{\flat}}{\to} & 
    \\ 
    & \stackrel{(-)^{\flat}}{\leftarrow} & 
    \\ 
    sSet & \stackrel{(-)^{\sharp}}{\to} & sSet^+ 
    \\ 
    & \stackrel{(-)^{\sharp}}{\leftarrow} & 
  }
$$
 
with $(-)^{\flat} \dashv (-)^{\flat} \dashv (-)^{\sharp} \dashv (-)^{\sharp}$.

* The hom-objects $Map^#(X,Y)$ make $sSet^+$ an 
  [[sSet]]-[[enriched category]].

=--






+-- {: .un_remark }
###### Remark (HTT, 3.1.4.5)

When instead using as hom-objects

$$
  hom(X,Y) := Map_S^\flat(X,Y)
$$

then one obtains an $sSet_{Joyal}$-[[enriched model category]] (enriched over the [[model structure for quasi-categories]]). This models the full [[(∞,2)-category]] of cartesian fibrations of [[(∞,1)-categories]].

=--



+-- {: .un_remark }
###### Remark (HTT, 3.1.3.1)

For $(X \to S) \in SSet^+/S$ and $p : Y \to S$ a [[Cartesian fibration]] we have

* $Map^\flat_S(X,Y^{cart})$ is a [[quasi-category]]

* $Map^#_S(X,Y^{cart})$ is the largest [[Kan complex]] in $Map^\flat_S(X,Y^{cart})$

=--


## Model structure on marked simplicial sets


### Definition

The **model structure on marked simplicial over-sets** $Set^+/S$ over $S \in SSet$ -- also called the **Cartesian model structure** since it models [[Cartesian fibration]]s -- is defined as follows.


+-- {: .un_def }
###### Definition/Proposition
**(Cartesial model structure on $sSet^+/S$)**

The category $SSet^+/S$ of [[marked simplicial set]]s over a marked simplicial set $S$ carries a structure of a [[proper model category|proper]] [[combinatorial simplicial model category]] defined as follows.

The [[SSet]]-[[enriched category|enrichment]] is given by 

$$
  hom(X,Y) := Map_S^#(X,Y)
  \,.
$$

A morphism $f : X \to X'$ in $SSet^+/S$ of [[marked simplicial set]]s is 

* a _cofibration_ if the underlying morphism of [[simplicial set]]s is a cofibration in the standard [[model structure on simplicial sets]] (i.e. a [[monomorphism]]).

  (def. 3.1.2.2 of [[Higher Topos Theory|HTT]])

* a weak equivalence if it is a **Cartesian equivalence**, namely such that for every [[cartesian fibration]] $Z \to S$ we have that

  * the induced morphism $Map_S^\flat(Y,Z^{cart}) \to Map_S^\flat(X,Z^{cart})$ is  an [[equivalence of quasi-categories]]

  * or equivalently: the induced morphism $Map_S^#(Y,Z^{cart}) \to Map_S^#(X,Z^{cart})$ is a [[model structure on simplicial sets|equivalence of Kan complexes]].


* a fibration if it has the right [[lifting property]] with respect to all acyclic cofibrations.

(Recall that $Map_S^#(X,Z^{cart})$ is the maximal [[Kan complex]] in $Map_S^\flat(X,Z^{cart})$.)

=--


+-- {: .proof}
###### Proof

The model structure is proposition 3.1.3.7 in [[Higher Topos Theory|HTT]]. The simplicial enrichment is corollary 3.1.4.4.

=--

+-- {: .un_def }
###### Definition/Proposition
**(coCartesial model structure on $sSet^+/S$)**

There is another such model structure, with [[Cartesian fibration]]s replaced everywhere by **coCartesian fibrations.

=--



### As a model for the $(\infty,1)$-category of $(\infty,1)$-categories

The Joyal [[model structure for quasi-categories]] $sSet_{Joyal}$ is an [[enriched category]] enriched over itself. So it is _not_ a [[simplicial model category]] in the standard sense, which means $sSet_{Quillen}$-enriched.

Indeed, the full sSet-enriched subcategory $(sSet_{Joyal})^\circ$ on fibrant-cofibrant objects is a model for the [[(∞,2)-category]] [[(∞,1)Cat]] of [[(∞,1)-categories]]. For many applications it is more convenient to work just with the [[(∞,1)-category of (∞,1)-categories]] inside that, obtained by taking in each [[hom-object]] [[quasi-category]] the maximal [[Kan complex]].

The resulting [[(∞,1)-category]] should have a presentation by a [[simplicial model category]]. And the model structure on marked simplicial sets does accomplish this.

### Properties


+-- {: .un_defn}
###### Definition ([[Higher Topos Theory|HTT, Def 3.1.1.1]])


The collection of **marked anodyne morphisms** in $SSet^+/S$ is the class of morphisms $An^+ = LLP(RLP(An^+_0))$ where the generating set $An^+_0$ consists of

* for $0 \lt i \lt n $ the minimally marked [[horn]] inclusions

  $$
    (\Lambda[n]_i)^\flat \to \Delta[n]^\flat
  $$

* for $i = n$ the horn inclusion with the last edge markeed:

  $$
    (\Lambda[n]_i, \mathcal{E} \cap (\Lambda[n]_i)_1)
    \to 
    (\Delta[n], \mathcal{E} )    
    \,,
  $$
  
  where $\mathcal{E}$ is the union of all degenete edges in $\Delta[n]$ together with the edge $\Delta^{\{n-1,n\}} \to \Delta[n]$.


* the inclusion

  $$
    (\Lambda[2]_1)^\sharp \coprod_{(\Lambda[2]_1)^\flat}
    (\Delta[2])^\flat
    \to
    (\Delta[2])^\sharp
    \,.
  $$

* for every [[Kan complex]] $K$ the morphism $K^\flat \to K^#$.

=--

+-- {: .un_prop}
###### Proposition (HTT, prop. 3.1.1.6)


A morphism $p : X \to S$ in $SSet^+$ has the [[right lifting property]] with respect to the class $An^+$ of marked anodyne maps precisely if

1. $p$ is an [[inner fibration]]

1. an edge $e$ of $X$ is marked precisely if it is a [[Cartesian morphism]] and $p(e)$ is marked in $S$

1. for every object $y$ of $X$ and every marked edge $\bar e : \bar x \to p(y)$ in $S$ there exists a marked edge $e : x \to y$ of $X$ with $p(e) = \bar e$.

=--

+-- {: .un_remark}
###### Remark (HTT, prop. 3.1.3.4)

Every morphism $f : X \to Y$ in $SSet^+/S$ whose underlying morphism in $SSet^+$ is marked anodyne is a Cartesian equivalence.

=--
  
## References 

Marked simplicial sets are introduced in section 3.1 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

The model structure on marked simplicial oversets is described in section 3.1.3


[[!redirects marked simplicial set]]
[[!redirects marked simplicial sets]]
[[!redirects model structure for coCartesian fibrations]]
[[!redirects model structure on marked simplicial over-sets]]
[[!redirects model structure on marked simplicial oversets]]
