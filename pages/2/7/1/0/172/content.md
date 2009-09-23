<div class="rightHandSide toc">
[[!include (infinity,1)-topos - contents]]
***
[[!include higher geometry - contents]]
</div>


#Contents#

* tic
{:toc}

#Idea#

The notion of $\infty$-stack is the $\infty$-[[vertical categorification|categorification]] of [[sheaf]] and [[stack]]. Where a sheaf is a [[presheaf]] with values in [[Set]] that satisfies the sheaf condition,
an [[higher category theory|∞-category]]-valued ([[pseudofunctor|pseudo]])[[presheaf]] is an _$\infty$-stack_ if it "satisfies descent" in that its assignment to a space $X$ is equivalent to its [[descent]] data for any [[cover]] or [[hypercover]] $Y^\bullet \to X$: if the canonical morphism

$$
  \mathbf{A}(X) \to
  Desc(Y^\bullet, \mathbf{A})
$$

is an equivalence. This is the _descent condition_.

One important motivation for $\infty$-stacks is that they generalize the notion of [[Grothendieck topos]] from [[category theory|1-categorical]] to [[higher category theory|higher categorical context]].

This is a central [[motivation for sheaves, cohomology and higher stacks|motivation for considering higher stacks]]. 

# Definition #

A well developed theory exists for $\infty$-stacks that are sheaves with values in [[∞-groupoid]]s. given that ordinary sheaves may be thought of as sheaves of [[0-category|0-categories]] and that $\infty$-groupoid-values sheaves may be thought of as sheaves of [[(infinity,0)-category|(∞,0)-categories]], these may be called [[(infinity,1)-sheaf|(∞,1)-sheaves]]. In the case that these $\infty$-groupoids have vanishing [[homotopy group]]s above some degree $n$, these are sometimes also called [[sheaves of n-types|sheaf of n-type]]s.

The currently most complete picture of [[(infinity,1)-sheaf|(∞,1)-sheaves]] appears in

* [[Jacob Lurie]], [[Higher Topos Theory]]

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

## Derived $\infty$-stacks ##

Notice that an $\infty$-stack is a [[(∞,1)-presheaf]] for which not only the codomain is an [[(∞,1)-category]], but where also the domain, the [[site]], may be an [[(∞,1)-category]].

To emphasize that one considers $\infty$-stacks on higher categorical sites one speaks of [[derived stack]]s.


#References#

The search for $\infty$-stacks probably began with [[Alexander Grothendieck]] in _[[Pursuing Stacks]]_.

The notion of $\infty$-stacks can be set up in various notions of $\infty$-categories. Jardine, [[Bertrand Toen]] and others have developed the theory of $\infty$-stacks in the context of [[simplicial presheaf|simplicial presheaves]] and [[Segal category|Segal categories]]. A review is

* [[Bertrand Toen]], _Higher and derived stacks: a global overview_ ([arXiv](http://arxiv.org/abs/math.AG/0604504)).

The explicit descent condition formulated above appears there on [page 12](http://arxiv.org/PS_cache/math/pdf/0604/0604504v3.pdf#page=12).

All this has been embedded into a coherent global theory in

* [[Jacob Lurie]], [[Higher Topos Theory]]

[[Note on Formatting|?]]

[[!redirects infinity-stacks]]
[[!redirects ∞-stack]]
[[!redirects ∞-stacks]]
[[!redirects infinity stack]]