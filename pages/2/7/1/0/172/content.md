
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

* [[sheaf]]

* [[2-sheaf]] / [[stack]]

* [[(∞,1)-sheaf]] / **$\infty$-stack**

***


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The notion of $\infty$-stack is the $\infty$-[[vertical categorification|categorification]] of [[sheaf]] and [[stack]]. Where a sheaf is a [[presheaf]] with values in [[Set]] that satisfies the sheaf condition, an [[higher category theory|∞-category]]-valued ([[pseudofunctor|pseudo]])[[presheaf]] is an _$\infty$-stack_ if it "satisfies descent" in that its assignment to a space $X$ is equivalent to its [[descent]] data for any [[cover]] or [[hypercover]] $Y^\bullet \to X$: if the canonical morphism

$$
  \mathbf{A}(X) \to
  Desc(Y^\bullet, \mathbf{A})
$$

is an equivalence. This is the _descent condition_.

One important motivation for $\infty$-stacks is that they generalize the notion of [[Grothendieck topos]] from [[category theory|1-categorical]] to [[higher category theory|higher categorical context]].

This is a central [[motivation for sheaves, cohomology and higher stacks|motivation for considering higher stacks]]. They may also be thought of as [[internal ∞-groupoid]]s in a [[Grothendieck topos|sheaf topos]].

## Definition 

A well developed theory exists for $\infty$-stacks that are sheaves with values in [[∞-groupoids]]. given that ordinary sheaves may be thought of as sheaves of [[0-category|0-categories]] and that $\infty$-groupoid-values sheaves may be thought of as sheaves of [[(infinity,0)-category|(∞,0)-categories]], these may be called [[(infinity,1)-sheaf|(∞,1)-sheaves]]. In the case that these $\infty$-groupoids have vanishing [[homotopy groups]] above some degree $n$, these are sometimes also called [[sheaves of n-types|sheaf of n-types]].

The currently most complete picture of [[(infinity,1)-sheaf|(∞,1)-sheaves]] appears in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

but is based on a long development by other authors, some of which is indicated in the list of references below. 

With the general machinery of [[(∞,1)-category]] theory in place, the definition of the [[(infinity,1)-category of (infinity,1)-sheaves|(∞,1)-category of ∞-stacks]] is literally the same as that of a [[category of sheaves]]: it is a [[reflective (∞,1)-subcategory]]

$$
  \infty Stacks(C) \simeq Sh_\infty(C)
  \stackrel{\stackrel{\bar{(\cdot)}}{\leftarrow}}{\to}
  PSh_\infty(C)
$$

of the [[(infinity,1)-category of (infinity,1)-functors|(∞,1)-category of (∞,1)-presheaves]] with values in [[∞Grpd]], such that the left adjoint [[(∞,1)-functor]] $\bar {(\cdot)}$ -- the [[∞-stackification]] operation -- is left exact.

One of the main theorems of [[Higher Topos Theory]] says that the old [[model structure on simplicial presheaves|model structures on simplicial presheaves]] are the canonical 

* [[models for ∞-stack (∞,1)-toposes]]. 

This allows to regard various old technical results in a new conceptual light and provides powerful tools for actually handling $\infty$-stacks. 

In particular this implies that the old definition of [[abelian sheaf cohomology]] is secretly the computation of [[∞-stackification]] for $\infty$-stacks that are in the image of the [[Dold-Kan correspondence|Dold-Kan embedding]] of [[chain complex]]es of sheaves into [[simplicial presheaves|simplicial sheaves]].

### Derived $\infty$-stacks

Notice that an $\infty$-stack is a [[(∞,1)-presheaf]] for which not only the codomain is an [[(∞,1)-category]], but where also the domain, the [[site]], may be an [[(∞,1)-category]].

To emphasize that one considers $\infty$-stacks on higher categorical sites one speaks of [[derived stacks]].


### Higher $\infty$-stacks 

The above concerns $\infty$-stacks with values in [[∞-groupoids]], i.e, [[(∞,0)-category|(∞,0)-categories]]. More generally there should be notions of $\infty$-stacks with values in  [[(n,r)-category|(n,r)-categories]]. These are expected to be modeled by the [[model structure on homotopical presheaves]] with values in the category of [[Theta spaces]].


### Quasicoherent $\infty$-stacks

An archetypical class of examples of $\infty$-stacks are [[quasicoherent ∞-stack]]s of [[module]]s, being the [[vertical categorification|categorification]] of the notion of [[quasicoherent sheaf]]. By their nature these are really $(\infty,1)$-stacks in that they take values not in [[∞-groupoid]]s but in [[(∞,1)-categories]], but often only their [[∞-groupoid]]al [[core]] is considered.


