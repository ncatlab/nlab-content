[[!redirects enriched hom-functors]]
[[!redirects enriched hom-functors]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The concept of _enriched hom-functor_ is the generalization of that of [[hom-functors]] from [[category theory]] to [[enriched category theory]].

## Definition

+-- {: .num_defn}
###### Definition
**(enriched hom-functor)**

For $\mathcal{V}$ a [[closed monoidal category|closed]] [[symmetric monoidal category]] with all [[limits]] and [[colimits]], let $\mathcal{C}$, be a $\mathcal{V}$-[[enriched category]]. Then its _$\mathcal{V}$-enriched hom-functor_ is the $\mathcal{V}$-[[enriched functor]]

$$
  \mathcal{C}(-,-)
  \;\colon\;
  \mathcal{C}^{op} \times \mathcal{C}
  \longrightarrow 
  \mathcal{V}
$$

from the enriched [[product category]] of $\mathcal{C}$ with its enriched [[opposite category]] to $\mathcal{V}$, canonically regarded as [[enriched category|enriched]] over itself, which sends [[pairs]] of [[objects]] to the corresponding [[hom-object]] in $\mathcal{C}$

$$
  c_1,c_2 \mapsto \mathcal{C}(c_1,c_2)
$$

and which on [[hom-objects]] of $\mathcal{C}^{op} \times \mathcal{C}$ is given by the evident pre- and post-[[composition]] operation.

=--

(e.g. [Borceux 94, Prop. 6.2.7](#Borceux94))


## Related concepts

* [[hom-set]], [[hom-object]]

* [[hom-functor]]

* [[enriched hom-functor]], [[internal hom-functor]]

* [[derived hom-functor]]


## References


* {#Borceux94} [[Francis Borceux]], Vol 2, Prop. 6.2.7 of _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)
