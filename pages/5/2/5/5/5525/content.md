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

Given any [[cohesive (∞,1)-topos]] 

$$
  (Disc \dashv \Gamma) : \mathbf{H}  \stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
$$

the [[inverse image]] $Disc$ of the [[global section]] functor is a [[full and faithful (∞,1)-functor]] and hence embeds [[∞Grpd]] as a full [[sub-(∞,1)-category]] of $\mathbf{H}$. A general object in $\mathbf{H}$ is a _cohesive $\infty$-groupoid_ . We say _discrete $\infty$-groupoid_ for the objects in the essential image of $Disc$. These are the $\infty$-groupoids with _[[discrete space|discrete]] cohesive_ structure.

This generalizes the traditional use of the word [[discrete group]].


## $Top$ as a cohesive $(\infty,1)$-topos {#TopAsCohesiveInfinTopos}

By the [[homotopy hypothesis]]-theorem the [[(∞,1)-topos]]es [[Top]] and [[∞Grpd]] are [[equivalence in an (∞,1)-category|equivalent]], hence indistinguishable by general abstract constructions in [[(∞,1)-topos theory]]. However, in practice it can be useful to distinguish them as two different [[presentable (∞,1)-category|presentations]] for an equivalence class of $(\infty,1)$-toposes.

For that purposes model [[(∞,1)-categories]] explicitly as [[quasi-categories]] and name for the purpose of this discussion the quasi-categories

$$
  Top := N(Top_{Quillen})^\circ \in N(sSet_{Joyal}^\circ)
$$

and

$$
  \infty Grpd := N(sSet_{Quillen})^\circ \in N(sSet_{Joyal}^\circ)
  \,,
$$

where on the right we have the standard [[model structure on topological spaces]] $Top_{Quillen}$ and the standard [[model structure on simplicial sets]] $sSet_{Quillen}$ as well as the Joyal-[[model structure for quasi-categories]] $sSet_{Joyal}$; and $N((-)^circ)$ denotes the [[homotopy coherent nerve]] of the [[simplicial category]] given by the full [[sSet]]-subcategory of these [[simplicial model categories]] on fibrant-cofibrant objects.

Then for 

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

Since this is an [[equivalence of (∞,1)-categories]] either functor serves as the [[left adjoint]] or [[right adjoint]] and so we may think of exhibiting $Top$ as a [[cohesive (∞,1)-topos]] over [[∞Grpd]] by setting

$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc)
  :
  Top
    \stackrel{\overset{\mathbb{R}Sing}{\to}}{\stackrel{\overset{\mathbb{L}{|-|}}{\leftarrow}}{\stackrel{\overset{\mathbb{R}Sing}{\to}}{\underset{\mathbb{L}{|-|}}{\leftarrow}}}}
  \infty Grpd
  \,.
$$

While degenerate, this setup does have some interest in practice. Notably it serves to identify the traditional presentation of the [[fundamental ∞-groupoid]] of a [[topological space]] by the [[singular simplicial complex]] explicitly as one instance of the general abstract notion of [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]

$$
  \Pi(X) = \mathbb{R} Sing X
  \,.
$$

This allows for instance to think of simplicial models for topological fibrations in terms of topological [[higher parallel transport]]. Some remarks on this are in <a href="http://ncatlab.org/nlab/show/higher+parallel+transport#FlatInTop">Flat higher parallel transport in Top</a>.


## Related concepts

* [[discrete space]]

* [[discrete group]]

* [[discrete groupoid]]

* **discrete ∞-groupoid**

[[!redirects discrete ∞-groupoid]]

[[!redirects discrete ∞-groupoids]]
[[!redirects discrete infinity-groupoids]]