### Affine $\infty$-stacks 


In 

* [[Bertrand Toen]], _Affine stacks (Champs affines)_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))

for the [[site]] $C = Alg_k^{op}$ with a suitable topology a [[Quillen adjunction]]

$$
  \mathcal{O} : sPSh(C)_{loc} \stackrel{\leftarrow}{\to}
  [\Delta^{op},Alg_k] \simeq dgAlg_k^{+}
  : 
  Spec
$$

is presented, where $\mathcal{O}$ sends and $\infty$-stack to its global [[dg-algebra]] of functions and $Spec$ constructs the simplicial presheaf "represented" degreewise by a simplicial algebra (under the [[monoidal Dold-Kan correspondence]] these are equivalent to dg-algebras).

An $\infty$-stack in the image of $Spec : dgAlg_k^+ \to sPSh(C)$ is an **affine $\infty$-stack**. The image of an arbitrary $\infty$-stack under the composite

$$
  Aff : sPSh(C) \stackrel{\mathcal{O}}{\to} dgAlg_k^+ \stackrel{Spec}{\to} sPSh(C)
$$

is its **affinization**.

This notion was considered in the full [[(∞,1)-category]] picture in 

* [[David Ben-Zvi]], [[David Nadler]], _Loop Spaces and Connections_ ([arXiv:math/1002.3636](http://arxiv.org/abs/1002.3636))

where it is also generalized to [[derived stack]]s, i.e. to the [[(∞,1)-site]] $dgAlg_k^-$ of cochain [[dg-algebra]]s in non-positive degree, where the pair of [[adjoint (∞,1)-functor]]s is

$$
  \mathcal{O} : 
  Sh_{(\infty,1)}((dgAlg_k^-)^{op})
  \stackrel{\leftarrow}{\to}
  [\Delta^{op},dgAlg_k^-] 
  \simeq
  dgAlg_k
  :
  Spec
$$

with $\mathcal{O}$ taking values in _unbounded_ dg-algebras.

In detail, $\mathcal{O}$ acts as follows: every [[∞-stack]] $X$ may be written as a ([[homotopy colimit|colimit]]) over [[representable functor|representable]] $Spec A_i \in dgAlg_i$

$$
  X \simeq \lim_{\to^i} Y(Spec A_i)
  \,,
$$

where $Y : (dgAlg^-)^{op} \to \mathbf{H}$ is the [[(∞,1)-Yoneda embedding]].

The functor $\mathcal{O}$ takes any such colimit-description, and simply reinterprets the colimit in $dgAlg^{op}$, i.e. the limit in $dgAlg$:

$$
  \mathcal{O}(X) = \lim_{\leftarrow^i} A_i
  \,.
$$




## References

The study of $\infty$-stacks is known in parts as the study of [[nonabelian cohomology]]. See there for further references.

The search for $\infty$-stacks probably began with [[Alexander Grothendieck]] in _[[Pursuing Stacks]]_.

The notion of $\infty$-stacks can be set up in various notions of $\infty$-categories. [[Andre Joyal]], Jardine, [[Bertrand Toen]] and others have developed the theory of $\infty$-stacks in the context of [[simplicial presheaf|simplicial presheaves]] and also in [[Segal category|Segal categories]].

* [[Bertrand Toën]], [[Gabriele Vezzosi]]; _Homotopical algebraic geometry. I. Topos theory_, Adv. Math. 193 (2005), no. 2, 257--372, [doi](http://dx.doi.org/10.1016/j.aim.2004.05.004), _Homotopical Algebraic Geometry II: geometric stacks and applications_, [math.AG/0404373](http://front.math.ucdavis.edu/0404.5373)

* [[Bertrand Toën]], [[Gabriele Vezzosi]]; _Segal topoi and stacks over Segal categories_, [math.AG/0212330](http://arxiv.org/abs/math.AG/0212330). 

* [[Bertrand Toën]]; _Higher and derived stacks: a global overview_ ([arXiv](http://arxiv.org/abs/math.AG/0604504)).

This concerns $\infty$-stacks with values in [[∞-groupoids]], i.e. $(\infty,0)$-categories. More generally [[descent]] conditions for $n$-stacks and $(\infty,n)$-stacks with values in [[(infinity,n)-category|(∞,n)-categories]] have been earlier discussed in

* [[Andre Hirschowitz]], [[Carlos Simpson]]; _Descente pour les $n$-champs_ ([arXiv](http://arxiv.org/abs/math/9807049))

All this has been embedded into a coherent global theory in the setting of [[quasicategory|quasicategories]] in

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects infinity-stacks]]
[[!redirects ∞-stack]]
[[!redirects ∞-stacks]]
[[!redirects infinity stack]]