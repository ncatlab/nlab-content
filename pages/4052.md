
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,2)$-Topos theory
+--{: .hide}
[[!include (infinity,2)-topos theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The notion of **2-topos** is the generalization of the notion of [[topos]] from [[category theory]] to the [[higher category theory]] of [[2-categories]].  

There are multiple conceivable such generalizations, depending in particular on whether one tries to generalize the notion of [[Grothendieck topos]] or of [[elementary topos]], and in the latter case what axioms one chooses to take as the basis for generalization.

In contrast, [[(n,1)-topos|(2,1)-toposes]] are much better understood.

A _Grothendieck 2-topos_ is a [[2-category]] of [[2-sheaves]] over a [[2-site]].

A _Grothendieck (2,1)-topos_ is a [[(2,1)-category]] of [[(2,1)-sheaves]] over a [[(2,1)-site]].

See also [[higher topos theory]].

## Properties

### Characterization of 2-sheaf 2-toposes

The [[2-toposes]] of [[2-sheaves]] over a [[2-site]] are special among all 2-toposes, in direct generalization of how [[sheaf toposes]] ("[[Grothendieck toposes]]") are special among all [[toposes]]. In that case, _[[Giraud's theorem]]_ famously characterizes sheaf toposes. This characterization has a 2-categorical analog: the _[[2-Giraud theorem]]_.

### $(n,r)$-Localic 2-toposes

A [[2-sheaf]] [[2-topos]] is "$(n,r)$-localic" or "$(n,r)$-truncated" if it has an [[(n,r)-site]] of definition.

In particular a $(2,1)$-localic 2-topos is the same as a [[(2,1)-topos]].


### In terms of internal categories
 {#InTermsOfInternalCategories}

Given a 2-topos $\mathcal{X}$, regard it is a [[2-site]] by equipping it with its [[canonical topology]]. 

+-- {: .num_defn}
###### Definition

Write $Cat(\mathcal{X})$ for the 2-category of _[[internal categories]]_ in $\mathcal{X}$, precisely: the 2-category of [[2-congruences]] and internal [[anafunctors]] between them (see [here](http://ncatlab.org/nlab/show/2-congruence#2CategoryOf2Congruences)).

=--


+-- {: .num_theorem #2SheavesAsInternalCategories}
###### Theorem

For $\mathcal{X}$ a 2-topos, there is an [[equivalence of 2-categories]]

$$
  \mathcal{X} \simeq Cat(\mathcal{X})
  \,.
$$

If $\mathcal{X}$ is $(2,1)$-localic, with a [[(2,1)-site]] of definition $C$, then there is already an equivalence

$$   
  \mathcal{X} \simeq Cat(Sh_{(2,1)}(C))
$$

with the 2-category of categories internal to the underlying [[(2,1)-topos]].

If $\mathcal{X}$ is $1$-localic, with 1-site of definition, then there is even already an equivalence

$$
  \mathcal{X} \simeq Cat(Sh(C))
$$

with the internal categories in the underlying [[sheaf topos]].

=--

+-- {: .proof}
###### Proof

By the [[2-Giraud theorem]], $\mathcal{X}$ is an [[exact 2-category]]. With this, the first statement is [this theorem](http://ncatlab.org/nlab/show/2-congruence#nCongExidempotent) at _[[2-congruence]]_.

By the discussion at [[n-localic 2-topos]], a 2-sheaf 2-topos has _[[core in a 2-category|enough groupoids]]_ precisely if it has a [[(2,1)-site]] of definition, and has _[[core in a 2-category|enough discretes]]_ precisely if it has a 1-site of definition.
With this the second and third statement is [this theorem](http://ncatlab.org/nlab/show/2-congruence#nCongOnGroupoidsAndDiscretes) at _[[2-congruence]]_.

=--

+-- {: .num_remark}
###### Remark

The noteworthy point about theorem \ref{2SheavesAsInternalCategories} is that for an ambient context which is a $(2,1)$-localic [[(2,1)-topos]], the straightforward morphisms of [[internal categories]], hence the notion of [[internal functors]], needs no further [[localization]]. This is in stark contrast to the situation for an ambient [[1-category]]. The generalization of this phenomenon is discussed at _[[category object in an (∞,1)-category]]_.

=--

## Examples

### The archetypical 2-topos

The archetypical 2-topos is [[Cat]]. This plays the role for 2-toposes as [[Set]] does for [[1-toposes]].

### Internal categories in a $(2,1)$-topos

Given any [[(2,1)-topos]] $\mathcal{X}$, the [[2-category]] $Cat(\mathcal{X})$ of [[internal (infinity,1)-category|internal categories]] in $\mathcal{X}$ ought to be a 2-topos. But it seems that at the moment there is no proof of this in the literature.

For literature on [[internal categories]] in [[1-toposes]] see at _[[2-sheaf]]_.

## Related concepts

* [[elementary theory of the 2-category of categories]] ([[ETCC]])


[[!include flavors of higher toposes -- list]]



## References

An introduction is in

* [[Mike Shulman]], _[[michaelshulman:What is a 2-topos]]?_

Early developments include

* [[Ross Street]], _Two dimensional sheaf theory_, J. Pure and Appl. Algebra 24 (1982) 2Opp.

A detailed discussion from the point of view of [[internal logic]] is at

* [[Mike Shulman]], _[[michaelshulman:2-categorical logic]]_

Discussion of the 2-categorical [[Giraud theorem]] for [[2-sheaf]] 2-toposes is in

* [[Ross Street]], _[[zoranskoda:Characterization of Bicategories of Stacks]]_  Category theory (Gummersbach 1981) LNM 962, 1982, MR0682967 (84d:18006)

* [[Mike Shulman]], _[[michaelshulman:2-Giraud theorem]]_

Discussion of the [[elementary topos]]-analog of 2-toposes is in

* [[Mark Weber]], _Yoneda structures from 2-toposes_ ([pdf](https://sites.google.com/site/markwebersmaths/home/yoneda-structures-from-2-toposes))

A notion of "flat 2-functor" (cf [[Diaconescu's theorem]]) perhaps relevant to the "points" of 2-toposes is in

* M.E. Descotte, [[Eduardo Dubuc]], M. Szyld, _On the notion of flat 2-functors_, arXiv:[1610.09429](https://arxiv.org/abs/1610.09429)


[[!redirects 2-toposes]]
[[!redirects 2-topoi]]


[[!redirects (2,1)-topos]]
[[!redirects (2,1)-toposes]]

[[!redirects (2,2)-topos]]
[[!redirects (2,2)-toposes]]


[[!redirects Grothendieck 2-topos]]
[[!redirects Grothendieck 2-toposes]]


