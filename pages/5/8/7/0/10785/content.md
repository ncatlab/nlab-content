[[!redirects weakly étale morphism]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A variant of [[étale morphism of schemes]] where the finitess conditions on [[étale morphisms]] are relaxed.

Used in the definition of _[[pro-étale site]]_ and _[[pro-étale cohomology]]_.

## Definition

+-- {: .num_defn #WeaklyEtale}
###### Definition

A [[morphism]] $f \colon X \longrightarrow Y$ of [[schemes]]
is called _weakly &#233;tale_ if 

1. $f$ is a [[flat morphism of schemes]];

1. its [[diagonal]] $X \longrightarrow X \times_Y X$ is also flat.

=--

([Bhatt-Scholze 13, def. 4.1.1](#BhattScholze13))


## Properties

+-- {: .num_prop}
###### Proposition

Every [[weakly étale morphism]] is a [[formally étale morphism]].

=--

([Gabber-Ramero 03, theorem 2.5.36, prop. 3.2.16](#GabberRamero03) [Bhatt-Scholze 13, prop. 2.3.3. (2)](#BhattScholze13))

+-- {: .num_remark}
###### Remark

As discussed there, an [[étale morphism]] is a [[formally étale morphism]] which is [[locally of finite presentation]].

=--

+-- {: .num_cor}
###### Corollary

A [[weakly étale morphism]] which is [[locally of finite presentation]] is an [[étale morphism of schemes|étale morphism]].

[[étale morphism of schemes|étale morphism]] $\Rightarrow$ [[weakly étale morphism of schemes|weakly étale morphism]] $\Rightarrow$ [[formally étale morphism of schemes|formally étale morphism]]

=--

In fact a weakly &#233;tale morphism is equivalently a [[formally étale morphism]] which is "locally [[pro-object|pro-finitely]] presentable" (dually locally of [[ind-object|ind]]-finite rank) in the following sense

+-- {: .num_defn #IndEtale}
###### Definition

For $A \to B$ a [[homomorphism]] of [[rings]], say that it is an **[[ind-étale morphism]]** if that $A$-[[associative algebra|algebra]] $B$ is a [[filtered colimit]] of $A$-[[étale algebras]].

=--

+-- {: .num_prop}
###### Proposition

Let $f \;\colon\; A \longrightarrow B$ be a [[homomorphism]] of [[rings]].

* If $f$ is ind-&#233;tale, def. \ref{IndEtale}, then it is weakly &#233;tale, def. \ref{WeaklyEtale}.

Almost conversely

* If $f$ is weakly &#233;tale, then there is a [[faithfully flat morphism]] $g \colon B \to C$ which is ind-&#233;tale such that the [[composition|composite]] $g\circ f$ is ind-&#233;tale.

=--

([Bhatt-Scholze 13, theorem 1.3](#BhattScholze13))

+-- {: .num_cor}
###### Corollary

The [[sheaf toposes]] over the [[sites]]  of weak &#233;tale morphisms and of [[pro-étale morphisms of schemes]] into  some base [[scheme]] are [[equivalence of categories|equivalent]], both define the  _[[pro-étale topos]]_ over the _[[pro-étale site]]_.

=--

## Related concepts

[[étale morphism of schemes|étale morphism]] $\Rightarrow$ [[pro-étale morphism of schemes|pro-étale morphism]] $\Rightarrow$ [[weakly étale morphism of schemes|weakly étale morphism]] $\Rightarrow$ [[formally étale morphism of schemes|formally étale morphism]]

## References

*  [[Ofer Gabber]] and Lorenzo Ramero, _Almost ring theory_, volume 1800 of Lecture Notes in Mathematics. Springer-Verlag, Berlin, 2003. ([arXiv:math/0201175](http://arxiv.org/abs/math/0201175))
 {#GabberRamero03}

* Bhargav Bhatt, [[Peter Scholze]], _The pro-&#233;tale topology for schemes_ ([arXiv:1309.1198](http://arxiv.org/abs/1309.1198))
 {#BhattScholze13}


[[!redirects weakly étale morphisms]]

[[!redirects weakly etale morphism]]
[[!redirects weakly etale morphisms]]