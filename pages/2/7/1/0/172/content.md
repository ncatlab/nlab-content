#Idea#

An $\infty$-stack is the [[vertical categorification|categorification]] of a [[sheaf]]. Where a sheaf is a [[presheaf]] with values in [[Set]] that satgisfies the sheaf condition,
an [[higher category theory|? category]]-valued ([[pseudofunctor|pseudo]])[[presheaf]] $\mathbf{A} : Spaces^{op} \to \infty-Cat$ is an _$\infty$-stack_ if it "satisfies descent" in that its assignment to a space $X$ is equivalent to its [[descent]] data for any [[hypercover]] $Y^\bullet \stackrel{\simeq}{\to}\gt X$: if the canonical morphism
$$
  \mathbf{A}(X) \to
  Desc(Y^\bullet, \mathbf{A})
$$
is an equivalence. This is the _descent condition_.

+-- {: .query}

[[John Baez]]: What does the 'greater than' sign mean above in the expression "$Y^\bullet \stackrel{\simeq}{\to}\gt X$"?  Or is this just a typo?  If not, some explanation would be nice.

[[Urs Schreiber]]: to my shame, I have to admit that $\to\gt$ was my hack for the symbol for _fibration_: an arrow with a double tip. 

=--


A well developed theory exists for the case of $\infty$-stacks with values in [[infinity-groupoid]]s. Their general theory is developed in

* [[Jacob Lurie]], [[Higher Topos Theory]]

With the general machinery of [[(infinity,1)-category]] theory in place, the definition of the [[(infinity,1)-category of (infinity,1)-sheaves]] is almost literally the same as that of the [[category of sheaves]].

One of the main theorems there says that the old [[model structure on simplicial presheaves]] are the canonical [[models for infinity-stack (infinity,1)-toposes]].


#References#

The search for $\infty$-stacks probably began with [[Alexander Grothendieck]] in _[[Pursuing Stacks]]_.

The notion of $\infty$-stacks can be set up in various notions of $\infty$-categories. Jardine, [[Bertrand Toen]] and others have developed the theory of $\infty$-stacks in the context of [[simplicial presheaf|simplicial presheaves]] and [[Segal category|Segal categories]]. A review is

* Bertrand To&#235;n, _Higher and derived stacks: a global overview_ ([arXiv](http://arxiv.org/abs/math.AG/0604504)).

The explicit descent condition formulated above appears there on [page 12](http://arxiv.org/PS_cache/math/pdf/0604/0604504v3.pdf#page=12).

All this has been embedded into a coherent global theory in

* [[Jacob Lurie]], [[Higher Topos Theory]]

[[!redirects infinity-stacks]]
[[!redirects ∞-stack]]
[[!redirects ∞-stacks]]
[[!redirects infinity stack]]