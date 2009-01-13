The concept of Cauchy completeness, ordinarily thought of as applying to metric spaces, was vastly generalized by Bill Lawvere in his influential paper "Metric spaces, closed categories, and generalized logic". It is now seen by category theorists as a concept of [[enriched category]] theory, with close ties to the concept of [[Morita equivalence]] in the theory of modules. 

The basic idea is that the Cauchy completion of a category is the closure of a category under what are called "absolute limits", i.e., limits that are preserved by any functor whatsoever. Equivalently, the Cauchy completion is the closure with respect to absolute colimits. If $C$ is small, the Cauchy completion $\bar{C}$ of $C$ lies between $C$ and its "free cocompletion", aka presheaf category

$$C \hookrightarrow \bar{C} \hookrightarrow Set^{C^{op}}$$ 

(see the entry at [[presheaf]] for "free cocompletion"), and consists of those presheaves $F$ dubbed "tiny" by Lawvere, meaning those presheaves which are connected and projective: the functor 

$$hom_{Set^{C^{op}}}(F, -): Set^{C^{op}} \to Set$$ 

preserves small coproducts and coequalizers. All of these concepts generalize straightforwardly to the context of general $V$-enriched categories, where $V$ is a complete, cocomplete, symmetric monoidal closed category. 

## Discussion 

_Todd_: I envision starting with the example $V = [0, \infty]$ before treating other bases $V$ such as $Set$ and $Ab$.

_Toby_: Although the term comes from $[0,\infty]$, readers might find it easier to understand in $\Set$, where we usually study limits first. That said, you should write whichever you want, and people will add to it.