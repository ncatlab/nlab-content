The concept of a _perfect stack_ in the context of $\infty$-categories was introduced by Ben-Zvi, Francis and Nadler in their paper [Integral transforms and Drinfeld centers in derived algebraic geometry](http://arxiv.org/abs/0805.0157). It represents the most general class of derived stacks where [[geometric infinity-function theory]] works best. A perfect stack is a stack whose space of functions --- the category $QC(X)$ of [[quasicoherent sheaf|quasicoherent sheaves]] on $X$ --- is locally the inductive limit of a category of 'finite' objects. 

Perfect stacks cover a broad array of spaces of interest, with notable exceptions being the classifying space of a topological group such as $S^1$ or the classifying spaces of most algebraic groups in non-zero characteristic. This is because if $X$ is perfect, then the global sections functor $\Gamma$ must preserve colimits, which fails when the global sections $\Gamma(X, \mathcal{O}_X)$ of the structure sheaf is 'too large', as in the previous cases.

To define a perfect stack $X$, we must first define which [[quasicoherent sheaf|quasicoherent sheaves]] on $X$ we shall consider to be 'finite'. These are called the _perfect complexes_.

+-- {: .un_defn}
###### Definition
Let $A$ be a derived commutative ring. An $A$-module is _perfect_ if it lies in the smallest $\infty$-subcategory of $Mod_A$ containing $A$ and closed under finite colimits and retracts. For a derived stack $X$, the $\infty$-category $Perf(X)$ is the full $\infty$-subcategory of $QC(X)$ consisting of those sheaves $M$ whose restriction $f^*M$ to any affine $f: U \rightarrow X$ over $X$ is a perfect module.
=--

Now we can define what it means for a stack to be perfect, as well as for morphisms between them.

+-- {: .un_defn}
###### Definition
A derived stack $X$ is said to be _perfect_ if it has affine diagonal and the $\infty$-category $QC(X)$ is the inductive limit
 \[
 QC(X) \simeq \Ind \Perf(X)
\]
of the full $\infty$-subcategory $Perf(X)$ of perfect complexes. A morphism $X \rightarrow Y$ is said to be _perfect_ if its fibers $X \times_Y U$ over affines $U \rightarrow Y$ are perfect.
=--
