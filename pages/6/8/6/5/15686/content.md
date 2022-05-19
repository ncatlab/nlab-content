
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### For modules over rings

Given a [[ring]] $R$, an element $m$ in an $R$-[[module]] $M$ is **torsion element** if there is a nonzero element $r$ in $R$ such that $r m=0$. In [[constructive mathematics]], given a [[ring]] $R$ with a [[tight apartness relation]] $\#$, an element $m$ in an $R$-[[module]] $M$ is a **torsion element** if there is a element $r$ in $R$ such that $r \# 0$ and $r m=0$. 

A **torsion module** is a module whose elements are all torsion. A [[torsion-free module]] is a module whose elements are not torsion, other than $0$. 

More generally, given an ideal $\mathfrak{a} \subset R$ then an $\mathfrak{a}$-torsion module is one all whose elements are annihilated by some power of elements in $\mathfrak{a}$.

### For $\infty$-modules over $E_\infty$-rings 

Let $A$  be an [[E-∞ ring]] and $\mathfrak{a} \subset \pi_0 A$ a [[generators and relations|finitely generated]] ideal of its underlying [[commutative ring]]. 


+-- {: .num_defn #TorsionInfinityModule}
###### Definition

An $A$-[[∞-module]] $N$ is an _$\mathfrak{a}$-torsion module_ if for all elements $n \in \pi_k N$ and all elements $a \in \mathfrak{a}$ there is $k \in \mathbb{N}$ such that $a^k n = 0$.

=--

([Lurie "Completions", def. 4.1.3](#LurieCompletions)).


+-- {: .num_prop #TorsionApproximation}
###### Proposition

The [[full sub-(∞,1)-category]]

$$
  A Mod_{\mathfrak{a}tor}
  \hookrightarrow
  A Mod
$$

is [[reflective sub-(∞,1)-category|co-reflective]] and the co-reflector $&#643;_{\mathfrak{a}}$ -- the _[[torsion approximation]]_ -- is [[smashing localization|smashing]].

=--

([Lurie "Completions", prop. 4.1.12](#LurieCompletions)).

+-- {: .num_prop}
###### Proposition

For $N \in A Mod_{\leq 0}$ then [[torsion approximation]], prop. \ref{TorsionApproximation}, intuced a [[monomorphism]] on $\pi_0$

$$
  \pi_0 &#643;_{\mathfrak{a}} N \hookrightarrow \pi_0 N
$$

including the $\mathfrak{a}$-nilpotent elements of $\pi_0 N$.

=--

([Lurie "Completions", prop. 4.1.18](#LurieCompletions)).

## Related concdepts

* [[torsion subgroup]]

* [[torsion-free module]]

## References

* {#Quillen96} [[Daniel Quillen]], _Module theory over nonunital rings_, August 1996 ([[QuillenModulesOverRngs.pdf:file]])

* {#LurieCompletions} [[Jacob Lurie]], section 4.1 of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_

[[!redirects torsion modules]]
