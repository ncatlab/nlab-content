
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

The _pro-&#233;tale site_ is a variant of the [[étale site]] where the finitess conditions on the [[fibers]] of [[étale morphisms of schemes|étale morphisms]] is relaxed to a 
[[pro-object|pro-]]finitenss condition ([[pro-étale morphism of schemes|pro-étale morphisms]])

The [[sheaf topos]] over the pro-&#233;tale site might by called the _pro-[[étale topos]]_. Its [[abelian sheaf cohomology]] -- _pro &#233;tale cohomology_ -- improves on that of the original [[étale topos]] in that it genuinely contains ([Bhatt-Scholze 13](#BhattScholze13)) the [[Weil cohomology theory]] called [[ℓ-adic cohomology]] (while over the [[étale site]] this is only given by an [[inverse limit]] of [[abelian sheaf cohomology]]).

## Definition

+-- {: .num_defn}
###### Definition

For $X$ a [[scheme]], its _pro &#233;tale site_ $X_{proet}$ is the [[site]]
whose [[objects]] are [[pro-étale morphisms]] into $X$ and whose [[Grothendieck topology]] is that of the [[fpqc site]].

=--

## Properties

### In terms of weakly &#233;tale maps

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


### Relation to the &#233;tale topos


+-- {: .num_defn}
###### Definition

Since every [[étale morphism of schemes]] is in particular a [[pro-étale morphism of schemes|pro étale morphism]], there is induced a [[geometric morphism]]

$$
  \nu
  \;\colo\;
  Sh(X_{proet})
  \longrightarrow
  Sh(X_{et})
$$

from the [[pro-étale topos]] to the [[étale topos]] of any [[scheme]] $X$.

=--

+-- {: .num_prop}
###### Proposition

$\nu$ is a [[surjective geometric morphism]] with [[full and faithful functor|fully faithful]] [[inverse image]]. Hence the ordinary [[étale topos]] is a [[coreflective subcategory|coreflection]] of the pro-&#233;tale topos.

=--

([Bhatt-Scholze 13, lemma 5.1.2](#BhattScholze13))

## References


The pro-&#233;tale topology was suggested by Scholze and then fully developed in

* Bhargav Bhatt, [[Peter Scholze]], _The pro-&#233;tale topology for schemes_ ([arXiv:1309.1198](http://arxiv.org/abs/1309.1198))
 {#BhattScholze13}

Some results used in the study of weakly &#233;tale maps appeared earlier in

*  [[Ofer Gabber]] and Lorenzo Ramero, _Almost ring theory_, volume 1800 of Lecture Notes in Mathematics. Springer-Verlag, Berlin, 2003. ([arXiv:math/0201175](http://arxiv.org/abs/math/0201175))
 {#GabberRamero03}


Reviews include

* [[The Stacks Project]], [chapter 46](http://stacks.math.columbia.edu/tag/0965) ([pdf](stacks.math.columbia.edu/download/proetale.pdf))


[[!redirects pro-etale site]]

[[!redirects pro-étale sites]]
[[!redirects pro-etale sites]]

[[!redirects pro-étale cohomology]]
[[!redirects pro-etale cohomology]]

[[!redirects pro-étale topos]]
[[!redirects pro-étale toposes]]
[[!redirects pro-etale topos]]
[[!redirects pro-etale toposes]]