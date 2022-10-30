+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The term _discrete $\infty$-groupoid_ or _bare $\infty$-groupoid_ is essentially synonymous to just _[[∞-groupoid]]_ . It is used for emphasis in contexts where one consideres $\infty$-groupoids with extra [[cohesive (∞,1)-topos|cohesive]] [[stuff, structure, property|structure]] to indicate that this extra structure is being disregarded, or rather that the special case of [[discrete space|discrete]] such structure is considered.

## Definition

+-- {: .un_observation}
###### Observation

The [[terminal object in an (∞,1)-category|terminal]] [[(∞,1)-sheaf (∞,1)-topos]] [[∞Grpd]] is trivially a [[cohesive (∞,1)-topos]], where each of the defining four [[(∞,1)-functor]]s $(\Pi \dashv Disc \dashv \Gamma \dashv coDisc) : \infty Grpd \to \infty Grpd$ is an [[equivalence of (∞,1)-categories]]. 

=--


+-- {: .un_defn}
###### Definition

In the context of [[cohesive (∞,1)-topos]]es we say that [[∞Grpd]] defines **discrete cohesion** and refer to its objects as **discrete $\infty$-groupoids**.

More generally, given any other [[cohesive (∞,1)-topos]] 

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv codisc) : \mathbf{H}  \stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

the [[inverse image]] $Disc$ of the [[global section]] functor is a [[full and faithful (∞,1)-functor]] and hence embeds [[∞Grpd]] as a full [[sub-(∞,1)-category]] of $\mathbf{H}$. A general object in $\mathbf{H}$ is a _cohesive $\infty$-groupoid_ . We say $X \in \mathbf{H}$ is a **discrete $\infty$-groupoid** if it is in the [[image]] of $Disc$.

=--

+-- {: .un_remark}
###### Remark

This generalizes the traditional use of the terms [[discrete space]] and [[discrete group]]: 

* a [[discrete space]] is equivalently a 0-[[truncated]] discrete $\infty$-groupoid;

* a [[discrete group]] is equivalently a 0-[[truncated]] [[group object in an (∞,1)-category|group object]] in discrete $\infty$-groupoids.

=--

## $Top$ as a cohesive $(\infty,1)$-topos {#TopAsCohesiveInfinTopos}

By the [[homotopy hypothesis]]-theorem the [[(∞,1)-topos]]es [[Top]] and [[∞Grpd]] are [[equivalence of (∞,1)-categories|equivalent]], hence indistinguishable by general abstract constructions in [[(∞,1)-topos theory]]. However, in practice it can be useful to distinguish them as two different [[presentable (∞,1)-category|presentations]] for an equivalence class of $(\infty,1)$-toposes.

For that purposes consider the following

+-- {: .un_defn}
###### Definition

Define the [[quasi-categories]]

$$
  Top := N(Top_{Quillen})^\circ \in N(sSet_{Joyal}^\circ)
$$

and

$$
  \infty Grpd := N(sSet_{Quillen})^\circ \in N(sSet_{Joyal}^\circ)
  \,,
$$

where on the right we have the standard [[model structure on topological spaces]] $Top_{Quillen}$ and the standard [[model structure on simplicial sets]] $sSet_{Quillen}$ as well as the Joyal-[[model structure for quasi-categories]] $sSet_{Joyal}$; and $N((-)^\circ)$ denotes the [[homotopy coherent nerve]] of the [[simplicial category]] given by the full [[sSet]]-subcategory of these [[simplicial model categories]] on fibrant-cofibrant objects.

=--

For 

$$
  ({|-| \dashv Sing}) : Top_{Quillen} \stackrel{\overset{{|-|}}{\leftarrow}}{\underset{Sing}{\to}} sSet_{Quillen}
$$

the standard [[Quillen equivalence]] of the [[homotopy hypothesis]]-theorem given by the [[singular simplicial complex]]-functor and [[geometric realization]], write

$$
  (\mathbb{L} {|-|} \dashv \mathbb{R}Sing) : 
  Top 
    \stackrel{\overset{\mathbb{L}{|-|}}{\leftarrow}}{\underset{\mathbb{R}Sing}{\to}}
  \infty Grpd
$$

for the corresponding [[derived functor]]s (the image under the [[homotopy coherent nerve]] of the restriction of ${|-|}$ and $Sing$ to fibrant-cofibrant objects followed by functorial fibrant-cofibrant replacement) that constitute a pair of [[adjoint (∞,1)-functor]]s modeled as morphisms of [[quasi-categories]].

Since this is an [[equivalence of (∞,1)-categories]] either functor serves as the [[left adjoint]] or [[right adjoint]] and so we have

+-- {: .un_observation}
###### Observation

[[Top]] is exhibited a [[cohesive (∞,1)-topos]] over [[∞Grpd]] by setting

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc)
  :
  Top
    \stackrel{\overset{\mathbb{R}Sing}{\to}}{\stackrel{\overset{\mathbb{L}{|-|}}{\leftarrow}}{\stackrel{\overset{\mathbb{R}Sing}{\to}}{\underset{\mathbb{L}{|-|}}{\leftarrow}}}}
  \infty Grpd
  \,.
  \,.
$$

In particular a presentation of the intrinsic [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] is given by the familiar [[singular simplicial complex]] construction

$$
  \Pi(X) \simeq \mathbb{R} Sing X
  \,.
$$


=--

+-- {: .un_remark}
###### Remark

While degenerate, it is sometimes useful to make this example of a [[cohesive (∞,1)-topos]] explicit. For instance it allows to think of simplicial models for topological fibrations in terms of topological [[higher parallel transport]]. Some remarks on this are in <a href="http://ncatlab.org/nlab/show/higher+parallel+transport#FlatInTop">Flat higher parallel transport in Top</a>.


=--

+-- {: .un_remark}
###### Remark

Notice that the [[topology]] that enters the explicit construction of the objects in [[Top]] here does _not_ show up as [[cohesive (∞,1)-topos|cohesive structure]]. A [[topological space]] here is a model for a _discrete_ $\infty$-groupoid, the [[topology]] only serves to allow the construction of $Sing X$.
For discussion of $\infty$-groupoids equipped with genuine _topological cohesion_ see [[Euclidean-topological ∞-groupoid]].

=--





## Related concepts

* [[discrete space]]

* [[discrete group]]

* [[discrete groupoid]]

* **discrete ∞-groupoid**

[[!redirects discrete ∞-groupoid]]

[[!redirects discrete ∞-groupoids]]
[[!redirects discrete infinity-groupoids]]
