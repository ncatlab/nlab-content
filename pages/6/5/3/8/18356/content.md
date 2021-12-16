
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_prop #GrothendieckToposesAreLexReflectionsOfPresheafToposes}
###### Proposition

Let $(\mathcal{C}, \tau)$ be a [[small site|small]] [[site]]. 
Then the [[full subcategory]] inclusion $i \colon Sh(\mathcal{C},\tau) \hookrightarrow PSh(\mathcal{C})$ of its [[category of sheaves]] ([[Grothendieck topos]]) into its [[category of presheaves]] is a [[reflective subcategory]] inclusion 

$$
  Sh(\mathcal{C},\tau)
   \underoverset
     {\underset{i}{\hookrightarrow}}
     {\overset{L}{\longleftarrow}}
     {\bot}
  PSh(\mathcal{C})
$$

such that the reflector $L \colon PSh(\mathcal{C})  \to Sh(\mathcal{C})$ [[preserved limit|preserves]] [[finite limits]] (the reflector being [[sheafification]]).

Moreover, up to [[equivalence of categories|equivalence]], every [[Grothendieck topos]] arises this way: Given a [[small category]] $\mathcal{C}$ there is a [[bijection]] between 

1. the [[equivalence classes]] of left exact reflective subcategories $\mathcal{E} \hookrightarrow PSh(\mathcal{C})$ of the [[category of presheaves]] 

1. [[Grothendieck topologies]] $\tau$ on $\mathcal{C}$, 

which is such that $\mathcal{E} \simeq Sh(\mathcal{C}, \tau)$. 

=--

(e.g. [Borceux 94, prop. 3.5.4, cor. 3.5.5](#Borceux94), [Johnstone, C.2.1.11](#Johnstone))


+-- {: .num_prop #AccessibleReflection}
###### Proposition
**(accessible embedding is implied)**

In the situation of prop. \ref{GrothendieckToposesAreLexReflectionsOfPresheafToposes}
it follows that the inclusion $i \colon Sh(\mathcal{C},\tau) \hookrightarrow PSh(\mathcal{C})$ is an [[accessible functor]], hence an [accessible reflective subcategory inclusion](reflective+subcategory#AccessibleReflectiveSubcategories).


=--

+-- {: .proof}
###### Proof

Every  [[Grothendieck topos]] like $Sh(\mathcal{C}, \tau)$ and $PSh(\mathcal{C})$ is a [[locally presentable category]] ([this prop.](Grothendieck+topos#LocallyPresentable), [Borceux 94, vol 3, prop. 3.4.16](#Borceux94)). Therefore with prop. \ref{GrothendieckToposesAreLexReflectionsOfPresheafToposes} the statement follows by the [[adjoint functor theorem]] for locally presentable categories ([this prop.](adjoint+functor+theorem#AdjFuncTheoremForLocallyPresentableCats)).


=--


+-- {: .num_remark #GeneralizationToInfinityToposes}
###### Remark
**(generalization to [[(∞,1)-toposes]])**

For [[(∞,1)-toposes]] the accessibility of the reflection is no longer implied in general, contrary to prop. \ref{AccessibleReflection} above, but needs to be required. It is however still implied for [[topological localizations]] ([Lurie, Cor. 6.2.1.6](#Lurie)). 

=--


## References

* {#Borceux94} [[Francis Borceux]], vol. 3, section 3.5 of _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]]_

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_

[[!redirects sheafification preserves finite limits]]
