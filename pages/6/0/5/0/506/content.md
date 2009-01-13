#Idea#

Recall that an ordinary [[sheaf]] is a $Sets$-valued functor $X : S^{op} \to Sets$ on a [[locally small]] category $S$. Being locally small just means being [[enriched category|enriched]] over $Sets$, so sheaves naturally live in the context of $V$-[[enriched category theory]] for $V = Sets$.

This suggests that there are useful generalizations of the notion of sheaf with $S$ non-trivially $V$-enriched for other choices of $V$. It seems there are few examples for this in the literature _except_ for the case that $V$ is a category of "higher structures" such as [[simplicial set|simplicial sets]], [[quasi-category|quasi-categories]] or other [[infinity-category|infinity categories]], which is recently gaining plenty of attention.

The idea is that

* taking the _codomain_ of sheaves to be categories $V$ of "higher structures" leads from sheaves to $\infty$-stacks, as described at [[infinity-stack homotopically]];

* but also taking the _domain_ site $S$ to be enriched over higher structures $V$ makes the $\infty$-stack a _derived_ $\infty$-stack.


#References#

Derived ($\infty$-)stacks are currently mostly, maybe exclusively, studied on algebraic sites $S$, where the category $S^{op} := $ [[Alg]] is replaced with a category of "$\infty$-algebras" of sorts. The theory of these $\infty$-algebras is described in great detail in


* Jacob Lurie, _Derived Algebraic Geometry II: Noncommutative Algebra_ ([arXiv](http://arxiv.org/abs/math/0702299))

For a quick idea of the concept of derived $\infty$-stacks on such algebraic $\infty$-sites it might be helpful to have a look at [page 32, 33](http://arxiv.org/PS_cache/math/pdf/0604/0604504v3.pdf#page=32) of

* B. To&#235;n, _Higher and derived stacks: a global overview_ ([arXiv](http://arxiv.org/abs/math.AG/0604504))

Sites enriched over $V = SimpSet$ are introduced and studied in

* Bertrand To&#235;n, Gabriele Vezzosi, _Homotopical Algebraic Geometry I Topos theory_ ([pdf](http://www.math.uiuc.edu/K-theory/0579/agmod-I-fin-web.pdf))

The full theory of **stacks on model category sites** is developed in

* Bertrand To&#235;n, Gabriele Vezzosi, _Homotopical Algebraic Geometry II: geometric stacks and applications_ ([arXiv](http://arxiv.org/abs/math/0404373))

A useful review of many ideas and constructions in To&#235;n's work together with useful applications to [[geometric function theory]] is in 

* David Ben-Zvi, John Francis, David Nadler, [Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry] ([arXiv](http://arxiv.org/abs/0805.0157)).

#Blog resources#

Related discussion at the $n$Caf&#233; is at: 

* [Ben-Zvi on geometric function theory](http://golem.ph.utexas.edu/category/2009/01/benzvi_on_geometric_function_t.html): [formalization of derived infinity-stacks](http://golem.ph.utexas.edu/category/2009/01/benzvi_on_geometric_function_t.html#c021313)

and

* [enriched sheaf and topos theory?](http://golem.ph.utexas.edu/category/2009/01/nlab_general_discussion.html#c021240).