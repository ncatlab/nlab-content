## Idea

If $C$ is a [[small category]] (or even a [[topological category]]), one can define a $C$-torsor (or _torsor with structure category $C$_) which generalizes the [[torsor]] (principal bundle) with structure group(oid). We present two variants in slightly different context.  

## Moerdijk's definition

If $F$ is a [[sheaf]] over $X$, denote by $F_x$ its stalk over $x$ (cf. [[etale space]]). 

A __$C$-torsor__ $E$ over a topological space $X$ is given by a functor $E : C\to Shv(X)$ such that 

1. (**surjectivity**) every 'total stalk' $\cup_{c\in C_0} E(c)_x$, where $x\in X$, is nonempty;

1. (**transitivity**) for any two germs 'in the same total stalk', $\alpha\in E(c)_x$, $\alpha'\in E(c')_x$, there is a span $c\stackrel{u}\leftarrow b\stackrel{u'}\to c'$ and $\xi\in E(b)_x$ such that $E(u)(\xi)=\alpha$ and $E(u')(\xi)=\alpha'$;

1. (**freeness**) a parallel pair $u_1,u_2: c\to c'$ of morphisms in $C$, may induce coalescence $E(u_1)(\alpha)=E(u_2)(\alpha)$ for some $\alpha\in E(c)_x$ only if there is a morphism $w:b\to c$ and $\zeta\in E(b)_x$ such that $u_1\circ w = u_2\circ w$ and $E(w)(\zeta)=\alpha$. 

This definition is from the monograph

* [[Ieke Moerdijk]], _Classifying spaces and classifying topoi_, Springer Lec. Notes Math. __1616__ (1995)

where it is shown that _the [[classifying space]] of a category $C$ classifies $C$-torsors_.

## Street's definition

Suppose now $C$ is a finitely complete category with a [[calculus of left fractions]] whose morphisms are called *covers*.

Let $A$ be an [[internal category]] in $C$. An __$A$-torsor trivialized by a cover__ $e : V\to U$ is a [[discrete fibration]] $A\stackrel{p}\leftarrow E\stackrel{q}\to U$ for which there exist a morphism $a : V\to A$ and a commutative diagram

<center><img src="http://latex.codecogs.com/gif.latex?
\xymatrix{
A\downarrow{a}\ar[r]^q \ar@/_2pc/[dd]_{p} \ar@%3C-.5ex%3E[d]
%26 V\ar[d]^e \\
E\ar[r]_q\ar[d]_p%26 U\\
A%26
}" />
</center>
in which the square is a pullback. Street says __$A$-torsor at $U$__ for an $A$-torsor trivialized by some cover $e : V\to U$.

* [[Ross Street]], _Combinatorial aspects of descent theory_, [pdf](http://www.math.mq.edu.au/~street/DescFlds.pdf) (page 25 in the file)

[[!redirects torsors with structure category]]