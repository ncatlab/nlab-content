
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

### In rings

Let $R$ be a [[ring]]. An element $r \in R$ is **quasiregular** if $1 - r$ is a [[unit]]. $r$ is **left quasiregular** if $1 - r$ is left [[invertible element|invertible]], and $r$ is **right quasiregular** if $1 - r$ is right [[invertible element|invertible]]. 

### In rigs

Let $R$ be a [[rig]]. An element $r \in R$ is **left quasiregular** if one can construct an element $s \in R$ such that $s = s r + 1$. An element $r \in R$ is **right quasiregular** if one can construct an element $s \in R$ such that $s = r s + 1$. An element $r \in R$ is **quasiregular** if it is both left and right quasiregular. If $R$ is a ring, one can show that these conditions is equivalent to $1 - r$ being a unit. 

## Properties

\begin{theorem}
Suppose that addition in a rig $R$ is [[cancellative monoid|cancellative]]. If the multiplicative [[neutral element]] $1 \in R$ is a quasiregular element $R$, then $R$ is the [[trivial rig]].
\end{theorem}

\begin{proof}
Suppose $1 \in R$ is quasiregular. We can construct element $s \in R$ such that $s = s1 + 1$, thus $s = s + 1$. By the cancellative property, we have $1 = 0$, meaning that $R$ is the trivial ring. 
\end{proof}

\begin{lemma}
The only [[ring]] where $1 \in R$ is quasiregular is the [[trivial ring]]. 
\end{lemma}

\begin{theorem}
Every [[nilpotent element]] in a [[ring]] is a [[quasiregular element]]. 
\end{theorem}

\begin{proof}
Given a ring $R$ and an element $x \in R$, if $x$ is nilpotent, then one can construct a natural number $n \in \mathbb{N}$ such that $x^{n + 1} = 0$, and

$$(1 - x)(1 + x + x^2 + \ldots + x^n) = 1 \qquad (1 + x + x^2 + \ldots + x^n)(1 - x) = 1$$ 

which means that $x$ is quasiregular. 
\end{proof}

## Related concepts

* [[quasiregular rig]]

* [[Jacobson radical]]

## References

* Wikipedia, [Quasiregular element](https://en.wikipedia.org/wiki/Quasiregular_element)

[[!redirects quasiregular]]
[[!redirects quasi-regular]]

[[!redirects left quasiregular]]
[[!redirects left quasi-regular]]

[[!redirects right quasiregular]]
[[!redirects right quasi-regular]]

[[!redirects quasiregularity]]
[[!redirects quasi-regularity]]

[[!redirects left quasiregularity]]
[[!redirects left quasi-regularity]]

[[!redirects right quasiregularity]]
[[!redirects right quasi-regularity]]

[[!redirects quasiregular element]]
[[!redirects quasiregular elements]]

[[!redirects left quasiregular element]]
[[!redirects left quasiregular elements]]

[[!redirects right quasiregular element]]
[[!redirects right quasiregular elements]]

[[!redirects quasi-regular element]]
[[!redirects quasi-regular elements]]

[[!redirects left quasi-regular element]]
[[!redirects left quasi-regular elements]]

[[!redirects right quasi-regular element]]
[[!redirects right quasi-regular elements]]