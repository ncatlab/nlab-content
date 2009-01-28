##Idea##

A [[crossed module]] is a bit like a normal subgroup... without being a subgroup. In fact if a crossed module has a boundary map which is a monomorphism then it is isomorphic to the inclusion crossed module of a normal subgroup.

Crossed modules model all connected homotopy 2-types.  Crossed squares model all connected [[homotopy 3-types]]s and correspond to pairs of normal subgroups. Suppose $G$ is a group and $M$ and $N$ are normal subgroups of $G$, then of course, so is $M\cap N$.  Put these groups in a square, with the inclusion maps between them. Finally note that if $m \in M$ and $n\in N$, then $[m,n]$ is in the intersection $M\cap N$. This gives you a crossed square with $h$-map $h(m,n) = [m,n]$.  Removing the  condition that the inclusions are inclusions(!) gives the general form.  

(The definition that follows is that given by Guin-Valery and Loday in their paper (see references).  Another definition can be given that is just the case $n = 2$ of that of [[crossed n-cube]], for which see that entry.
 

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

The classical homotopical example $\Pi(X;A,B)$ is determined by a pointed triad $(X; A,B)$ where $A,B \subseteq X$, and $P= \pi_1(A \cap B)$, $M= \pi_2(A, A \cap B), N= \pi_2(B, A \cap B)$ and $L=\pi_3(X; A,B)$. The operations of $P$ are the standard ones and  $h$ is the generalised Whitehead product. (The conventions may be slightly different from the standard ones in homotopy theory.)  This can be generalised to a functor $\Pi: (squares of pointed spaces) \to (crossed squares)$. 

Ellis uses this construction in 

G.J. Ellis, Crossed squares and combinatorial homotopy, Math. Z., 461 (1993) 93-110,

where the fact that that the crossed square associated to a triad is defined directly in terms of certain homotopy classes is important. 

The fact that there is a van Kampen type theorem for $\Pi$ implies that one calculates some nonabelian groups. It also implies that one is calculating some (pointed) homotopy 3-types. 




See also [[cat-2-group]]s. 