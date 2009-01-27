##Idea##
'Homotopy 3-type' is a special case of [[homotopy n-type]] and you are referred to that entry for the generalities.

##Discussion##
There are many useful algebraic models for a homotopy 3-type. (Assume the homotopy type is connected for simplicity.)

* [[2-crossed module]] All I will say here for the moment is that these are related to but not equivalent to the next two algebraic structures. So there is currently no higher homotopy van Kampen theorem with values in 2-crossed modules. 

* [[crossed squares]] I can do the Latex for a crossed square diagram using xypic, not in this system, but here is the written out definition. 

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

* [[cat 2-group|cat^2 group]] Here one can say easily that a cat^2-group is a double groupoid (or, equivalently, double category) internal to the category of groups. They are equivalent to crossed squares. Note that to calculate a colimit it is better to work with crossed squares, but to prove something is a colimit, it is better to work with cat^2-groups. 

(Someone please add their favorite version of the Gray groupoid type model. I am not sure I know it well enough to do a good job of it. Also any others?)
