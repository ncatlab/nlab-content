Given a pair $L\dashv R$ of adjoint functors, $L:A\to B:R$, with counit $\epsilon$ and unit $\eta$, one forms a comonad $\mathbf{\Omega} = (\Omega, \delta,\epsilon)$ by $\Omega := LR$, $\delta := L\eta R$. $\mathbf{\Omega}$ comodules form a category $B_{\mathbf{\Omega}}$ and there is a natural comparison functor $K = K_{\mathbf{\Omega}} : A\to B_{\mathbf{\Omega}}$ given by $A\mapsto (LA,LA\stackrel{L(\eta_A)}\to LRLA)$. 

A functor $L:A\to B$ is __comonadic__ if it has a right adjoint $R$ and the corresponding comparison functor $K$ is an equivalence of categories. 

This situation is dual to the situation of a [[monadic functor]].

[[!redirects comonadic functor]]