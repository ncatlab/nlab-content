#$\infty$-Stack#

An [[higher category theory|infinity category]]-valued (pseudo)[[presheaf]] $\mathbf{A} : Spaces^{op} \to \infty-Cat$ is an _$\infty$-stack_ if it "satisfies descent" in that its assignment to a space $X$ is equivalent to its [[descent and codescent|descent data]] for any [[hypercover]] $Y^\bullet \stackrel{\simeq}{\to}\gt X$: if the canonical morphism
$$
  \mathbf{A}(X) \to
  Desc(Y^\bullet, \mathbf{A})
$$
is an equivalence. This is the _descent condition_.
 

##Examples##

* **Sheaves**: in the case that $\mathbf{A}$ takes values only in 0-categories (i.e. in $Sets$), this reproduces the definition of [[sheaf]].

* **Stacks**: in the case that $\mathbf{A}$ takes values only in 1-categories, this reproduces the definition of [[stack]].

#$\infty$-Costack#

Accordingly, an $\infty$-category valued (pseudo)copresheaf $\mathbf{B} : Spaces \to \infty-Cat$ is a **$\infty$-costack** if for all $X \in Spaces$ and all [[hypercover|hypercovers]] $Y^\bullet \stackrel{\simeq}{\to}\gt X$ the canonical morphism
$$
  Codesc(Y^\bullet, \mathbf{B}) \to \mathbf{B}(X)
$$
is an equivalence.


##Examples##

The $\infty$-groupoid valued co-presheaf 
$$
  \Pi_\infty : X \mapsto \Pi_\infty(X)
$$
which sends each space to its [[fundamental groupoid|fundamental infinity-groupoid]]. Should be an $\infty$-costack. For strict $n$-categories up to $n = 2$ this has been proven in

* Urs Schreiber, Konrad Waldorf, _Parallel Transport and Functors_ ([arXiv](http://arxiv.org/abs/0705.0452))

(for $n=1$) and

* Urs Schreiber, Konrad Waldorf, _Connections on non-abelian Gerbes and their Holonomy_ ([arXiv](http://arxiv.org/abs/0808.1923))

(for $n=2$).

The [[higher van Kampen theorem]] which has been proven for [[omega-category]]-valued $\Pi_\omega$, asserts that $\Pi_\omega(X)$ is not only equivalent to the _homotopy_ colimit over $\Pi_\omega(Y^n)$, for a cover $Y \to X$, but also to the _strict_ colimit. For further discussion of this see

* [_Codescent and the van Kampen theorem_](http://golem.ph.utexas.edu/category/2008/10/codescent_and_the_van_kempen_t.html)


#References.#

The notion of $\infty$-stacks can be set up in various notions of $\infty$-categories. Jardine, To&#235;n and others have developed the theory of $\infty$-stacks in the context of simplicial presheaves and [[Segal category|Segal categories]]. A review is

* Bertrand To&#235;n, _Higher and derived stacks: a global overview_ ([arXiv](http://arxiv.org/abs/math.AG/0604504)).

The explicit descent condition formulated above appears there on [page 12](http://arxiv.org/PS_cache/math/pdf/0604/0604504v3.pdf#page=12).

But the theory can be formulated whenever notions of [[descent and codescent]] $\infty$-categories exist. In the context of [[omega-category|omega-categories]] a formulation of $\infty$-stacks and costacks is discussed at [[schreiber:Differential Nonabelian Cohomology]].