
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
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A variant of the [[étale site]] where the finitess conditions on [[étale morphisms]] are relaxed.

The resulting [[abelian sheaf cohomology]] -- _pro &#233;tale cohomology_ -- has a good relation to [[ℓ-adic cohomology]].

## Definition

+-- {: .num_defn}
###### Definition

A [[morphism]] $f \colon X \longrightarrow Y$ of [[schemes]]
is called _weakly &#233;tale_ if 

1. $f$ is a [[flat morphism of schemes]];

1. its [[diagonal]] $X \longrightarrow X \times_Y X$ is also flat.

=--

([Bhatt-Scholze 13, def. 4.1.1](#BhattScholze13))

+-- {: .num_defn}
###### Definition

For $X$ a [[scheme]], its _pro &#233;tale site_ $X_{proet}$ is the [[site]]
whose [[objects]] are [[weakly étale morphisms]] into $X$ (hence weakly &#233;tale $X$-schemes) and whose [[Grothendieck topology]] is that of the [[fpqc site]].

=--

([Bhatt-Scholze 13, def. 4.1.1](#BhattScholze13))


## Properties

+-- {: .num_prop}
###### Proposition

Every [[weakly étale morphism]] is a [[formally étale morphism]].

=--

([Gabber-Ramero 03, theorem 2.5.36, prop. 3.2.16](#GabberRamero03) [Bhatt-Scholze 13, prop. 2.3.3. (2)](#BhattScholze13))


+-- {: .num_cor}
###### Corollary

A [[weakly étale morphism]] which is [[locally of finite presentation]] is an [[étale morphism of schemes|étale morphism]].


=--


## References

*  [[Ofer Gabber]] and Lorenzo Ramero, _Almost ring theory_, volume 1800 of Lecture Notes in Mathematics. Springer-Verlag, Berlin, 2003. ([arXiv:math/0201175](http://arxiv.org/abs/math/0201175))
 {#GabberRamero03}

The pro-&#233;tale topology was suggested by Scholze and then fully developed in

* Bhargav Bhatt, [[Peter Scholze]], _The pro-&#233;tale topology for schemes_ ([arXiv:1309.1198](http://arxiv.org/abs/1309.1198))
 {#BhattScholze13}



Reviews include

* [[The Stacks Project]], [chapter 46](http://stacks.math.columbia.edu/tag/0965) ([pdf](stacks.math.columbia.edu/download/proetale.pdf))


[[!redirects pro-etale site]]

[[!redirects pro-étale sites]]
[[!redirects pro-etale sites]]

[[!redirects pro-étale cohomology]]
[[!redirects pro-etale cohomology]]