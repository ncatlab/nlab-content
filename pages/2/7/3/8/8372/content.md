
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A [[module]] over a [[ring]] whose underlying [[abelian group]] has trivial [[torsion subgroup]] is called _torsion-free_.

## Definition 

### Torsion-free $\mathbb{Z}$-modules

In classical mathematics, a **torsion-free $\mathbb{Z}$-module** or **torsion free [[abelian group]]** $M$ could be defined using a variant of the zero-divisor property characteristic of [[integral domains]]: for all $r$ in $\mathbb{Z}$ and $m$ in $M$, if $r m = 0$, then $r = 0$ or $m = 0$, or the [[contrapositive]], if $r \neq 0$ and $m \neq 0$, then $r m \neq 0$. 

There is also an equivalent definition: a **torsion-free $\mathbb{Z}$-module** $M$ or **torsion free abelian group** is such that right multiplication by $m$ is injective if $m \neq 0$ and left multiplication by $r$ is injective if $r \neq 0$, where "multiplication" refers to the $\mathbb{Z}$-action. 

In [[constructive mathematics]], there are multiple inequivalent ways of defining a torsion-free $\mathbb{Z}$-module. One could define a torsion-free module as a module such that for all $r$ in $\mathbb{Z}$ and $m$ in $M$, if $r m = 0$, then $r = 0$ and $m = 0$. The first definition is valid in all modules with [[decidable equality]], and could be defined using [[coherent logic]], but is not valid for $\mathbb{R}$-modules. 

If the module has a [[tight apartness relation]], then one could define a torsion-free $\mathbb{Z}$-module as a module such that for all $r$ in $\mathbb{Z}$ and $m$ in $M$, if $r \neq 0$ and $m \# 0$, then $r m \# 0$. This is valid in $\mathbb{R}$, but is no longer capable of being defined in coherent logic. Similarly, one could define a torsion-free $\mathbb{Z}$-module $M$ is such that right multiplication by $m$ is injective if $m \# 0$ and left multiplication by $r$ is injective if $r \neq 0$. 

A torsion-free ring is a [[monoid object]] in torsion-free $\mathbb{Z}$-modules. 

### Torsion-free $R$-modules

In classical mathematics, given a [[commutative ring]] $R$, a **torsion-free $R$-module** is a module $M$ such that for all $r$ in $Can(R)$, where $Can(R)$ is the [[multiplicative submonoid of cancellative elements]] in $R$ and $m$ in $M$, if $r m = 0$, then $r = 0$ or $m = 0$. Equivalently, the [[contrapositive]], if $m \neq 0$, then $r m \neq 0$. Some authors require $R$ to be an [[integral domain]], where $Can(R)$ is the monoid of nonzero elements in $R$. 

In [[constructive mathematics]], given a [[ring]] $R$, there are multiple inequivalent ways of defining a torsion-free $R$-module. One could define a torsion-free module as a module such that for all $r$ in $Can(R)$ and $m$ in $M$, if $r m = 0$, then $m = 0$. The first definition is valid in all modules with [[decidable equality]], and could be defined using [[coherent logic]], but is not valid for $\mathbb{R}$-modules. 

If $M$ has a [[tight apartness relations]], then one could define a torsion-free module as a module such that for all $r$ in $Can(R)$ and $m$ in $M$, if $m \# 0$, then $r m \# 0$. This is valid in $\mathbb{R}$-modules, but is no longer capable of being defined in coherent logic. 

A torsion-free $R$-[[associative unital algebra|algebra]] is a [[monoid object]] in torsion-free $R$-modules. 

## Properties

\begin{proposition}
Every [[divisible group|divisible]] torsion-free $\mathbb{Z}$-module is a [[rational vector space]].
\end{proposition}

\begin{proposition}
Every [[integral domain]] $R$ is a torsion-free $R$-module. 
\end{proposition}

## Locality

Being torsion-free is **not** a local property in general.

\begin{proposition}
Let $R$ be a commutative and assume its [[total ring of fractions]] $\mathrm{Q}(R)$ be [[absolutely flat]].
Then for an $R$-module $M$ the following are equivalent :

1. $M$ is torsion-free over $R$ ;
1. $M_\mathfrak{p}$ is torsion-free over $R_\mathfrak{p}$ for every prime ideal $\mathfrak{p} \subset R$ ;
1. $M_\mathfrak{m}$ is torsion-free over $R_\mathfrak{m}$ for every maximal ideal $\mathfrak{m} \subset R$.

\end{proposition}

\begin{proof}
$1 \Rightarrow 2$. Suppose that $M$ is a torsion-free $R$-module and that $\overline{\alpha}\overline{x} = 0$ for a regular $\overline{\alpha} \in R_\mathfrak{p}$ and $\overline{x} \in M_\mathfrak{p}$.
Set $\mathfrak{a}_\mathfrak{p} = \{a ; a s = 0 \quad\text{ for some }\quad s \in R - \mathfrak{p}, a \in R\}$ and $M' = \{m ; s m = 0 \quad\text{ for some }\quad s \in R - \mathfrak{p}, m \in M\}$. Then we may assume that $\overline{\alpha} \in R/\mathfrak{a}_\mathfrak{p}$ and $\overline{x} \in M/M'$ by multiplying suitably elements of $R/\mathfrak{a}_\mathfrak{p} - \mathfrak{p}/\mathfrak{a}_\mathfrak{p}$ to $\overline{\alpha}, \overline{x}$. (...)

$2 \Rightarrow 3$. Obvious.

$3 \Rightarrow 1$. If $r$ is a regular element of $R$ and $x$ is non zero with $r x = 0$, then taking any maximal ideal $(r) \subset \mathfrak{m}$, one gets the same equation in $\overline{r}\overline{x} = 0$ in $M_\mathfrak{m}$. 
\end{proof}

## Related concepts

* [[free module]] $\Rightarrow$ [[projective module]] $\Rightarrow$ [[flat module]] $\Rightarrow$ **torsion-free module**

* [[torsion module]]

* [[integral domain]]

* [[multiplicative submonoid of cancellative elements]]

## References

* Shizuo Endo, On semi-hereditary rings, J. Math. Soc. Japan Vol. 13, No. 2, 1961

See also 

+ Wikipedia, _[Torsion-free module](https://en.wikipedia.org/wiki/Torsion-free_module)_

[[!redirects torsion-free modules]]
[[!redirects torsion free module]]
[[!redirects torsion free modules]]

[[!redirects torsionfree module]]
[[!redirects torsionfree modules]]

[[!redirects torsion free]]
[[!redirects torsion-free]]

[[!redirects torsion-free abelian group]]
[[!redirects torsion-free abelian groups]]
[[!redirects torsion free abelian group]]
[[!redirects torsion free abelian groups]]

[[!redirects torsion-free Z-module]]
[[!redirects torsion-free Z-modules]]
[[!redirects torsion free Z-module]]
[[!redirects torsion free Z-modules]]

[[!redirects torsion-free ring]]
[[!redirects torsion-free rings]]
[[!redirects torsion-free algebra]]
[[!redirects torsion-free algebras]]