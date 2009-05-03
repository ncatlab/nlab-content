A constant [[infinity-stack]] or [[(infinity,1)-sheaf]] is the [[infinity-stackification]] of a [[(infinity,1)-presheaf]] which is constant as an [[(infinity,1)-functor]].

#Remarks#

For any [[(infinity,1)-category]] $S$, there is the obvious embedding of [[infinity-groupoid]]s into [[(infinity,1)-presheaf|(infinity,1)-presheaves]] on $S$

$$
  const : \infty Grpd \to [S^{op}, \infty Grpd]
$$

where of course

$$
  const_K : U \mapsto K
$$

for all $U$.

This is all very obvious, but deserves maybe a special remark in the case that $\infty$-groupoids are modeled as (compactly generated and weakly Hausdorff) [[topological space]]s: in particular in the case that $S = Top$ itself, there are then two different ways to regard a topological space as an $\infty$-stack, and they have very different meaning.


In particular, with $X$ a [[topological space]], the $\infty$-stack _constant_ on $X$ has the property that its [[loop space object]] $\Lambda X$ is indeed the $\infty$-stack constant on the free loop space of $X$, while the [[loop space object]] of $X$ regarded as a representable $\infty$-stack is just $X$ itself again. 

This is because 

* the $\infty$-stack represented by regards $X$ as a [[discrete category|categorically discrete]] topological groupoid;

* while the $\infty$-stack constant on $X$ regards $X$ as a topologically discrete groupoid which however may have nontrivial morphisms.




