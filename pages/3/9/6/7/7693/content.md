[[!redirects I.6, the four definitions of formal schemes]]
This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

+-- {: .num_defn}
###### Definition and Remark

Let $k$ be a field. Let $Mf_k$ denote the category of finite dimensional $k$-rings.

1. A $k$-scheme is called a $k$_-formal scheme_ if it is is equivalent to a codirected colimit of finite (affine) $k$-schemes.

1. A $k$-scheme is a $k$-formal scheme if it is presented by a profinite $k$-ring or -equivalently- by a $k$-ring which is the limit of discrete quotients which are finite $k$-rings. If $A$ is such a topological $k$-ring $Spf_k(A)(R)$ denotes the set of continous morphisms from $A$ to the topological discrete ring $R$. We have $Spf_k$ is a contravariant equivalence between the category of profinite $k$-rings and the category $fSch_k$ of formal $k$-schemes.

1. Instead of defining $fSch_k$ as the opposite of $Mf_k$ define it covariantly on the category of finite dimensional $k$-corings.

1. A formal $k$-scheme is precisely a left exact (commutig with finite limits) functor $X:Mf_k\to Set$.

The inclusion $Mf_k\hookrightarrow M_k$ induces a functor

$${}^\hat\; :Sch_k\to fSch_k$$

called _completion functor_.
=--
## 3 

### [[k-coalgebra]] and [[k-coring]]

A *$k$-coalgebra* is a $k$-[[vector space]] $C$ equipped with a $k$-linear map $\Delta:C\to C\otimes_k C$.

A $k$-coalgebra $C$ is called a *$k$-coring* if $\Delta$ is

1. coassociative in that $(\Delta\otimes 1_C)\circ \Delta=(1_C\otimes \Delta)\circ \Delta$

1. cocommutative in that the image of $\Delta$ consists only of symmetric tensors.

1. has a counit $\epsilon$ to $\Delta$ satisfying $\Delta\circ (1_C\otimes \epsilon)=\Delta\circ (\epsilon\otimes 1_C)=1_C$.

### [[spectrum of a k-coring]]

Let $A$ and $R$ be two finite $k$-rings, let $A^*$ denote the [[k-coalgebra|dual k-coring]] of $A$.

Linear maps $A\to R$ correspond bijectively to elements of the tensor product $A^*\otimes R$. The $k$-linear maps $\Delta_{A^*}$ and $\epsilon_{A^*}$ extends to $R$-linear maps

$$A^*\otimes R\to (A^*\otimes R)\otimes_R(A^*\otimes R)$$

and

$$A^*\otimes R\to R$$

denoted by $\Delta$ and $\epsilon$.

+--{: .num_lemma}
###### Lemma and Definition

1. A $k$-linear map $A\to R$ associated to $u\in A^*\otimes R$ is a ring morphism iff $\Delta u= u\otimes u$ and $\epsilon u=1$.

1. There is a functorial isomorphism 

$$Sp(A(R)=\{u\in A^*\otimes R|\Delta u=u\otimes u, \epsilon u =1\}$$

and the *$k$-formal spectrum of the coring $C$* is defined by

$$Sp^* C(R)=\{u\in C\otimes R|\Delta u =u\otimes u, \epsilon u =1\}$$

in particular $Sp^*: M_k^{op}\to coPsh(M_k)$ is a covariant functor from the category of $k$-corings to the category of $k$-formal functors.
=--





## References

* Michel Demazure, lectures on p-divisible groups [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)