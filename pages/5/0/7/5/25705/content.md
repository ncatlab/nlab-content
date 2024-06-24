
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


\tableofcontents


## Idea
 {#Idea}

In variation of the standard definition of *[[topological spaces]]*, a **$\sigma$-topological space** is a [[set]] $X$ equipped with a **$\sigma$-topology**: a collection $O(X)$ of [[subsets]] of $X$, called *[[open sets]]*, which is closed under 

1. [[finite limit|finite]]$\;$[[intersections]],

1. [[countable]]$\;$[[unions]].

(the difference being that for an ordinary [[topological spaces|topology]] one requires closure under arbitrary [[unions]], see [there](topological+space#TheStandardDefinition)).

The [[open sets]] $O(X)$ of a **$\sigma$-topological space** form a *[[sigma-frame|$\sigma$-frame]]*. 

An example of a $\sigma$-topological space is a [[sigma-algebra|$\sigma$-algebra]], whose collection $O(X)$ is also closed under [[complements]] and countable intersections. Another example of a $\sigma$-topological space is a [[zero-set structure]]. 

## Properties

\begin{theorem}
Let $X = \prod_{n \to \alpha} X_n$ be an internal set, and let $\mathcal{F}_X$ be the collection of all subsets of $X$ that can be expressed as the union of at most countably many internal subsets of $X$. Then $(X, \mathcal{F}_X)$ is a [[countably compact]] [[T_1-topological space|$T_1$]] $\sigma$-topological space.
\end{theorem}

## Related concepts

* [[topological space]]
 
* [[sigma-frame]]

* [[sigma-locale]]

* [[sigma-algebra]]

* [[zero-set structure]]

* [[countably compact space]]

* [[first countable space]]

## References

* Fedor Petrov, *"countable" topology*, MathOverflow (2014) &lbrack;[MO:q/173255](https://mathoverflow.net/q/173255/381)&rbrack;

* Balazs Szegedy, *Gowers norms, regularization and limits of functions on abelian groups* &lbrack;[arXiv:1010.6211](https://arxiv.org/abs/1010.6211)&rbrack;

* Vitaly Bergelson, [[Terence Tao]], *Multiple recurrence in quasirandom groups*, Geom. Funct. Anal. **24** (2014) 1–48 &lbrack;[arXiv:1211.6372](https://arxiv.org/abs/1211.6372), [doi:10.1007/s00039-014-0252-0](https://doi.org/10.1007/s00039-014-0252-0)&rbrack;


[[!redirects sigma-topology]]
[[!redirects sigma-topologies]]

[[!redirects sigma-topological space]]
[[!redirects sigma-topological spaces]]

