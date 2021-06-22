
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

For $C$ an [[(∞,1)-category]] and $X \in C$ an [[object]], the _over-$(\infty,1)$-category_ or _slice $(\infty,1)$-category_ $C_{/X}$ is the $(\infty,1)$-category whose [[objects]] are [[morphism]] $p : Y \to X$ in $C$, whose morphisms $\eta : p_1 \to p_2$ are [[2-morphisms]] in $C$ of the form

$$
  \array{
     Y_1 &&\stackrel{f}{\to}&& Y_2
     \\
     & {}_{\mathllap{p_1}}\searrow &\swArrow_{\simeq}^{\eta}& \swarrow_{\mathrlap{p_2}}
     \\
     && X
  }
  \,,
$$

hence 1-morphisms $f$ as indicated together with a [[homotopy]] $\eta \colon p_2 \circ f \stackrel{\simeq}{\to} p_1$; and generally whose [[n-morphisms]] are [[diagrams]] 

$$
  \Delta[n+1] = \Delta[n] \star \Delta[0]\to C
$$ 

in $C$ of the shape of the cocone under the $n$-[[simplex]] that take the tip of the [[cocone]] to the object $X$.

This is the generalization of the notion of [[over-category]] in ordinary [[category theory]].

## Definition

We give the definition in terms of the model of [[(∞,1)-categories]] in terms of [[quasi-categories]].

Recall from [[join of quasi-categories]] that there are two different but quasi-categorically equivalent definitions of _join_, denoted $\star$ and $\diamondsuit$. Accordingly we have the following two different but quasi-categoricaly equivalent definitions of over/under quasi-categories.


+-- {: .num_prop}
###### Defnition/Proposition

Let $C$ be a [[quasi-category]]. let $K$ be any [[simplicial set]] and let 

$$
  F : K \to C
$$ 

be an [[(∞,1)-functor]] -- a morphism of simplicial sets. 


1. The **under-quasi-category** $C_{F/}$ is the 
   simplicial set characterized by the property 
   that for any other simplicial set $S$ there is 
   a natural bijection of hom-sets

   $$
    Hom_{sSet}(S, C_{F/})
     \cong
     (Hom_{(K\downarrow SSet)})(i_{K,S} , F)
     \,,
   $$

   where $i_{K,S} : K \to K \star S$ is the canonical inclusion of $K$ into its [[join of simplicial sets]] with $S$.

   Similarly, the **over quasi-category** over $F$ is the simplicial set
   characterized by the property that

   $$
    Hom_{sSet}(S, C_{/F})
     \simeq
     Hom_{(K\downarrow SSet)}(
       j_{K,S} , F
     )
   $$

   naturally in $S$, where $j_{K,S}$ is the canonical inclusion map $K\to S\star K$.  

1. The functor 

   $$
      sSet \to sSet_{K/}
   $$

   $$
     S \mapsto K \diamondsuit S
   $$

   with $\diamondsuit$ denoting the other definition of [[join of quasi-categories]] (as described there)

   has a [[right adjoint]]

   $$
      sSet_{K/} \to sSet
   $$

   $$
     (F : K \to C) \mapsto C^{F/} 
   $$

   and its image $C^{F/}$ is another definition of 
   the quasi-category under $F$.

=--

The first definition in terms of the the mapping property is due to [[Andre Joyal]]. Together with the discussion of the concrete realization it appears as [[Higher Topos Theory|HTT, prop 1.2.9.2]]. The second definition appears in [[Higher Topos Theory|HTT]] above prop. 4.2.1.5.

+-- {: .num_prop}
###### Proposition

The simplicial sets $C_{/F}$ and $C_{F/}$ are indeed themselves again [[quasi-categories]].

=--

This appears as [[Higher Topos Theory|HTT, prop. 1.2.9.3]]



+-- {: .num_prop}
###### Proposition

The two definitions yield equivalent results in that the canonical morphism

$$ 
  C_{/F} \to C^{/F}
  \,.
$$

is an equivalence of quasi-categories.

=--

This is [[Higher Topos Theory|HTT, prop. 4.2.1.5]]


From the formula 

$$
  (C_{/F})_n = (Hom_{sSet})_F(\Delta^n \star K , C)
$$

