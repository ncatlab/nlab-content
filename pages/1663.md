##Idea#
[[crossed complex|Crossed complexes]] are a useful extension of crossed modules allowing not only the encoding of an algebraic model for the  [[homotopy 2-type]], but also information on the '[[complex of chains on the universal cover]]'.  The category of crossed complexes is a monoidal closed category equivalent to various types of strict infinity groupoid. 

To model the homotopy 3-type of a space, we can use either a [[2-crossed module]] or a [[crossed square]] (or various other algebraic models to be s=added some time in the future). A [[crossed complex]] is a 'hybrid', part [[crossed module]] but with a 'tail' which is a chain complex. What would be the 'hybrid' between a 2-crossed module and a chain complex. Are there examples that are easily constructed? What sort of information do they encode? Are they easy to analyse, understand, ... and useful?

##Definition#
 A _2-crossed complex_ is a [[normal complex   of  groups]]

 $$\ldots \to C_n \stackrel{\partial_n}{\longrightarrow} C_{n-1} \longrightarrow \ldots \longrightarrow C_0,$$

 together with a 2-crossed module structure  given on $C_2\to C_1\to C_0$ by a Peiffer lifting function $\{ -,-\} : C_1\times C_1 \to C_2$, such that, on writing $\pi = Coker(C_1\to C_0)$,

1. each $C_n$, $n\geq 3$ and $Ker \,\partial_2$ are  $\pi$-modules and the $\partial_n$ for $n\geq 4$, together with the codomain restriction of $\partial_3$, are $\pi$-module homomorphisms;

1. the   $ \pi $-module structure on $Ker \partial_2$ is the action  induced from the  $C_0$-action on $C_2$ for which the action of $\partial_1 C_1$ is trivial.

 
 
 A  2-crossed complex morphism is defined in the obvious way, being compatible with all the actions, the pairings and Peiffer liftings.  We will denote by $2-Crs$, the corresponding category. 