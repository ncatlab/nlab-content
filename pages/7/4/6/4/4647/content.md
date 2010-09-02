Given a pair $L\dashv R$ of adjoint functors, $L:A\to B:R$, with counit $\epsilon$ and unit $\eta$, one forms a comonad $\mathbf{\Omega} = (\Omega, \delta,\epsilon)$ by $\Omega := LR$, $\delta := L\eta R$. $\mathbf{\Omega}$ comodules form a category $B_{\mathbf{\Omega}}$ and there is a natural comparison functor $K = K_{\mathbf{\Omega}} : A\to B_{\mathbf{\Omega}}$ given by $A\mapsto (LA,LA\stackrel{L(\eta_A)}\to LRLA)$. 

A functor $L:A\to B$ is __comonadic__ if it has a right adjoint $R$ and the corresponding comparison functor $K$ is an equivalence of categories. 

Beck's [[monadicity theorem]] has its dual, comonadic analogue. To discuss it, observe that for every $\Omega$-comodule $(N,\rho)$, 

<center><img src="http://latex.codecogs.com/gif.latex?
\xymatrix{
N\ar[r]_{\rho} %26 Q^* Q_* N \ar@/_1pc/[l]_{\epsilon_N} \ar@%3C.5ex%3E [r]^{Q^* Q_* \rho}\ar@%3C-.5ex%3E[r]_{Q^*\eta_{Q_* N}} %26 Q^* Q_* Q^* Q_* N\ar@/_2pc/[l]_{\epsilon_{Q^*Q_*N}}
}" />
</center>

manifestly exhibits a _split equalizer_ sequence.

...

[[!redirects comonadic functor]]