
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A [[locally small category]] $C$ is **total** if its [[Yoneda embedding]] $C\to [C^{op},Set]$ has a [[adjoint functor|left adjoint]].  If $C^{op}$ is total, $C$ is called **cototal**.

The definition above requires some set-theoretic assumption to ensure that the [[functor category]] $[C^{op},Set]$ exists, but it can be rephrased to say that the [[colimit]] of $Id_C:C\to C$ [[weighted limit|weighted]] by $W$ exists, for any $W:C^{op}\to Set$.  (This still involves [[quantification]] over large objects, however, so some foundational care is needed.)  This version has an evident generalization to [[enriched category|enriched]] categories.

## Properties

* Total categories satisfy a very satisfactory [[adjoint functor theorem]]: any colimit-preserving functor from a total category to a locally small category has a [[right adjoint]].

* Although the definition refers explicitly only to colimits, every total category is also [[complete category|complete]], i.e. has all small limits.  It also has some large limits.  In fact, it has "all possible" large limits that a locally small category can have: if $F\colon D\to C$ is a functor such that $lim_d Hom_C(X,F d)$ is a small set for all $X\in C$, then $F$ has a limit.


## Examples

Any category which is [[monadic]] over [[Set]] is total, as is any category admitting a [[topological functor|topological functor]] to [[Set]].


## References

* [[Max Kelly]], _A survey of totality for enriched and ordinary categories_ ([pdf](http://archive.numdam.org/article/CTGDC_1986__27_2_109_0.pdf))


[[!redirects cototal category]]