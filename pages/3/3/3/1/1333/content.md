An **indiscrete category**, also called a **chaotic category**, is a [[category]] $C$ in which there is a unique [[morphism]] from each [[object]] $x$ to each object $y$:
$$
  \forall x,y \in Obj(C) : C(x,y) = *
  \,,
$$
where $*$ is the [[point]].

This means that 
* an indiscrete category is in fact a [[groupoid]];
* any [[inhabited set|inhabited]] indiscrete category is [[equivalence of categories|equivalent]] to the [[terminal category]].

Therefore, up to [[equivalence of categories|equivalence]], an indiscrete category is simply a [[truth value]].

The functor $Set\to Cat$ sending a set $X$ to the indiscrete category with $X$ as its set of objects is [[adjoint functor|right adjoint]] to the [[forgetful functor]] $Cat\to Set$ sending a category to its set of objects.  The [[adjoint functor|left adjoint]] to this forgetful functor sends a set $X$ to the [[discrete category]] on $X$.  (Although this forgetful functor is [[evil]], its adjoints are not.)