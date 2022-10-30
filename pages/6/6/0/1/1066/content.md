
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
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

The [[homotopy category]] of an [[(∞,1)-category]] $\mathcal{C}$ is its [[decategorification]] to an ordinary [[category]] obtained by identifying 1-[[morphisms]] that are connected by a [[2-morphism]].

If the [[(∞,1)-category]] $\mathcal{C}$ is presented by a [[category with weak equivalences]] $C$ (for instance as the [[simplicial localization]] $\mathcal{C} = L C$) then the notion of [[homotopy category]] of $C$ (where the weak equivalences are universally turned into [[isomorphism]]s) coinicides with that of $\mathcal{C}$:

$$
  Ho(\mathcal{C}) \simeq Ho(C)
  \,.
$$


## Definition 

The component-wise definition depend on the chosen model for $(\infty,1)$-categories, as either

* [[simplicially enriched category]]/ Top-category

* [[complete Segal space]]

* [[Segal category]]

* [[quasi-category]]

### In terms of simplicially enriched categories

The **homotopy category** $h C$ of a [[sSet]]-[[enriched category]] $C$ (equivalently of a [[Top]]-[[enriched category]]) is hom-wise the image under the functor

$$
  \pi_0 : sSet \to Set
 \,,
$$

which sends each [[simplicial set]] to its 0th [[homotopy group|homotopy set]]
of [[connected]] components, i.e. to the set of [[path component]]s:

$$
  Hom_{h C}(A,B) := \pi_0(Hom_C(A,B))
  \,.
$$

Sometimes it is useful to regard this after all as an enriched category, but now enriched over the [[homotopy category]] of the standard [[model structure on simplicial sets]] $sSet_{Quillen}$, which is the _homotopy category of an $(\infty,1)$-category_ of [[∞Grpd]].

Let $\mathbf{h}: sSet \to Ho(sSet)$ be the localization functor to the [[homotopy category]] (of a [[category with weak equivalences]]).  This functor is a [[monoidal functor]] by the fact that the cartesian monoidal product is a left-[[Quillen bifunctor]] for $sSet$, which means that since every object in $sSet$ is cofibrant, it preserves weak equivalences in both arguments and hence descends to the homotopy category

$$
  \array{
    sSet \times sSet &\stackrel{\times}{\to}& sSet
    \\
    \downarrow^{\mathrlap{\mathbf{h} \times \mathbf{h}}}
    &&
    \downarrow^{\mathrlap{\mathbf{h}}}
    \\
    Ho(sSet) \times Ho(sSet) &\stackrel{\mathbf{h}(\times)}{\to}&
    Ho(sSet)
  }
  \,.
$$

This inuces a canonical functor $h:sSet Cat\to Ho(sSet) Cat$ which is given by the identity on objects and: $Map_{h C}(A,B):=\mathbf{h} Map_{C}(A,B)$.   Then since $Hom_C(A,B)=Hom_{sSet}(\Delta^0,Map_{C}(A,B))$, it is easy to see that $Hom_{hC}(A,B)=Hom_{Ho(sSet)}(\mathbf{h} \Delta^0, \mathbf{h} Map_C(A,B))=\pi_0 Map_C(A,B)$.  



### In terms of complete Segal spaces and Segal categories

Similar, but more complicated, definitions work for [[complete Segal space]]s and [[Segal category|Segal categories]].


### In terms of quasi-categories

For [[quasi-category|quasi-categories]], one can write down a definition similar to those of $sSet$-enriched categories.

Viewing $C$ as a [[simplicial set]], the homotopy category $hC$ can also be described as its [[fundamental category]] $\tau_1(C)$, i.e. the image of $C$ by the [[left adjoint]] $\tau_1 : SSet \to Cat$ of the [[nerve]] functor $N$.

## Properties

### Brown representability 
 {#BrownRepresentability}

The [[Brown representability theorem]] characterizes [[representable functors]] on homotopy categories of $(\infty,1)$-categories:

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be a [[locally presentable (∞,1)-category]], [[compactly generated (∞,1)-category|generated]] by a set

$$
  \{S_i \in \mathcal{C}\}_{i \in I}
$$

of [[compact object in an (infinity,1)-category|compact objects]] (i.e. every object of $\mathcal{C}$ is an [[(∞,1)-colimit]] of the objects $S_i$.)

If each $S_i$ admits the structure of a [[cogroup]] object in the [[homotopy category of an (infinity,1)-category|homotopy category]] $Ho(\mathcal{C})$, then a [[functor]]

$$
  F \;\colon\; Ho(\mathcal{C})^{op} \longrightarrow Set
$$

(from the [[opposite category|opposite]] of the [[homotopy category of an (infinity,1)-category|homotopy category]] of $\mathcal{C}$ to [[Set]])

is [[representable functor|representable]] precisely if it satisfies these two conditions:

1. $F$ sends small [[coproducts]] to [[products]];

1. $F$ sends [[(∞,1)-pushouts]] $X \underset{Z}{\sqcup}Y$ to [[epimorphisms]], i.e. the canonical morphisms into the [[fiber product]]

   $$
     F\left(X \underset{Z}{\sqcup}Y\right)
     \stackrel{epi}{\longrightarrow}
     F(X) \underset{F(Z)}{\times} F(Y)
   $$

   are [[surjections]].

=--

([Lurie "Higher Algebra", theorem 1.4.1.2](#LurieHigherAlgebra))


## References



* [[Jacob Lurie]], [Section 1.2.3, p. 33](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=33)  of [[Higher Topos Theory]]

* {#LurieHigherAlgebra} [[Jacob Lurie]], section 1.4.1 of _[[Higher Algebra]]_


[[!redirects homotopy categories of (infinity,1)-categories]]

[[!redirects homotopy category of an (∞,1)-category]]
[[!redirects homotopy categories of (∞,1)-categories]]

