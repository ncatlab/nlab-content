
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

In classical mathematics, a **torsion-free module** could be defined using a variant of the zero-divisor property characteristic of [[integral domains]]: for all $r$ in $R$ and $m$ in $M$, if $r m = 0$, then $r = 0$ or $m = 0$. Equivalently, the contrapositive, if $r \neq 0$ and $m \neq 0$, then $r m \neq 0$. 

In [[constructive mathematics]], there are multiple inequivalent ways of defining a torsion-free module. The first definition is valid in all modules with [[decidable equality]], and could be defined using [[coherent logic]], but is not valid for $\mathbb{R}$-modules. If the module has a [[tight apartness relation]], then one could define a torsion-free module as a module such that for all $r$ in $R$ and $m$ in $M$, if $r \# 0$ and $m \# 0$, then $r m \# 0$. This is valid in $\mathbb{R}$-modules, but is no longer capable of being defined in coherent logic. 

## Examples 

Every [[integral domain]] $R$ is a torsion-free $R$-module. 

## Related concepts

* [[free module]] $\Rightarrow$ [[projective module]] $\Rightarrow$ [[flat module]] $\Rightarrow$ **torsion-free module**

* [[torsion module]]

* [[integral domain]]

[[!redirects torsion-free modules]]

[[!redirects torsionfree module]]
[[!redirects torsionfree modules]]

