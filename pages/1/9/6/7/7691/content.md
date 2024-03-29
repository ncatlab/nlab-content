[[!redirects I.1, k-functors]]
This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)


+-- {: .num_defn}
###### Definition
(k-ring, k-functor,affine k-scheme)

For a ring $k$ the _category of $k$-rings_, denoted by $M_k:=k/Ring$ is defined to be the category of commutative associative $k$-algebras with unit which are rings. This is equivalently the category of pairs $(R,f:k\to R)$ where $R$ is a Ring and $f$ is a morphism of $k$-algebras.

The _category of $k$-functors_, denoted by $co Psh (M_k)$, is defined to be the category of covariant functors $M_k\to Set$.

The forgetful functor $O_k:R\to R$ sending a $k$-ring to its underlying set is called _affine line_.

For the full and faithful contravariant functor

$$Sp_k:\begin{cases}
M_k&\to& co Psh(M_k)
\\
A&\to& M_k(A,-)
\end{cases}$$

 $Sp_k A$ (and every isomorphic functor) is called an _affine $k$-scheme_. (In most modern texts one uses the notation ''$Spec$'' instead of ''$Sp$''.) $Sp_k$ restricts to an equivalence between the categories of $k$-rings and the category $Aff Sch_k$ of affine $k$-schemes. We think of this category as of $M_k^{op}$. The functor $Sp_k$ commutes with limits and skalar extension (see below). Consequently $Aff Sch_k$ is closed under limits and base change.

The affine line $O_k=M_k(k[t],-)$ is an affine $k$-scheme.

A _[[k-ring of functions on a k-functor|function on a]]_ $k$-scheme $X$ is defined to be an object $f\in O(X):=co Psh (M_k)(X,O_k)$. $O(X)$ is a $k$-ring by component-wise addition and -multiplication.
=--

+-- {: .num_prop}
###### Proposition
There is an adjoint equivalence

$$(Sp\dashv O):Sch_{aff}\stackrel{O}{\to}Ring_k$$

of the categories of [[affine scheme|affine k-schemes]] and $k$-rings.
=--

+-- {: .num_remark}
###### Remark
The category of $k$-functors has limits.

The terminal object is $e:R\mapsto\{\varnothing\}$. Products and pullbacks are computed component-wise.
=--

+-- {: .num_remark}
###### Remark
For $\phi:k\to k^\prime$ the ''base change'' functor $(-)\otimes_k k^\prime:co Psh(M_k)\to co Psh(M_{k^\prime})$ induced by $(-)\circ \phi:M_k\to M_{k^\prime}$ given by postcompositions with $\phi$ is called _skalar extension_. 
=--