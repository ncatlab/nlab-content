+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[general topology|basic topology]] and [[differential geometry]], by an _atlas_ of/for a [[topological manifold|topological]]-, [[differentiable manifold|differentiable]]- or [[smooth manifold]] $X$ one means a collection of [[coordinate charts]] $U_i \subset X$ which form an [[open cover]] of $X$.

If one considers here the [[disjoint union]] $\mathcal{U} \coloneqq \underset{i}{\sqcup} U_i$ of all the [[coordinate charts]], then the separate chart embeddings $U_i \subset X$ give rise to a single [[map]] ([[continuous function|continuous]]/[[differentiable function]])

$$
  \mathcal{U} \longrightarrow X
$$

and now the condition for an atlas is that this is a [[surjective function|surjective]] [[étale map]]/[[local diffeomorphism]].

If, next, one regards this morphism, under the [[Yoneda embedding]], inside the [[topos]] of [[formal smooth sets]], then these conditions on an atlas say that this morphism is

1. an [[effective epimorphism]];

1. a [[formally étale morphism]].

In this abstract form the concept of an atlas generalizes to any [[cohesion|cohesive]] [[higher geometry]] ([KS 17, Def. 3.3](#KhavkineSchreiber17), [Wellen 18, Def 4.13](#Wellen18), [Sati & Schreiber 2020, p. 27](#SatiSchreiber20)). 

Next, for a [[geometric stack]] $\mathcal{X}$, an atlas is a [[smooth manifold]] $\mathcal{U}$ (for [[differentiable stacks]]) or [[scheme]] $\mathcal{U}$ (for [[algebraic stacks]]) or similar, equipped with a morphism 

$$
  \mathcal{U} \longrightarrow \mathcal{X}
$$

that is an [[effective epimorphism]] and [[formally étale morphism]]
in the corresponding [[(infinity,1)-topos|higher topos]] (for instance in that of [[formal smooth infinity-groupoids]]).


Here the terminology has a bifurcation: 

1. In the general context of [[geometric stacks]] one typically drops the second condition and calls any [[effective epimorphism]] from a [[smooth manifold]] or [[scheme]] to a [[differentiable stack]] or [[algebraic stack]], respectively, an _atlas_ (e.g. [Leman 10, 4.4](#Leman10)). 

1. If in addition the condition is imposed that such an effective epimorphism exists which is also [[formally étale morphism|formally étale]], then the [[geometric stack]] is called an _[[orbifold]]_ or _[[Deligne-Mumford stack]]_ (often with various further conditions imposed).


From here, the terminology generalizes to [[infinity-stacks|$\infty$-stacks]] in general [[(infinity,1)-toposes|$\infty$-toposes]], see [this Remark](groupoid+objects+in+an+infinity1-topos+are+effective#InterpretationInTermsOfInfinityStacksWithAtlases) at *[[groupoid objects in an (∞,1)-topos are effective]]*.



## Related concepts

* [[n-types cover]]

## References

Review of the classical concept of atlases for geometric stacks:

* {#Leman10} [[Eugene Lerman]], Section 4.4 of: _Orbifolds as stacks?_, L'Enseign. Math. (2) 56 (2010), no. 3-4, 315--363 ([arXiv:0806.4160](https://arxiv.org/abs/0806.4160))

Formalization in [[cohesive homotopy theory]] and [[cohesive homotopy type theory|cohesive]]/[[modal homotopy type theory]]:

* {#KhavkineSchreiber17} [[Igor Khavkine]], [[Urs Schreiber]], _Synthetic geometry of differential equations_ ([arXiv:1701.06238](https://arxiv.org/abs/1701.06238))

* {#Wellen18} [[Felix Wellen]], _[[schreiber:thesis Wellen|Formalizing Cartan Geometry in Modal Homotopy Type Theory]]_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966))

* {#SatiSchreiber20} [[Hisham Sati]], [[Urs Schreiber]], p. 27 of: *[[schreiber:Proper Orbifold Cohomology]]* ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))




[[!redirects atlases]]
