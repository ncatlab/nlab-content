##Idea

Here we will look at the relationships between the two topics in the title! We will explore some of the functors linking the two categories.

##The functors $C^*$ and $L_*$.

####Cochain functors $C^* : DGLA\to CDGA$

Let $(V,\partial)$ be a differential graded vector space.  We let

$$C^r(V) = \bigoplus_{p+q=r}C^{p,q} (V),$$


where $C^{p,q} (V) \subset Hom^{p+q}(\otimes^p sV, k)$ is the subspace of (graded) _symmetric_ functions:

$$f(su_1,\ldots,su_p) = \varepsilon(\sigma)f(su_{\sigma(1)},\ldots,su_{\sigma(p))}),$$

for each permutation $\sigma$, having $\varepsilon(\sigma)$ as its Koszul sign.

The product of $f\in C^{p,q}$ and $g\in C^{r,s}$ is 

$$(f\wedge g)(su_1, \ldots,su_{p+r}) = \sum_{\sigma}\varepsilon(\sigma)f(su_{\sigma(1)},\ldots, su_{\sigma(p)})g(su_{\sigma(p+1)},\ldots,su_{\sigma(p+r)}),$$

where the sum is over all $(p,r)$-shuffles, $\sigma$ and $\varepsilon(\sigma)$ is the Koszul sign of :

$$(f,g,su_1,\ldots, su_{p+r})\to (f,su_{\sigma(1)},\ldots, su_{\sigma(p)},g,su_{\sigma(p+1)},\ldots,su_{\sigma(p+r)}).$$

With this product, $C(V)$ is a commutative graded algebra.

Now let $(L,\partial)$ be a [[differential graded Lie algebra]]. There are two derivations with square zero, which anti-commute defined by

$$\array{
(d_1f)(su_1,\ldots,su_n) &=&(-1)^{|f|}\sum_{i=1}^p(-1)^{|su_1|+ \ldots + |su_{i-1}|}f(su_1,\ldots,s\partial u_i,\ldots,su_p) \\
(d_2f)(su_1,\ldots,su_n)&=&(-1)^{|f|}\sum_{i\lt j}\varepsilon_{ij}(-1)^{|su_i|}f(s[u_i,u_j],su_1,\ldots, s\hat{u_i}, \ldots,s\hat{u_j},\ldots,su_p),}$$

where $\varepsilon_{ij}$ is the Koszul sign of 
	
$$(su_1, \ldots, su_p)\to (su_i,su_j,su_1,\ldots, s\hat{u_i}, \ldots,s\hat{u_j},\ldots,su_p),$$ 

where ''$s\hat{u_i}$'' indicates that the element $su_i$ has been omitted.  Putting $d = d_1 + d_2$, we have a commutative dga, $C^*(L,\partial)$, $d_1$ and $d_2$ being called, respectively, the linear and quadratic part of $d$.

