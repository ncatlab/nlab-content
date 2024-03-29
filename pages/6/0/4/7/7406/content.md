
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $C$ be a [[coherent category]].  Write $\tau C$ for the category whose objects are pairs $(X,F)$ where $X$ is an object of $C$ and $F$ is a [[prime filter]] on $Sub_C(X)$.  This is the full subcategory of the [[category of filters]] of $C$ spanned by the prime filters.  Jet $J_p$ be the [[Grothendieck topology]] on $\tau C$ induced from the [[coherent topology]] on the category of filters. 

As defined by [Makkai](#Makkai), the **topos of types** $\mathbf{T}(C)$ of $C$ is the [[sheaf topos]]

$$
  \mathbf{T}(C) \coloneqq Sh_{J_p}(\tau C)
  \,.
$$

**Note:** The word "types" here has nothing to do with [[type theory]].  Instead, refers to the notion of [[type (in model theory)|type in model theory]].

## Properties

### In terms of the coherent hyperdoctrine

Let $C$ be a [[coherent category]]. The [[canonical extension]] $\mathcal{S}_C^\delta$ of its [[coherent hyperdoctrine]] $\mathcal{S}_C$  is naturally an [[internal locale]] in the [[presheaf topos]] $[C^{op}, Set]$ (as well as in the [[sheaf topos]] $Sh_{coh}(C)$ for the [[coherent topology]] on $C$).

The topos of types is equivalent to the topos of [[internal sheaves]] over this [[internal locale]].

$$
  \mathbf{T}(C) 
  \simeq
  Sh(\mathcal{S}_C^\delta)  
  \,.
$$

This is due to ([Coumans, theorem 25](#Coumans)).

In particular this implies that there is a [[localic geometric morphism]]

$$
 \mathbf{T}(C) \to Sh_{coh}(C)
 \,.
$$

Let $Mod(C) \simeq Func_{coh}(C,Set)$ be the category of [[models]] of the [[coherent theory]] given by $C$ in [[Set]]. 

There is a [[full subcategory]] $\mathcal{K} \hookrightarrow Mod(C)$ such that the [[Yoneda extension]] of the [[evaluation map]] $ev : C \to Func(\mathcal{K}, Set)$ is the [[inverse image]] of a [[geometric morphism]]

$$
  \phi_{ev} : Set^{\mathcal{K}} \to Sh_{coh}(C)
  \,.
$$

The [[(hyperconnected, localic) factorization system|hyperconnected / localic factorization]] of this morphism is through the topos of types of $C$:

$$
  \phi_{ev}
   :
  Set^{\mathcal{K}}
  \stackrel{hyperconn.}{\to}
  \mathbf{T}(C)
  \stackrel{localic}{\to}  
  Sh_{coh}(C)
  \,.
$$

This is ([Coumans, theorem 39](#Coumans)).



## Related concepts

* [[canonical extension]]


## References

The notion was introduced in 

* [[Michael Makkai]], _The topos of types_, Logic Year 1979-80 (Proc. Seminars and Conf. Math. Logic, Univ. Connecticut, Storrs, Conn., 1979/80), Lecture Notes in Math. __859__, Springer, Berlin (1981) pp. 157-201, [doi](http://dx.doi.org/10.1007/BFb0090947).
 {#Makkai}

The relation to [[canonical extension]] is made explicit in 

* Dion Coumans, _Generalizing canonical extensions to the categorical setting_, Annals of Pure and Applied Logic
December 2012, Vol.163(12):1940&#8211;1961  doi:[10.1016/j.apal.2012.07.002](http://dx.doi.org/10.1016/j.apal.2012.07.002), [pdf](http://www.math.ru.nl/~coumans/Generalisingcanonicalextensiontothecategoricalsetting-DionCoumans-vs2.pdf)
{#Coumans}

[[!redirects toposes of types]]
[[!redirects topoi of types]]
