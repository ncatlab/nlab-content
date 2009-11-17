#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

_Deformations_ and _deformation retracts_ are tools in [[homotopy theory]] for constructing the [[homotopy category]] of a [[model category]] or more general [[homotopical category]]. 

The idea of a deformation retract is to find a [[full subcategory]] of a given [[homotopical category]] $C$ such that

* a given functor $F$ from $C$ to another [[homotopical category]] becomes a [[homotopical functor]] on this subcategory;

* every object in the category is naturally weakly equivalent to an object in the subcategory.

Deformations are a generalizations of _cofibrant replacement functors_ in a [[model category]].


##Definition##

Let $C$ be a [[homotopical category]].

* A **left deformation** of $C$ is a functor $Q : C \to C$ equipped with a natural weak equivalence
$$
  \array{
    & \nearrow  \searrow^{Q}&
    \\
    C
    &\Downarrow^{q}_\simeq&
    C
    \\
    & \searrow  \nearrow_{Id}
  }
$$
(it follows from [[category with weak equivalences|2-out-of-3]] that $Q$ is a [[homotopical functor]]).

* A **left deformation retract** is a [[full subcategory]] $C_Q$ containing the image of a left deformation $(Q,q)$.

Now let $F : C \to D$ be a functor between [[homotopical category|homotopical categories]].

* A **left deformation retract for $F$**  is a left deformation retract $C_Q$ of $C$ such that $F$ becomes a [[homotopical functor]] when restricted to $C_Q$.

Right deformations are defined analogously.


##Generalization##

There are pretty obvious generalizations of deformation retracts for functors of more than one variable. 

* A **deformation retract** for a [[two-variable adjunction]] $(\otimes , hom_l, hom_r) : C \times D \to E$ consists of left deformation retracts $C_Q$, $D_Q$ for $C$ and $D$, respectively, and a right deformation retract $E_Q$ of $E$, such that

  * $\otimes$ is [[homotopical functor|homotopical]] on $C_Q \times D_Q$;

  * $hom_l$ is [[homotopical functor|homotopical]] on $C_Q^{op} \times E_Q$;

  * $hom_r$ is [[homotopical functor|homotopical]] on $D_Q^{op} \times E_Q$.

##References##

The definition of deformation and deformation retract is in paragraph 40 of

* William G. Dwyer, Philip S. Hirschhorn, Daniel M. Kan, and Jeffrey H. Smith. Homotopy Limit Functors on Model Categories and Homotopical Categories, volume 113 of Mathematical Surveys and Monographs. American Mathematical Society, 2004.

The notion of deformation retract of a [[two-variable adjunction]] is [definition 15.1, p. 43](http://arxiv.org/PS_cache/math/pdf/0610/0610194v1.pdf#page=43)
in 

* Michael Shulman, _Homotopy limits and colimits and enriched homotopy theory_ ([arXiv](http://arxiv.org/abs/math.AT/0610194v1))
