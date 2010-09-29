If $C$ is a [[small category]] (or even a [[topological category]]), one can define a $C$-torsor (or _torsor with structure category $C$_) which generalizes the [[torsor]] (principal bundle) with structure group(oid).  

If $F$ is a [[sheaf]] over $X$, denote by $F_x$ its stalk over $x$ (cf. [[etale space]]). 

A __$C$-torsor__ $E$ over a topological space $X$ is given by a functor $E : C\to Shv(X)$ such that 

1. (**surjectivity**) every 'total stalk' $\cup_{c\in C_0} E(c)_x$, where $x\in X$, is nonempty;

1. (**transitivity**) for any two germs 'in the same total stalk', $\alpha\in E(c)_x$, $\alpha'\in E(c')_x$, there is a span $c\stackrel{u}\leftarrow b\stackrel{u'}\to c'$ and $\xi\in E(b)_x$ such that $E(u)(\xi)=\alpha$ and $E(u')(\xi)=\alpha'$;

1. (**freeness**) a parallel pair $u_1,u_2: c\to c'$ of morphisms in $C$, may induce coalescence $E(u_1)(\alpha)=E(u_2)(\alpha)$ for some $\alpha\in E(c)_x$ only if there is a morphism $w:b\to c$ and $\zeta\in E(b)_x$ such that $u_1\circ w = u_2\circ w$ and $E(w)(\zeta)=\alpha$. 

This definition is from the monograph

* [[Ieke Moerdijk]], _Classifying spaces and classifying topoi_, Springer Lec. Notes Math. __1616__ (1995)

where it is shown that _the [[classifying space]] of a category $C$ classifies $C$-torsors_.

There is another notion of $C$-torsor in

* [[Ross Street]], _Combinatorial aspects of descent theory_, [pdf](http://www.math.mq.edu.au/~street/DescFlds.pdf) (page 25 in the file)

[[!redirects torsors with structure category]]