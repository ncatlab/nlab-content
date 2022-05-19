
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

### Torsion-free $\mathbb{Z}$-module

In classical mathematics, a **torsion-free $\mathbb{Z}$-module** $M$ could be defined using a variant of the zero-divisor property characteristic of [[integral domains]]: for all $r$ in $\mathbb{Z}$ and $m$ in $M$, if $r m = 0$, then $r = 0$ or $m = 0$. Equivalently, the contrapositive, if $r \neq 0$ and $m \neq 0$, then $m r \neq 0$. 

In [[constructive mathematics]], there are multiple inequivalent ways of defining a torsion-free $\mathbb{Z}$-module. The first definition is valid in all modules with [[decidable equality]], and could be defined using [[coherent logic]], but is not valid for $\mathbb{R}$. If the module has a [[tight apartness relation]], then one could define a torsion-free $\mathbb{Z}$-module as a module such that for all $r$ in $\mathbb{Z}$ and $m$ in $M$, if $r \neq 0$ and $m \# 0$, then $r m \# 0$. This is valid in $\mathbb{R}$, but is no longer capable of being defined in coherent logic. 

A torsion-free ring is a [[monoid object]] in torsion-free $\mathbb{Z}$-modules. 

### Torsion-free $R$-module

In classical mathematics, given a torsion-free ring $R$, a **torsion-free $R$-module** could be defined using a variant of the zero-divisor property characteristic of [[integral domains]]: for all $r$ in $R$ and $n$ in $\mathbb{Z}$, if $n r = 0$, then $r = 0$ or $m = 0$. Equivalently, the contrapositive, if $r \neq 0$ and $n \neq 0$, then $n r \neq 0$. 

In [[constructive mathematics]], given a torsion-free ring $R$, there are multiple inequivalent ways of defining a torsion-free $R$-module. The first definition is valid in all modules with [[decidable equality]], and could be defined using [[coherent logic]], but is not valid for $\mathbb{R}$-modules. If $R$ and $M$ both have [[tight apartness relations]], then one could define a torsion-free module as a module such that for all $r$ in $R$ and $m$ in $M$, if $r \# 0$ and $m \# 0$, then $r m \# 0$. This is valid in $\mathbb{R}$-modules, but is no longer capable of being defined in coherent logic.  

A torsion-free $R$-[[associative unital algebra|algebra]] is a [[monoid object]] in torsion-free $R$-modules. 

## Related concepts

* [[free module]] $\Rightarrow$ [[projective module]] $\Rightarrow$ [[flat module]] $\Rightarrow$ **torsion-free module**

* [[torsion module]]

* [[integral domain]]

[[!redirects torsion-free modules]]

[[!redirects torsionfree module]]
[[!redirects torsionfree modules]]


[[!redirects torsion-free ring]]
[[!redirects torsion-free rings]]
[[!redirects torsion-free algebra]]
[[!redirects torsion-free algebras]]