we see that

* an object in the over quasi-category $C_{/F}$ is a **[[cone]]** over $F$;. 

  For instance if $K = \Delta[1]$ then an object in $C_{/F}$ is a 2-cell

  $$
    \array{
       && v
       \\
       & \swarrow &\swArrow& \searrow
       \\
       F(0) &&\to&& F(1)
    }
  $$

  in $C$.

* a morphism in $C_{/F}$ is a morphism of cones, 

* etc:.

So we may think of the overcategory $C_{/F}$ as the **quasi-category of cones over $F$**. Accordingly we have that

* the [[terminal object in a quasi-category|terminal object]] in $C_{/F}$ is (if it exists) the [[limit in a quasi-category|limit in]] $C$ over $F$;

* the [[terminal object in a quasi-category|initial object]] in $C_{F/}$ is (if it exists) the [[limit in a quasi-category|colimit of]] $F$ in $C$.


## Properties

### Relation to over-1-categories

+-- {: .num_prop}
###### Proposition


For $C = N(\mathcal{C})$ (the [[nerve]] of) an ordinary [[category]] $\mathcal{C}$ and $K = *$, this construction coincides with the ordinary notion of [[overcategory]] $\mathcal{C}/F$ in that there is a canonical [[isomorphism]] of simplicial sets

$$
  N(\mathcal{C}/F) \simeq N(\mathcal{C})/F
  \,.
$$

=--

This appears as [[Higher Topos Theory|HTT, remark 1.2.9.6]].

### Functoriality of the slicing


+-- {: .num_prop}
###### Proposition

If $q : C \to D$ is a [[model structure for quasi-categories|categorical equivalence]] then so is the induced morphism $C_{/F} \to D_{/q F}$.

=--

This appears as [[Higher Topos Theory|HTT, prop 1.2.9.3]].


+-- {: .num_prop}
###### Proposition

For $C$ a [[quasi-category]] and $p : X \to C$ any morphism of simplicial sets, the canonical morphisms

$$
  C_{p/} \to C
$$ 

and

$$
  C^{p/} \to C
$$

are both [[left Kan fibrations]].

=--

This is a special case of [[Higher Topos Theory|HTT, prop 2.1.2.1]] and [[Higher Topos Theory|prop. 4.2.1.6]].


