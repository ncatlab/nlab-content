# Monadic decompositions

* table of contents
{: toc}

## Idea

Suppose $F_1: C_1 \rightleftarrows D : U_1$ is an [[adjunction]], with induced [[monad]] $T_1 = U_1 F_1$ on $C_1$.  Then we can form the [[Eilenberg-Moore category]] $C_2 \coloneqq C_1^{T_1}$, and the comparison functor $U_2 : D \to C_2$.  If $D$ has [[reflexive coequalizers]], then $U_2$ has a left adjoint $F_2$, with induced monad $T_2 = U_2 F_2$ on $C_2$, and we can iterate.

If $D$ is moreover [[cocomplete category|cocomplete]], we can pass to limits and obtain a tower of adjunctions indexed by all [[ordinal numbers]].  If this tower converges (which happens, for instance, if $D$ is [[well-copowered category|well-copowered]]), then it factors the original adjunction into an adjunction $F_\infty : C_\infty \rightleftarrows D : U_\infty$ that is a [[reflection]] (i.e. the induced monad $T_\infty = U_\infty F_\infty$ on $C_\infty$ is the identity) followed by an adjunction $C_1 \rightleftarrows C_\infty$ whose right adjoint $C_\infty \to C_1$ is a [[transfinite composite]] of [[monadic functors]], hence in particular [[faithful functor|faithful]] and [[conservative functor|conservative]].  This is called a/the **monadic decomposition** of the original adjunction, and produces a [[factorization system on a 2-category|factorization system]] on a suitable 2-category.

## References

* Applegate and Tierney, *Iterated cotriples*, [springerlink](https://link.springer.com/chapter/10.1007%2FBFb0060440)

* MacDonald and Stone, *The tower and regular decompositions*, [numdam](http://www.numdam.org/item/CTGDC_1982__23_2_197_0)

* Adamek and Herrlich and Tholen, *Monadic decompositions*, [sciencedirect](https://www.sciencedirect.com/science/article/pii/0022404989901291)


[[!redirects monadic decompositions]]
[[!redirects iterated monads]]
[[!redirects iterated comonads]]
