
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
=--
=--

\tableofcontents

## Definition

Since every [[ordered local ring]] $R$ has [[characteristic zero]], the positive integers $\mathbb{Z}_+$ are a subset of $R$, with [[injection]] $i:\mathbb{Z}_+ \hookrightarrow R$. An **Archimedean ordered local ring** is an [[ordered local ring]] which satisfies the [[archimedean property]]: for all elements $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then there exists a positive integer $n \in \mathbb{Z}_+$ such that such that $a \lt i(n) \cdot b$. 

Unlike [[Archimedean ordered fields]], which require arithmetic [[Heyting pretoposes]], Archimedean ordered local rings are definable in any [[arithmetic pretopos]]. 

## In analysis

Archimedean ordered local rings are important for modeling notions of [[infinitesimals]]. These include the dual numbers, which represent nilsquare infinitesimals and are used to synthetically define [[differentiable functions]] in the real numbers, Archimedean ordered Weil rings, which represent nilpotent infintiesimals and are used to synthetically define [[smooth functions]] in the real numbers, as well as [[formal power series]] on the [[ground ring]], which represent infinitesimals which are not nilpotent and are used to synthetically define [[analytic functions]] in the real numbers. 

### Kock-Lawvere axiom

An Archimedean ordered local ring $R$ satisfies the *[[Kock-Lawvere axiom]]* if and only if given any Weil $R$-algebra $W$, the canonical function from $W$ to $R^{\mathrm{spec}_R^W}$ the [[function algebra]] with [[domain]] the [[formal spectrum]] of $W$ and codomain $R$ is an $R$-algebra [[isomorphism]]. 

## See also

* [[Archimedean ordered field]]
* [[ordered local ring]]
* [[Archimedean ordered Artinian local ring]]
* [[Archimedean ordered reduced local ring]]
* [[Archimedean ordered local integral domain]]

## References

* [[Ieke Moerdijk]], [[Gonzalo E. Reyes]]: **Models for Smooth Infinitesimal Analysis**, Springer (1991), [doi:10.1007/978-1-4757-4143-8](https://link.springer.com/book/10.1007/978-1-4757-4143-8)

[[!redirects Archimedean ordered local ring]]
[[!redirects Archimedean ordered local rings]]

[[!redirects archimedean ordered local ring]]
[[!redirects archimedean ordered local rings]]

[[!redirects Archimedean local ring]]
[[!redirects Archimedean local rings]]

[[!redirects archimedean local ring]]
[[!redirects archimedean local rings]]

