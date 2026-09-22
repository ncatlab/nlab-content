\tableofcontents

## Idea

A [[Mahlo cardinal]] is a [[large cardinal]] in [[set theory]] needed to make the set theory equivalent to a [[type theory]], like [[Agda]], with [[type universes]] with [[inductive-recursive types]] inside of the universe. 

## Definition

The [[ordinal]] $\kappa$ is Mahlo iff for any function $F : \kappa \to \kappa$, there is an [[inaccessible cardinal]] $\lambda$ such that $\lambda \lt \kappa$ and $\lambda$ is closed under $F$.

We can phrase this more structurally as follows: $\kappa$ is Mahlo iff for any functor $F : Core(Set_{\lt\kappa}) \to Core(Set_{\lt\kappa})$ on the category of sets strictly smaller than $\kappa$ and bijections, there is a [[universe]] $U$ with $|U| \lt \kappa$ which is closed under $F$.

## Without full separation

In the absence of the [[axiom of full separation]], such as in [[BZC]] or [[Mostowski set theory]], one typically works with recursively [[Mahlo cardinals]] instead of the usual [[Mahlo cardinals]]. Recursively [[Mahlo cardinals]] are like Mahlo cardinals but restricted to bounded $\Delta_0$-statements in the definition. 

Any large cardinal defined using [[elementary embeddings]] can only prove the existence of recursively [[Mahlo cardinals]], rather than the usual unbounded [[Mahlo cardinals]], in the absence of the [[axiom of full separation]]. These include [[measurable cardinals]], nearly [[supercompact cardinals]], [[Reinhardt cardinals]], the [[wholeness axiom]], and the $I_0$ through $I_3$ axioms. 

Furthermore, many large cardinals can be defined in more than one way. In the absence of the [[axiom of full separation]], these definitions no longer coincide with each other. Many large cardinals traditionally between recursively [[Mahlo cardinals]] and [[measurable cardinals]] have this property: they each have a combinatorial definition and a model-theoretic definition, and without full separation, the combinatorial definition of the cardinal does not coincide with the model-theoretic definition of the cardinal. In addition, only the model-theoretic definition has sufficient power to prove the existence of recursively [[Mahlo cardinals]], and none of the definitions has sufficient power to prove the existence of the usual [[Mahlo cardinals]]. Examples of such cardinals include weakly compact cardinals, subtle cardinals, ineffable cardinals, Erdős cardinals, Silver cardinals, Jónsson cardinals, Rowbottom cardinals, Ramsey cardinals, Magidor cardinals, and [[measurable cardinals]]. 

## See also

* [[large cardinal]]

## External links

* Wikipedia, [Mahlo cardinal](https://en.wikipedia.org/wiki/Mahlo_cardinal)

* [[Reinhard Kahle]], [[Anton Setzer]]: *An extended predicative definition of the Mahlo universe* &lbrack;[pdf](https://csetzer.github.io/articles/kahleSetzerExtendedPredicativeMahloPohlersFestschrift.pdf)&rbrack;

[[!redirects Mahlo cardinal]]
[[!redirects Mahlo cardinals]]

[[!redirects recursively Mahlo cardinal]]
[[!redirects recursively Mahlo cardinals]]