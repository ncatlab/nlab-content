
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* automatic toc goes here
{:toc}


## Definitions

A __filtered colimit__ or **finitely filtered colimit** is a [[colimit]] of a [[functor]] $F\colon D \to C$ where $D$ is a [[filtered category]].  

For $\kappa$ a [[cardinal number|regular cardinal]] a **$\kappa$-filtered colimit** is one over a $\kappa$-filtered category.


Similarly, a __cofiltered limit__ is a [[limit]] of a functor $F\colon D \to C$ where $D$ is a [[cofiltered category]], or equivalently of a [[contravariant functor]] $F\colon D \to C$ (that is a functor $F\colon D^{op} \to C$) where $D$ is a filtered category.  A cofiltered limit may also be called a __filtered limit__ (although this can be unclear); the respective terms __filtered [[direct limit]]__ and __filtered [[inverse limit]]__ are also popular.


A [[functor]] that preserves all finitely filtered colimits is called [[finitary functor|finitary]].


## Properties {#properties}

One of the reasons filtered colimits are important is that in [[Set]], filtered colimits commute with finite limits (and in fact, the filtered colimits can be characterized as precisely those colimits that commute with all finite limits in $Set$).  

For more on this see also [[limits and colimits by example]].

Filtered colimits are also important in the theory of [[locally presentable category|locally presentable]] and [[accessible category|accessible]] categories.  See also [[pro-object]] and [[ind-object]].

According to 1.5 and 1.21 in the book 

* Adamek & Rosicky, _Locally presentable and accessible categories_

a category has $\kappa$-[[directed colimits]] precisely if it has $\kappa$-filtered ones, and a functor preserves $\kappa$-directed colimits iff it preserves $\kappa$-filtered ones. A proof of this result, following Adamek & Rosicky, may be found [[theorem:directed colimits imply filtered colimits|here]]. 

The fact that directed colimits suffice to obtain all filtered ones may be regarded as a convenience similar to the fact that all [[colimits]] can be constructed from [[coproducts]] and [[coequalizers]].  Of course, a [[duality|dual]] result holds for [[codirected limits]].

### Flat functors and points of presheaf toposes ###

Let $C$ be a small category. Recall that a functor $F: C \to Set$ is **[[flat functor|flat]]** if it is a filtered colimit of [[representable functor]]s. 

Equivalently, a "module" $F: C \to Set$ is flat if and only if the [[tensor product]] 

$$- \otimes_C F: Set^{C^{op}} \to Set$$ 

is left exact. One may prove as a corollary that if $C$ is [[finitely complete category|finitely complete]], $F$ is flat if and only if it is [[left exact functor|left exact]] (preserves finite limits). Since this tensor product is automatically a left adjoint, we have the following basic result: 

+-- {: .un_prop} 
######Proposition 
For $C$ a small category, the category of "points" of $Set^{C^{op}}$ (i.e., geometric morphisms $Set \to Set^{C^{op}}$ and natural transformations between them) is equivalent to the category of flat modules on $C$. 
=-- 

(More was/is to be written here, including an application to geometric realization, relation to Diaconescu's theorem, and perhaps more.) 

[[!redirects cofiltered limit]]
[[!redirects filtered colimit]]
[[!redirects filtered inverse limit]]
[[!redirects cofiltered inverse limit]]
[[!redirects filtered direct limit]]
[[!redirects filtered limits]]
[[!redirects cofiltered limits]]
[[!redirects filtered colimits]]
[[!redirects filtered inverse limits]]
[[!redirects cofiltered inverse limits]]
[[!redirects filtered direct limits]]