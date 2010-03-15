

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **model structure for right fibrations** $(SSet/S)_{rfib}$ is a [[model category]] structure on the [[overcategory]] $SSet/S$ of [[simplicial set]]s over a given [[quasi-category]] $S$, that [[presentable (∞,1)-category|presents]] the [[(∞,1)-category]] of [[right Kan fibration]]s [[fibrations of quasi-categories|of quasi-categories]] over $S$

$$
  ((SSet/S)_{rfib})^\circ \simeq RFib(S)
  \,.
$$

This is the $(\infty,1)$-analog of the $(2,1)$-category $Fib_{grpd}(S)$ of [[category fibered in groupoids|categories fibered in groupoids]] over a category $S$.

Similarly there is an analogous **model structure for left fibrations** that models [[left Kan fibration]]s, i.e.  op-fibrations in [[∞-groupoid]]s

$$
  ((SSet/S)_{lfib})^\circ \simeq LFib(S)
  \,.
$$

The extension of this from right fibrations to [[Cartesian fibration]]s and from left fibrations to [[coCartesian fibration]]s is the [[model structure for coCartesian fibrations]].

The [[(∞,1)-Grothendieck construction]] relates this to the [[global model structure on functors]] that presents the [[(∞,1)-category of (∞,1)-functors]] $Fun(S,\infty Grpd)$ (for left fibrations) and $Fun(S^{op},\infty Grpd)$ (for right fibrations).

## Motivation {#Motivation}

The following [[model category]] structure is best understood with the [[(∞,1)-Grothendieck construction]] in mind, which it serves to model.

Recall from the discussion there that given a morphism $p : X \to S$ of [[quasi-categories]], the [[(∞,1)-functor]] $S^{op} \to \infty Grpd$ that the left adjoint to the Grothendieck construction extracts from it is all encoded in the [[pushout]] $X^{\triangleleft} \coprod_X S$ in

$$
  \array{
    X &\stackrel{p}{\to}& S
    \\
    \downarrow && \downarrow
    \\
    X^{\triangleleft} &\to& X^{\triangleleft} \coprod_X S
  }
  \,,
$$

where $X^\triangleleft = (*) \star X $ is the [[join of quasi-categories|join]] of $X$ with the point, i.e. $X$ with an [[initial object]] freely adjoined to it.

More discussion of why this is the case is at [Adjoints to the Grothendieck construction](http://ncatlab.org/nlab/show/Grothendieck+construction#adjunction).

The model category structure described below declares that a morphism in the [[overcategory]] $sSet/S$ is a weak equivalence if it induces a weak equivalence of the quasi-categories given by these pushouts. So this is effectively saying that we regard a morphism of right fibration of quasi-categories as a weak equivalences, if under the left adjoint to the $(\infty,1)$-Grothendieck construction it induces a weak equivalences of the $(\infty,1)$-functors that classify these fibrations.


## Definition

For $f : X \to S$ a morphism of [[simplicial set]]s, write $C^{\triangleleft}(f)$ for the [[pushout]]

$$
  \array{
    X &\hookrightarrow& X^{\triangleleft}
    \\
    \downarrow && \downarrow
    \\
    S &\to& S \coprod_{X} X^{\triangleleft} & =: C^{\triangleleft}(f) 
  }
$$

in the category [[sSet]] of simplicial sets. Call this the  **left cone** over $f$.

The [[colimit]]s in [[sSet]] are computed componentwise, so that the set of vertices $C^{\triangleleft}(f)_0$ is the disjoint union of the vertices of $S$ and one extra vertex $v$, the **cone point**.

+-- {: .un_defn}
###### Definition

([[Higher Topos Theory|HTT, def. 2.1.4.5]])


The **model structure for left fibrations** or **covariant model structure** $(sSet/S)_{lfib}$ on $SSet/S$ is given by

A morphism $f : X \to Y$ is 

* a cofibration if the underlying morphism of simplicial sets is a cofibration in the standard [[model structure on simplicial sets]], i.e. a [[monomorphism]];

* a weak equivalence if the induced morphism of cones

  $$
    X^{\triangleleft} \coprod_X S
    \to 
    Y^{\triangleleft} \coprod_Y S
  $$

  is a weak equivalence in the Joyal [[model structure for quasi-categories]], where $X^{\triangleleft}$ is the [[join of simplicial sets|join]] $X^{\triangleleft} := {*} \star X$.

=--

+-- {: .un_prop}
###### Proposition


This is a 

* [[proper model category|proper]]

* [[simplicial model category|simplicial]]

* [[combinatorial model category]].

([[Higher Topos Theory|HTT, prop 2.1.4.7, 2.1.4.8]])

We have 

* The fibrant objects are precisely the [[left fibration]]s 
  ([[Higher Topos Theory|HTT, corollary 2.2.3.12]])

* Every left anodyne morphism is an acyclic cofibration. 
  ([[Higher Topos Theory|HTT, prop 2.1.4.9]])


=--

## Properties

For every morphism $j : S \to S'$ we have the corresponding [[adjunction]] on [[overcategories]]

$$
  (j_! \dashv j^*)
  :
  sSet/S \stackrel{\overset{f_!}{\to}}{\underset{j^*}{\leftarrow}}
  sSet/{S'}
  \,,
$$

where

* $j_!$ is given by postcomposition of $j$;

* $j^*$ is given by [[pullback]] along $j$.



+-- {: .un_prop}
###### Proposition
**(change of base)**

This is a [[Quillen adjunction]] with respect to the model structures 
for left fibrations over $S$ and $S'$, respectively. ([[Higher Topos Theory|HTT, prop. 2.1.4.10]])

If $j$ is a [[model structure for quasi-categories|weak equivalence in]] $sSet_{Joyal}$, then this is a [[Quillen equivalence]]. ([[Higher Topos Theory|HTT, remark. 2.1.4.11]])


=--

+-- {: .un_prop}
###### Proposition
**($(\infty,1)$-Grothendieck construction)**

For $C$ a [[simplicially enriched category]] and $S = N(C)$ its [[homotopy coherent nerve]], there is a [[Quillen equivalence]]

$$
  (sSet/S)_{lfib} \stackrel{\leftarrow}{\to}
  [C, sSet_{Quillen}]
$$

between the model structure for left fibrations over $S$ and the [[global model structure on functors|global model structure on sSet-functors]]s on $C$ with values in [[sSet]] equipped with the standard [[model structure on simplicial sets]].

=--

For more on this see [[(∞,1)-Grothendieck construction]].


## References

This is the content of section 2.1.4 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

There the model structure $(sSet/S)_{lfib}$ is called the **covariant model structure** and the model structure $(sSet/S)_{rfib}$  the **contravariant model structure**.

[[!redirects model structure for right fibrations]]