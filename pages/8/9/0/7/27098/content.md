## Idea

Reflection of an object $d$ in $D$ along a functor $F:C\to D$ is a component $\eta_d$ in $D$ of would-be unit of adjunction $L\dashv F$ (which may not exist in general), satisfying the part of the universal property of the unit for that component. If a reflection of each object in $D$ along $F$ exists and is chosen then the [[left adjoint functor]] to $F$ exists.

Similarly, one can define a coreflection along a functor by a component $\epsilon_d$ in $D$ of would-be counit of adjunction $F\dashv R$.

## Definition

Let $F:C\to D$ be a functor and $d$ an object in $D$. 

A __reflection__ of $d$ along $F$ is a pair $(L_d,\eta_d)$ of an object $L_d\in C$ and a morphism $\eta_d : d\to F(L_d)$ in $D$ which is universal in the sense that for any $c\in C$ and a morphism $f:d\to F(c)$ there is a unique $\alpha: L_d\to c$ such that $F(\alpha)\circ\eta_d = f$.

A __coreflection__ of $d$ along $F$ is a pair $(R_d,\epsilon_d)$ of an object $R_c\in C$ and a morphism $\epsilon_d : F(R_d)\to d$ in $D$ which is universal in the sense that for any $c\in C$ and a morphism $g:F(c)\to d$ there is a unique $\beta: c\to R_d$ such that $\epsilon_d\circ F(\beta) = g$.

## Literature 

*  [[Francis Borceux]], _Handbook of categorical algebra_,  I.3.1

[[!redirects coreflection along a functor]]