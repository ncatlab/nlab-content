
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

The _pro-&#233;tale site_ is a variant of the [[étale site]] where the finiteness conditions on the [[fibers]] of [[étale morphisms of schemes|étale morphisms]] is relaxed to a 
[[pro-object|pro-]]finiteness condition ([[pro-étale morphism of schemes|pro-étale morphisms]])

The [[sheaf topos]] over the pro-&#233;tale site might be called the _pro-[[étale topos]]_. Its [[abelian sheaf cohomology]] -- _pro-&#233;tale cohomology_ -- improves on that of the original [[étale topos]] in that it genuinely contains ([Bhatt-Scholze 13](#BhattScholze13)) the [[Weil cohomology theory]] called [[ℓ-adic cohomology]] (while over the [[étale site]] this is only given by an [[inverse limit]] of [[abelian sheaf cohomology]]).

## Definition

+-- {: .num_defn}
###### Definition

For $X$ a [[scheme]], its _pro-&#233;tale site_ $X_{proet}$ is the [[site]]
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

For $X$ a [[scheme]], its _pro-&#233;tale site_ $X_{proet}$ is the [[site]]
whose [[objects]] are [[weakly étale morphisms]] into $X$ (hence weakly &#233;tale $X$-schemes) and whose [[Grothendieck topology]] is that of the [[fpqc site]].

=--

([Bhatt-Scholze 13, def. 4.1.1](#BhattScholze13))

### Generation by w-contractible rings

+-- {: .num_defn #wContractible}
###### Definition

A [[commutative ring]] $R$ is a **[[w-contractible ring]]** if every [[faithfully flat morphism|faithfully flat]] [[pro-étale morphism]] $Spec A \to Spec R$ has a [[section]].

=--

([Bhatt-Scholze 13, def. 2.4.1](#BhattScholze13))

+-- {: .num_prop}
###### Proposition

For every [[commutative ring]] $R$, there is a a w-contractible $A$, def. \ref{wContractible},
equipped with a [[faithfully flat morphism|faithfully flat]] [[pro-étale morphism]] $Spec A \to Spec R$.

=--

([Bhatt-Scholze 13, lemma 2.4.9](#BhattScholze13))

+-- {: .num_remark}
###### Remark

So the [[full subcategory]] on the [[w-contractible rings]] forms a [[dense subsite]] of the pro-&#233;tale site, consisting of objects with pro-[[étale homotopy type]] a set.

=--

### Relation to the &#233;tale topos


+-- {: .num_defn}
###### Definition

Since every [[étale morphism of schemes]] is in particular a [[pro-étale morphism of schemes|pro-étale morphism]], there is induced a [[geometric morphism]]

$$
  \nu
  \;\colon\;
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


## Examples

Given a [[field]] $k$ with [[separable closure]] $\overline{k}$, then the pro-etale site of $Spec(\overline{k})$ is equivalently the category of [[profinite sets]]. The pro-etale site of $Spec(k)$ identifies with the category of profinite continuous $G$-sets. ([Bhatt-Scholze 13, example 4.1.10](#BhattScholze13)).




## Related concepts

* [[étale homotopy]]

* [[étale cohomology]]

* [[condensed set]]

* [[condensed cohesion]]

## References


The pro-&#233;tale topology was suggested by Scholze and then fully developed in

* {#BhattScholze13} [[Bhargav Bhatt]], [[Peter Scholze]], _The pro-&#233;tale topology for schemes_ Ast&#233;risque No. 369 (2015), 99&#8211;201([arXiv:1309.1198](http://arxiv.org/abs/1309.1198))
 

Some results used in the study of weakly &#233;tale maps appeared earlier in

* {#GabberRamero03} [[Ofer Gabber]] and Lorenzo Ramero, _Almost ring theory_, volume 1800 of Lecture Notes in Mathematics. Springer-Verlag, Berlin, 2003. ([arXiv:math/0201175](http://arxiv.org/abs/math/0201175))
 

A textbook account is in 

* {#StacksProjectProEtaleCohomology} [[The Stacks Project]], _[Pro-&#233;tale Cohomology](http://stacks.math.columbia.edu/tag/0965)_ ([pdf](http://stacks.math.columbia.edu/download/proetale.pdf))


Further developments include

* Takashi Suzuki, _Duality for local fields and sheaves on the category of fields_ ([arXiv:1310.4941](http://arxiv.org/abs/1310.4941))

[[!redirects pro-etale site]]

[[!redirects pro-étale sites]]
[[!redirects pro-etale sites]]

[[!redirects pro-étale cohomology]]
[[!redirects pro-etale cohomology]]

[[!redirects pro-étale topos]]
[[!redirects pro-étale toposes]]
[[!redirects pro-etale topos]]
[[!redirects pro-etale toposes]]

[[!redirects proetale site]]
[[!redirects proetale sites]]
[[!redirects proetale topos]]
[[!redirects proetale toposes]]
[[!redirects proetale topoi]]
