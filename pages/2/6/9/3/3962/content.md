
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **local field** is a [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] (non-discrete) [[topological space|topological]] [[field]]. 

## Properties

Any local field is one of the following types: 

* Characteristic zero. In this case local fields $F$ are completions of [[number field]]s with respect to metrics induced by [[valuation]]s. The valuations may be 

  * Archimedean. Here for every $x \in F$, there exists $n \in \mathbb{N}$ such that $\|n x\| \gt 1$, where $\| \cdot \|$ is the valuation. The local fields in this case are isomorphic as topological fields to $\mathbb{R}$ or $\mathbb{C}$. 

  * Nonarchimedean. Such valuations are discrete valuations, and are the completions of discrete valuations induced by prime ideals $v$ of the ring of algebraic integers $\mathcal{O}_k$ in a number field $k$. The valuation on the number field is defined by $\|x\|_v = q^{-n}$ where $q$ is the cardinality of the finite field $\mathcal{O}_k/v$, and $n$ is the least integer such that $x \in v^n$. The completion is called the $v$-**adic completion** and is denoted $k_v$. 

* Characteristic $p \gt 1$. In this case local fields are fields of Laurent series $\mathbb{F}_q((t))$ over a finite field $\mathbb{F}_q$ of cardinality $q = p^n$; here $\|f(t)\| = q^{-n}$ where $f(t) = a_n t^n + a_{n+1}t^{n+1} + \ldots$. The valuation is nonarchimedean. 

Local fields are technically useful in modern number theory; for example in formulating local-to-global principles, and in formulations of class field theory following Tate's thesis. Part of the technical convenience resides in the fact that one can effectively do Fourier analysis on them; as additive topological groups, they are self-dual locally compact abelian groups (in the sense of [[Pontryagin duality]]). 
 

## Relation to local rings

There's not much relation. One can say that the $p$-adic local fields have [[local ring]]s in them: the elements of norm 1 or less, where the maximal ideal is the set of elements of norm less than 1. 

In general, given a local ring $(R, m)$, it's possible to complete it by taking an inverse [[limit]] of the quotient rings $R/m^n$, and the $p$-adic local fields arise as fields of fractions of completions of localizations of rings of integers in number fields. But those local rings coming from number field are a tiny fraction of local rings in general.