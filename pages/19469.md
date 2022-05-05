
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

##Idea 

For any [[2-category]], $K$, there is a 2-category $Adj(K)$ composed of the objects of $K$, [[adjunctions]] in $K$, and adjunction morphisms.

$Adj(Adj(K))$ is formed by the [[adjoint triples]] of $K$.

Morphisms in $Adj(K)$ are 2-functors from [[Adj]] to $K$. The inclusion of $Mnd$, the free monad, in $Adj$ induces a 2-functor from the 2-category of adjunctions in $K$ to the 2-category of monads in $K$. The adjoints to this 2-functor are the [[Kleisli category|Kleisli]] and [[Eilenberg-Moore category|Eilenberg-Moore]] constructions on monads in $K$. 