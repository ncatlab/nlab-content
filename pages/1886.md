

# Idea #

The axioms of a [[category]] ensure that every _finite_ number of composable morphisms has a (unique) composite.

_Transfinite composition_ is a means to talk about morphisms in a category that behave as if they were the result of composing infinitely many morphisms.

# Definition #

Let $\alpha$ denote in the following some [[ordinal number]] regarded as a [[poset]], hence as a [[category]] itself. Let $0 \in Obj(\alpha)$ be the smallest element.

Let $C$ be a [[category]] and $I \subset Mor(C)$ a class of morphisms in $C$. A **transfinite composition** of morphisms in $I$ is the universal morphism

$$
  F(0) \to colim_\alpha F(\alpha)
$$

from a [[diagram]]

$$
  F : \alpha \to C
$$

into its [[colimit]], where the diagram is such that 

* $F$ takes all successor morphisms $\beta \stackrel{\leq}{\to} \beta + 1$ in $\alpha$ to morphisms in $I$
  
  $$
    F(\beta \to \beta + 1) \in I
  $$

* $F$ is _continuous_ in that for every [[ordinal number|limit ordinal]] $F$ restricted to the diagram
  $\{\gamma \leq \beta\}$ is a [[colimit|colimiting cocone]] in $C$ in $F$ restricted to $\{\gamma \lt \beta\}$.


# Applications #

Transfinite composition plays a role in

* the [[small object argument]];

* [[cofibrantly generated model category|cofibrantly generated model categories]] .

# References #

The above formulation is taken from page 6 of 

* Tibor Beke, _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv.org/abs/math.CT/0102087))

