Let $V$ be a [[closed monoidal category]]. Recall that for $C$ a category [[enriched category|enriched over]] $V$, a $V$-[[module]] is a $V$-functor $\rho : C \to V$. We think of the object $\rho(a)$ for $a \in Obj(C)$ as the objects on which $C$ acts, and of $\rho(C(a,b))$ as the action of $C$ on these objects.

In this language a $C$-$D$ _bimodule_ for $V$-categories $C$ and $D$ is a $V$-functor

$$
  C^{op} \otimes D \to V
  \,.
$$

Such a functor is also called a profunctor or [[distributor]].

#Examples#

* Let $V = Vect$ and let $C = \mathbf{A}_1$ and $D = \mathbf{A}_2$ be two one-object $Vect$-enriched categories, whose endomorphism vector spaces are hence [[algebra]]s. Then a $C$-$D$ bimodule is a vector space $V$ with an action of $A_1$ on the left and and action of $A_2$ on the right.