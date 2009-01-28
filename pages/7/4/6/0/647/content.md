##Definition:##

(Ronnie put this up on another entry and I have just shifted it here. more will be added later.)

You are given four morphisms of groups $\lambda: L \to M$, $\lambda': L \to N$, $\mu: M \to P$, $\nu: N \to P$,  such that $\nu \lambda'= \mu \lambda$ together with actions of the group $P$ on $L, M, N$ on the left, conventionally, (and hence actions of $M$ on $L$ and $N$ via $\mu$ and of $N$ on $L$ and $M$ via $\mu$) and a function $h: M \times N \to L$. This structure
shall satisfy the following axioms:

1. the maps $\lambda, \lambda '$ preserve the actions of $P$; further, with the
given actions, the maps $\lambda, \lambda',\mu, \nu$ and $\kappa = \mu\lambda = \mu
'\lambda '$ are crossed modules;
1. $\lambda h(m,n)=m^n m^{-1},\lambda 'h(m,n)= {^m}n\,n^{-1}$
1. $h(\lambda l, n)= l^n l^{-1}, h(m,\lambda 'l)= {^m}l\, l^{-1}$
1. $ h(mm',n) = {^m}h(m',n) h(m,n), h(m,nn') = h(m,n) ^n h(m,n')$;
1. $h(^p m, {^p n})= {^p}h(m,n)$;

for all $l\in L, \,m, m'\in M,\, n,n'\in N$ and $p\in P$. 

This should be thought of as a _crossed module of crossed modules_ (in either direction!)

The classical homotopical example is determined by a pointed triad $(X; A,B)$ where $A,B \subseteq X$, and $P= \pi_1(A \cap B)$, $M= \pi_2(A, A \cap B), N= \pi_2(B, A \cap B)$ and $L=\pi_3(X; A,B)$. The operations of $P$ are the standard ones and  $h$ is the generalised Whitehead product. (The conventions may be slightly different from the standard ones in homotopy theory.)  This can be generalised to a functor $\Pi: (squares of pointed spaces) \to (crossed squares)$. 

See also [[cat^2-groups]]. 