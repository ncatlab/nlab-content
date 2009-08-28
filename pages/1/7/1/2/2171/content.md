The **Artin braid group**, $Br_{n+1}$, defined using $n+1$ strands is a [[group]] given by 

* generators: $y_i$, $i = 1, \ldots, n$;

* relations: 

  * $r_{i,j} \equiv y_i y_j y_i^{-1} y_j^{-1}$ for $i+1 \lt j$

  * $r_{i,i+1}\equiv y_i y_{i+1} y_i y_{i+1}^{-1} y_i^{-1} y_{i+1}^{-1}$ for $1 \leq i \lt n$.


## Examples

We will look at such groups for small values of $n$.

+-- {: .un_example}
###### The group $Br_1$

By default, $Br_1$ has no generators and no relations, so is trivial.
=--

+-- {: .un_example}
###### The group $Br_2$

By default, $Br_2$ has one generator and no relations, so is infinite cyclic.
=--

+-- {: .un_example}
###### The group $Br_3$
(We will simplify notation writing $u = y_1$, $v = y_2$.)

This then has presentation 

$$\mathcal{P} = ( u,v : r \equiv u v u v^{-1} u^{-1} v^{-1}).$$

It is also the 'trefoil group', i.e., the fundamental group of the complement of a trefoil [[knot]]. 
=--

+-- {: .un_example}
###### The group $Br_4$

Simplifying notation as before, we have generators $u,v,w$ and relations

 *  $r_u \equiv  v w v w^{-1} v^{-1} w^{-1}$,
 *  $r_v \equiv  u w u^{-1} w^{-1}$,
 *  $r_w \equiv  u v u v^{-1} u^{-1} v^{-1}$.
=--


## References

English Wikipedia article: [Braid group](http://en.wikipedia.org/wiki/Braid_group)