+-- {: .num_prop #FinalFunctorsInduceEquivalentSlices}
###### Proposition

Let $v \colon K \to \tilde K$ be a map of small [[(∞,1)-categories]], $\mathcal{C}$ an $(\infty,1)$-category, $\tilde{p}: \tilde{K} \to \mathcal{C}$ and $p = \tilde{p}v$. The induced [[(∞,1)-functor]] between slice $(\infty,1)$-categories

$$
  \mathcal{C}_{/ \tilde{p}} \to \mathcal{C}_{/p}
$$

 is an [[equivalence of (∞,1)-categories]] for each diagram $\tilde{p}$ precisely if $v$ is an op-[[final (∞,1)-functor]] (hence if $v^{op}$ is final).

=--

This is ([Lurie, prop. 4.1.1.8](#Lurie)).

### Hom-spaces in a slice
 {#HamSpacesInASlice}


+-- {: .num_prop}
###### Proposition

For $C$ an [[(∞,1)-category]] and $X \in C$ an [[object]] in $C$ and $f : A \to X$ and $g : B \to X$ two objects in $C/X$, the [[derived hom-space|hom-∞-groupoid]] $C/X(f,g)$ is equivalent to the [[homotopy fiber]] of
$C(A,B) \stackrel{g_*}{\to} C(A,X)$ over the morphism $f$: we have an [[(∞,1)-pullback]] [[diagram]]

$$
  \array{
     C/X(f,g) & \longrightarrow & C(A,B)
     \\
     \downarrow && \downarrow^{\mathrlap{g_*}}
     \\
     {*} & \stackrel{\vdash f}{\longrightarrow} & C(A,X)
  }
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.5.12]].


### Limits and Colimits in a slice
 {#LimitsAndColimits}

The forgetful functor $\mathcal{C}_{/X} \to \mathcal{C}$ out of a slice ([[dependent sum]]) [[reflected limit|reflects]] [[(∞,1)-colimits]]:

+-- {: .num_prop}
###### Proposition

Let $f \colon K \to \mathcal{C}_{/X}$ be a [[diagram]] in the slice of an [[(∞,1)-category]] $\mathcal{C}$ over an object $X \in \mathcal{C}$. Then if the composite $K \stackrel{f}{\to} \mathcal{C}_{/X} \to \mathcal{C}$ has an [[(∞,1)-colimit]], then so does $f$ itself and the projection $\mathcal{C}_{/q} \to \mathcal{C}$ takes the latter to the former. Conversely, a cocone $K \star \Delta^0  \to \mathcal{C}_{/X}$ under $f$ is an [[(∞,1)-colimit]] of $f$ precisely if the composite $K \star \Delta^0 \to \mathcal{C}_{/X} \to \mathcal{C}$ is an $(\infty,1)$-colimit of the projection of $f$.

=--

This appears as ([Lurie, prop. 1.2.13.8](#Lurie)).

On the other hand [[(∞,1)-limits]] in the slice are computed as limits over the diagram with the slice-cocone adjoined:

+-- {: .num_prop #LimitsInSliceAreLimitsInUnderlyingCategoryOverCoconeDiagram}
###### Proposition

For $\mathcal{C}$ an [[(∞,1)-category]], $X \;\colon\; \mathcal{D} \longrightarrow \mathcal{C}$ a [[diagram]], $\mathcal{C}_{/X}$ the [[comma category]] (the over-$\infty$-category if $\mathcal{D}$ is the point) and $F \;\colon\; K \to \mathcal{C}_{/X}$ a [[diagram]] in the [[comma category]], then the [[(∞,1)-limit]] $\underset{\leftarrow}{\lim} F$ in $\mathcal{C}_{/X}$ coincides with the limit $\underset{\leftarrow}{\lim} F/X$ in $\mathcal{C}$. 
 
=--

For a proof see at [[(∞,1)-limit]]  _[here](limit+in+a+quasi-category#InOvercategories)_.





[[!include sliced adjoint functors -- section]]






## Examples

* [[pointed homotopy types]]


## Related concepts

* [[arrow category]]

* [[over-category]] 

  * [[slice category]] 

  * [[under category]] 

  * [[over topos]]


* **over-(∞,1)-category**

  * [[model structure on an over category]] 

  * [[over-(∞,1)-topos]], [[etale geometric morphism]]

* [[arrow (∞,1)-category]], [[arrow (∞,1)-topos]]

* [[slice 2-category]]

## References

Section 1.2.9 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 
 {#Lurie}

[[!redirects over-category in quasi-categories]]
[[!redirects over quasi-categories]]
[[!redirects over quasicategory]]
[[!redirects over-quasi-category]]
[[!redirects over-quasicategory]]
[[!redirects overquasicategory]]
[[!redirects slice quasi-category]]
[[!redirects slice quasicategory]]

[[!redirects over-(∞,1)-category]]
[[!redirects over-(infinity,1)-category]]

[[!redirects slice infinity-category]]
[[!redirects slice infinity-categories]]

[[!redirects over-(∞,1)-categories]]
[[!redirects over-(infinity,1)-categories]]

[[!redirects under-(∞,1)-category]]
[[!redirects under-(infinity,1)-category]]

[[!redirects under-(∞,1)-categories]]
[[!redirects under-(infinity,1)-categories]]



[[!redirects over (∞,1)-category]]
[[!redirects over (infinity,1)-category]]

[[!redirects over (∞,1)-categories]]
[[!redirects over (infinity,1)-categories]]

[[!redirects over quasi-category]]

[[!redirects slice-(∞,1)-category]]
[[!redirects slice-(∞,1)-categories]]

[[!redirects slice (∞,1)-category]]
[[!redirects slice (∞,1)-categories]]
[[!redirects slice (infinity,1)-category]]
[[!redirects slice (infinity,1)-categories]]

[[!redirects coslice-(∞,1)-category]]
[[!redirects coslice-(∞,1)-categories]]

[[!redirects coslice (∞,1)-category]]
[[!redirects coslice (∞,1)-categories]]
[[!redirects coslice (infinity,1)-category]]
[[!redirects coslice (infinity,1)-categories]]

