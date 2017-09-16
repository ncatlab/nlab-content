#Idea#

The _category of elements_ is a $0$-category-theoretic version of the [[Grothendieck construction]], due to Mac Lane.

#Definition#

Given a functor $P:C^{\mathrm{op}}\to\mathbf{Set}$ (a [[presheaf]] of sets on $C$), one defines a category $\int_C P$ called the __category of elements__ of $P$. Objects of $\int_C P$ are pairs $(c,x)$ where $c$ is an object in $C$ and $x$ is an element in $P(c)$ and morphisms $(c,x)\to(c',x')$ are morphisms $u:c\to c'$ such that $P(u)(x') = x$.

The category of elements comes equipped with a _projection functor_ $\pi_P:\int_C P \to C$ given by $(c,x)\mapsto c$ and $u\mapsto u$; this projection should be viewed also as a $C$-indexed family.