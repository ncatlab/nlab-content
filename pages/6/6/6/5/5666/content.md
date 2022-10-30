#Contents#
* table of contents
{:toc}

## Idea

It is often easier to study formal group schemes using the associated Dieudonne module.


## Inductive Systems of Witt Modules

Let $k$ be a [[perfect field]] of positive [[characteristic]] $p$ and $A$ a $k$-[[algebra]]. Let $W_n(-)$ be the [[functor]] of truncated p-typical [[Witt vectors]].

We have an [[inductive limit|inductive system]] formed by shifting $V: W_n(A)\to W_{n+1}(A)$ given by $V(a_0, \ldots, a_{n-1})=(0, a_0, \ldots, a_{n-1})$. The shift satisfies many properties such as $RFV=p$, where $R$ is restriction and $F$ is the [[Frobenius map]].

Now let $\Lambda=W(k)$. We normally treat $W(A)$ as a $\Lambda$-[[module]] by taking $\lambda\in \Lambda$ and considering it as an element in $W(A)$ via the natural map $W(k)\to W(A)$ induced from the algebra map and then using Witt multiplication. When we do this, recall that $V$ is only a semi-linear map. It has the property that $V(\lambda a)=\lambda^{1/p}V(a)$. So it is not a map of $\Lambda$-modules, and hence the [[inductive limit|inductive system]] is not a system of $\Lambda$-modules. 

We can alter the $\Lambda$-structure to make $V$ a linear map. For notation, we'll say that $\overline{\lambda}$ is the image of $\lambda$ via $W(k)\to W(A)\to W_n(A)=W(A)/V^n(W(A))$. Let $W_n(A)$ be a $\Lambda$-module by the altered action $\lambda \star x= \overline{\lambda}^{p^{1-n}}x$, where two elements next to eachother means Witt multiplication. 

Let's check that this makes $V$ a $\Lambda$-linear map. $\displaystyle V(\lambda\star a)=V(\overline{\lambda}^{p^{1-n}}a)=V(F(\overline{\lambda}^{p^{-n}})a)=\overline{\lambda}^{p^{-n}}V(a)=\lambda\star V(a)$

Thus we have an inductive system of $\Lambda$-modules. 

## Dieudonne Module Definition

If $G$ is an [[affine scheme|affine]] [[commutative ring|commutative]] [[unitary]] [[group scheme]] over $k$, then we use this inductive system to define $D(G)$, the Dieudonne module of $G$ by taking $\displaystyle D(G)=\lim Hom(G, W_n(k))$, and similarly in the [[ind-object|Ind category]] so we have a Dieudonne module for [[formal group]] schemes and [[p-divisible groups]]. 

## Properties

Since all the $V$ operators are are monomorphisms, we get that $Hom(G, W_n(k))\to Hom(G, W_{n+1}(k))$ are all injective and hence we can identify $Hom(G, W_n(k))$ with a submodule of $D(G)$ or explicitly we know that $Hom(G, W_n(k))=\{m \in D(G): V^n(m)=0\}$. Thus every element of $D(G)$ is killed by a power of $V$. 

If we introduce a bit of abstraction we can see the beauty of all this. Let $D=\Lambda\{F, V\}$ be the noncommutative polynomial ring over the Witt vectors on two indeterminates that satisfy the commutation laws $Fw=w^p F$, $w^p V=Vw$, and $FV=VF=p$. This is called the [[Dieudonne ring]]. We have a canonical way to consider $D(G)$ as a left $D$-module. Thus $G\mapsto D(G)$ is a [[contravariant functor]] from affine unitary group schemes to the category of $D$-[[module]]s with $V$ torsion. This turns out to be an [[equivalence of categories|anti-equivalence]] of categories.

## Examples

* If $G$ is a [[p-divisible group]], then $D(G)$ is a free $\Lambda$-module of rank the height of $G$. 



## References

* Michel Demazure, Lectures on $p$-Divisible Groups




[[!redirects Dieudonné module]][[!redirects Dieudonne modules]][[!redirects Dieudonné modules]]



