
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
* automatic table of contents goes here
{:toc}

## Idea

## Definition

We give the definition in terms of the model of [[(∞,1)-categories]] in terms of [[quasi-categories]].

Recall from [[join of quasi-categories]] that there are two different but quasi-catgorically equivalent definitions of _join_, denoted $\star$ and $\diamondsuit$. Accordingly we have the following two different but quasi-categoricaly equivalent definitions of over/under quasi-categories.


+-- {: .un_prop}
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

+-- {: .un_prop}
###### Proposition

The simplicial sets $C_{/F}$ and $C_{F/}$ are indeed themselves again [[quasi-categories]].

=--

+-- {: .proof}
###### Proof

This appears as [[Higher Topos Theory|HTT, prop. 1.2.9.3]]

=--


+-- {: .un_prop}
###### Proposition

The two definitions yield equivalent results in that the canonical morphism

$$ 
  C_{/F} \to C^{/F}
  \,.
$$

is an equivalence of quasi-categories.

=--

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, prop. 4.2.1.5]]

=--

From the formula 

$$
  (C_{/F})_n = (Hom_{sSet})_F(\Delta^n \star K , C)
$$

we see that

* an object in the over quasi-category $C_{/F}$ is a **cone** over $F$;. 

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



+-- {: .un_prop}
###### Proposition


For $C = N(\mathcal{C})$ (the [[nerve]] of) an ordinary [[category]] $\mathcal{C}$ and $K = *$, this construction coincides with the ordinary notion of [[overcategory]] $\mathcal{C}/F$ in that there is a canonical [[isomorphism]] of simplicial sets

$$
  N(\mathcal{C}/F) \simeq N(\mathcal{C})/F
  \,.
$$

=--

+-- {: .proof}
###### Proof

This appears as [[Higher Topos Theory|HTT, remark 1.2.9.6]].

=--

+-- {: .un_prop}
###### Proposition


If $q : C \to D$ is a [[model structure for quasi-categories|categorical equivalence]] then so is the induced morphism $C_{/F} \to C_{/q F}$.

=--

+-- {: .proof}
###### Proof

This appears as [[Higher Topos Theory|HTT, prop 1.2.9.3]].

=--


+-- {: .un_prop}
###### Proposition

For $C$ an [[(∞,1)-category]] and $X \in C$ an [[object]] in $C$ and $f : A \to X$ and $g : B \to X$ two objects in $C/X$, the [[derived hom-space|hom-∞-groupoid]] $C/X(f,g)$ is equivalent to the [[homotopy fiber]] of
$C(A,B) \stackrel{g_*}{\to} C(A,X)$ over the morphism $f$: we have an [[(∞,1)-pullback]] [[diagram]]

$$
  \array{
     C/X(f,g) &\to& C(A,B)
     \\
     \downarrow && \downarrow^{\mathrlap{g_*}}
     \\
     {*} & \stackrel{f}{\to} & C(A,X)
  }
  \,.
$$

=--

This is [[Higher Topos Theory|HTT, prop. 5.5.5.12]].

## Related concepts

* [[over-category]] 

  * [[slice category]] 

  * [[under category]] 

  * [[over topos]]


* **over-(∞,1)-category**

  * [[model structure on an over category]] 

  * [[over-(∞,1)-topos]]


## References

Section 1.2.9 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

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

[[!redirects over-(∞,1)-categories]]
[[!redirects over-(infinity,1)-categories]]

[[!redirects over (∞,1)-category]]
[[!redirects over (infinity,1)-category]]

[[!redirects over (∞,1)-categories]]
[[!redirects over (infinity,1)-categories]]

[[!redirects over quasi-category]]
