

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea ##

A cofunctor is a kind of morphism between [[category|categories]] (not to be confused with a [[contravariant functor]]). In contrast to a [[functor]], the assignment on objects of a cofunctor goes in the _opposite_ direction to the assignment on morphisms. 

Cofunctors generalise both [[bijective on objects functor|bijective-on-objects functors]] and [[discrete fibration|discrete opfibrations]]. 

Cofunctors arise naturally in the study [[internal category in a monoidal category|non-cartesian internal categories]]. 

## Definition ##

A **cofunctor** $\varphi$ from a [[category]] $A$ to a category $B$ consists of a 
map sending each [[object]] $a \in A$ to an object $\varphi_{0}a \in B$ 
and a map sending each pair $(a \in A, u : \varphi_0a \to b)$ to a [[morphism]] $\varphi_{1}(a, u) : a \to a'$ in $A$, where $a$ is an object in $A$ and $u : \varphi_{0}a \to b$ is a morphism in $B$, such that 

* $\varphi_{1}$ respects codomains: $\varphi_{0}a' = cod(u)$ where $a' = cod(\varphi_{1}(a, u))$, 

* $\varphi_{1}$ preserves identity morphisms: $\varphi_{1}(a, 1_{\varphi_{0}a}) = 1_{a}$, 

* $\varphi_{1}$ preserves composition: $\varphi_{1}(a, v \circ u) = \varphi_{1}(a', v) \circ \varphi_{1}(a, u)$ where $a' = cod(\varphi_{1}(a, u))$. 

## References ##

* {#HigginsMackenzie93} [[Philip J. Higgins]], [[Kirill C. H. Mackenzie]], _Duality for base-changing morphisms of vector bundles, modules, Lie algebroids and Poisson structures_, Mathematical Proceedings of the Cambridge Philosophical Society, 114, 1993 ([doi:10.1017/S0305004100071760](http://dx.doi.org/10.1017/S0305004100071760))

* {#Aguiar97} [[Marcelo Aguiar]], _Internal categories and quantum groups_, PhD thesis, Cornell University, 1997 ([pdf](http://pi.math.cornell.edu/~maguiar/thesis2.pdf))

* {#AhmanUustalu17} Danel Ahman, Tarmo Uustalu, _Taking updates seriously_, CEUR Workshop Proceedings, 1827, 2017 ([pdf](http://ceur-ws.org/Vol-1827/paper11.pdf))
