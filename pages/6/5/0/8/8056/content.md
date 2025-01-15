
# Iterated monoidal categories
* table of contents
{: toc}

## Idea 

An _iterated monoidal category_, or _$n$-fold monoidal category_ for varying $n$, is an algebraic analogue of the concept of [[n-fold loop space]]. By means of a suitable [[bar construction]], the [[geometric realization]] of an $n$-fold monoidal category, or rather its [[group completion]], bears a structure of $n$-fold loop space. 

Roughly speaking, the iterative idea is that an $(n+1)$-fold monoidal category is a [[pseudomonoid|(pseudo-)monoid]] in the monoidal $2$-category of $n$-fold monoidal categories and ([[normal lax monoidal functor|normal lax]]) $n$-fold monoidal functors. Were the laxity to be strengthened so that the relevant structure constraints become isomorphisms ([[strong monoidal functor|strong]] $n$-fold monoidal functors), we would get [[braided monoidal categories]] in the case $n = 2$, and [[symmetric monoidal categories]] at $n = 3$ and beyond (in other words, the concept stabilizes at $n = 3$). Without that strengthening, however, we get a new type of structure for each $n$, without [[stabilization]]. 


## Definition 

Let $C$ be a [[2-category]] with [[2-products]]. Form a new 2-category with 2-products $Mon_{lax,norm}(C)$ whose 

* $0$-cells are [[pseudomonoids]] in $C$. 

* $1$-cells are _[[normal lax morphism|normal]]_ lax morphisms of pseudomonoids. 

* $2$-cells are [[monoidal transformations]] between normal lax morphisms of pseudomonoids. 

The $2$-product structure on $Mon(C)$ is inherited from the $2$-product structure of $C$. 

+-- {: .num_def}
###### Definition 
A __$0$-fold monoidal category__ is an ordinary [[category]]; the $2$-category of $0$-fold monoidal categories is [[Cat]]. By [[recursion]], the $2$-category of $n$-fold monoidal categories is $Mon_{norm}(C)$ where $C$ is the $2$-category of $(n-1)$-fold monoidal categories; objects of $Mon_{norm}(C)$ are of course called __$n$-fold monoidal categories__. 
=-- 

## Related pages

* 2-fold monoidal categories are precisely the same as [[normal duoidal categories]].

* [[distributivity for monoidal structures]]

## References 

* Balteanu, Fiedorowicz, Schw&#228;nzl, and Vogt, _Iterated monoidal categories II_, ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.45.290&rep=rep1&type=pdf)).


[[!redirects iterated monoidal category]]
[[!redirects iterated monoidal categories]]
[[!redirects n-fold monoidal category]]
[[!redirects n-fold monoidal categories]]
[[!redirects 2-fold monoidal category]]
[[!redirects 2-fold monoidal categories]]
