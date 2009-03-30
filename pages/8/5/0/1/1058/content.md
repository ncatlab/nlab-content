If $C$ is a [[small category]] (or even a [[topological category]]), one can define a $C$-torsor (or _torsor with structure category $C$_) which generalizes the [[torsor]] (principal bundle) with structure group(oid).  

If $F$ is a [[sheaf]] over $X$, denote by $F_x$ its stalk over $x$ (cf. [[etale space]]). 

A __$C$-torsor__ $P$ over a space $X$ is given by a functor $P : C\to Shv(X)$ such that 

1. (**surjectivity**) every 'total stalk' $\cup_{c\in C_0} E(c)_x$, where $x\in X$, is nonempty;

1. (**transitivity**) for any two germs 'in the same total stalk', $\alpha\in E(c)_x$, $\alpha'\in E(c')_x$  there is a span $u:b\to c$, $u:b\to d$ and $\xi\in E(b)_x$ such that $E(u)(\xi)=\alpha$ and $E(u')(\xi)=\alpha'$;

1. (**freeness**) a parallel pair $u_1,u_2: c\to c'$ of morphisms in $C$, may induce coalescence $E(u_1)(\alpha)=E(u_2)(\alpha)$ for some $\alpha\in E(c)_x$ only if there is a morphism $w:b\to c$ and $\zeta\in E(b)_x$ such that $u_1\circ w = u_2\circ w$ and $E(w)(\zeta)=\alpha$. 

The [[classifying space]] of a category $D$ classifies $D$-torsors.

Literature: I. Moerdijk, Classifying spaces and classifying topoi, Springer Lec. Notes Math. 1616 (1995)