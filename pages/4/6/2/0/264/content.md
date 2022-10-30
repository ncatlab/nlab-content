
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Given a [[category with weak equivalences]] $(\mathcal{C},W)$, then its _homotopy category_ $Ho(\mathcal{C})$ is, if it exists, the result of universally forcing the [[weak equivalences]] to become actual [[isomorphisms]], also called the _[[localization]]_ at the weak equivalences

$$
  \mathcal{C} \longrightarrow Ho(\mathcal{C})= \mathcal{C}[W^{-1}]
  \,.
$$

The classical example is the category of [[topological spaces]] with weak equivalences those [[continuous functions]] which are _[[homotopy equivalences]]_ or _[[weak homotopy equivalences]]_. The corresponding homotopy category is often referred to as "the homotopy category", by default, or the "[[classical homotopy category]]" for emphasis. This turns out to be equivalent to the category of topological spaces or (for weak homotopy equivalences) of just those [[homeomorphism|homoemorphic]] to [[CW-complexes]] with [[left homotopy]]-[[homotopy class|classes]] of continuous functions between them, whence the name "homotopy category".

The existence of a homotopy category, as well as tractable presentations of it typically require extra [[properties]] of the class of weak equivalences (such as that they admit a [[calculus of fractions]]) or even extra [[structure]] (such as [[fibration category]]/[[cofibration category]] structure, or full [[model category]] structure, or further enhancements of that to [[simplicial model category]] structures, etc). See at _[[homotopy category of a model category]]_ for more on this.

More generally, to every [[(∞,1)-category]] is associated a homotopy category, whose morphisms are literally the [[homotopy classes]] of the original morphisms. See at _[[homotopy category of an (∞,1)-category]]_ for more on this.

These two concepts of "homotopy category" are compatible: to a [[category with weak equivalences]] is associated, if it exists, an [[(∞,1)-category]] obtained by universally forcing the [[weak equivalences]] to become actual [[homotopy equivalences]], also called the _[[simplicial localization]]_ $L_W \mathcal{C}$ at the weak equivalences. The homotopy categories of $(\mathcal{C},W)$ and of $L_W \mathcal{C}$ coincide, which justifies the terminology "homotopy category" generally.


## Definition

### For simplicially enriched categories

Given a simplicially enriched category $C$, we can form for each pair of objects, $x,y$, of objects of $C$, the set, $\pi_0C(x,y)$, of connected components of the 'function space' $C(x,y)$.  As $\pi_0$ preserves finite limits, this gives a category, denoted $\pi_0(C)$.  As 1-simplices in $C(x,y)$ can be often interpreted as being homotopies, this category $\pi_0(C)$ is often called the _homotopy category of $C$_, and then the notation $Ho(C)$ may be used.  


This notions is closely related to the next, by using, say the [[hammock localisation]] of Dwyer and Kan, as then $\pi_0$ of that simplicially enriched category, coincides with the following.

### For categories with weak equivalences

Given a [[category with weak equivalences]] (such as a [[model category]]), its __homotopy category__ $Ho(C)$ is -- if it exists -- the [[category]] which is universal with the property that there is a [[functor]]

$$
 Q :  C \to Ho(C)
$$

that sends every weak equivalence in $C$ to an [[isomorphism]] in $Ho(C)$. 

One also writes $Ho(C) := W^{-1}C$ or $C[W^{-1}]$ and calls it the [[localization]] of $C$ at the collection $W$ of weak equivalences.

More in detail, the universality of $Ho(C)$ means the following:

* for any (possibly [[large category|large]]) category $A$ and functor $F : C \to A$ such that $F$ sends all $w \in W$ to isomorphisms in $A$, there exists a functor $F_Q : Ho(C) \to A$ and a natural isomorphism

$$
  \array{
     C &&\stackrel{F}{\to}& A
     \\
     \downarrow^Q& \Downarrow^{\simeq}& \nearrow_{F_Q}
     \\
     Ho(C)
  }
$$


* the functor $Q^* : Func(Ho(C),A) \to Func(C,A)$ is a [[full and faithful functor]].


The second condition implies that the functor $F_Q$ in the first condition is unique up to unique isomorphism.


## Properties

* If it exists, the homotopy category $Ho(C)$ is unique up to [[equivalence of categories]].



* As described at [[localization]], in general, the morphisms of $Ho(C)$ must be constructed using zigzags of morphisms in $C$ in which the backwards-pointing arrows are weak equivalences.  This means that in general, $Ho(C)$ need not be [[locally small category|locally small]] even if $C$ is.  However, in many cases (such as any [[model category]]) there is a more direct description of the morphisms in $Ho(C)$ as [[homotopy]] classes of maps in $C$ between suitably "good" (fibrant and cofibrant) objects.

* In [[2-limit|2-categorical terms]], the homotopy category $Ho(C)$ is the _coinverter_ of the canonical 2-cell
$$\array{& \to \\ W & \Downarrow & C\\ & \to}$$
where $W$ is the category whose objects are morphisms in $W$ and whose morphisms are commutative squares in $C$.



## Examples

* In classical [[homotopy theory]], _the_ homotopy category refers to the homotopy category [[Ho(Top)]] of [[Top]] with weak equivalences taken to be [[weak homotopy equivalences]].

* [[Ho(Top)]] is often restricted to the [[full subcategory]] of spaces of the [[homotopy type]] of a [[CW-complex]] (the full subcategory of CW-complexes in $Ho(Top)$). This is equivalent to $Ho(sSet_{Quillen})$, the homotopy category of the standard Quillen-[[model structure on simplicial sets]]. This equivalence is one aspect of the [[homotopy hypothesis]].

* In [[homological algebra]] the localization of the [[category of chain complexes]] at the [[quasi-isomorphisms]] is called the _[[derived category]]_. But see also at _[[homotopy category of chain complexes]]_.

* In [[stable homotopy theory]] one considers the [[stable homotopy category]] of [[spectra]].

* In [[equivariant stable homotopy theory]] one considers the [[equivariant stable homotopy category]] of spectra.

* For the homotopy category of [[Cat]], see [[Ho(Cat)]].

## Related concepts

* [[homotopy category of a model category]]

* [[homotopy category of an (infinity,1)-category]]

* [[homotopy 2-category]]


## References

See the references at [[model category]].

[[!redirects homotopy categories]]
