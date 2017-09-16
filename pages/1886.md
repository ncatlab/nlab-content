

# Idea #

The axioms of a [[category]] ensure that every _finite_ number of composable morphisms has a (unique) composite.

_Transfinite composition_ is a means to talk about morphisms in a category that behave as if they were the result of composing infinitely many morphisms.


# Definition #

Let $\alpha$ denote in the following some [[ordinal number]] regarded as a [[poset]], hence as a [[category]] itself. Let $0 \in Obj(\alpha)$ be the smallest element.

Let $C$ be a [[category]], $O$ an object of $C$, and $I \subset Mor(C)$ a class of morphisms in $C$. A **transfinite composition** of morphisms in $I$ is the universal morphism
$$
  O \to colim_\alpha F(\alpha)
$$
from a [[diagram]]
$$
  F : \alpha \to C
$$
into its [[colimit]], where the diagram is such that 

* $F$ takes all [[successor]] morphisms $\beta \stackrel{\leq}{\to} \beta + 1$ in $\alpha$ to morphisms in $I$
  $$
    F(\beta \to \beta + 1) \in I
  ,$$

* $F$ is _continuous_ in that for every nonzero [[ordinal number|limit ordinal]] $\beta \lt \alpha$, $F$ restricted to the diagram
  $\{\gamma \;|\; \gamma \leq \beta\}$ is a [[colimit|colimiting cocone]] in $C$ for $F$ restricted to $\{\gamma \;|\; \gamma \lt \beta\}$, and

* $F(0) = O$ if $\alpha \gt 0$.

Because of the latter clause, we really do not need to mention $O$ in the data except to cover the possibility that $\alpha = 0$.

For purposes of [[constructive mathematics]], the continuity condition should be stated as follows:

* For *every* ordinal $\beta$, $F$ restricted to the diagram $\{\gamma \;|\; \gamma \leq \beta\}$ is a colimiting cone in $C$
  for the disjoint union of $\{O\}$ and the restriction of $F$ to $\{\gamma + 1 \;|\; \gamma \lt \beta\}$.

This actually includes $F(0) = O$ as a special case but says nothing when $\beta$ is a successor (so the successor clause is still required).


# Applications #

Transfinite composition plays a role in

* the [[small object argument]];

* [[cofibrantly generated model category|cofibrantly generated model categories]] .


# References #

The above formulation is taken from page 6 of 

* Tibor Beke, _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math.CT/0102087))

