
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### [[categories of categories - contents|categories of categories]]
+-- {: .hide}
[[!include categories of categories - contents]]
=--
=--
=--



**$(\infty,1)Cat$** is the [[(∞,2)-category]] of all small [[(∞,1)-categories]].

Its full [[subcategory]] on [[∞-groupoid]]s is [[∞Grpd]].

#Contents#
* table of contents
{:toc}

## The $(\infty,2)$-category 

### As an $SSet$-category

One incarnation of [[(∞,2)-categories]] is given by [[quasi-category]]-enriched categories (see there for details). As such $(\infty,1)Cat$ is the full [[SSet]]-[[enriched category|enriched]] [[subcategory]] of [[SSet]] on those [[simplicial set]]s that are [[quasi-categories]]. By the fact described at [[(∞,1)-category of (∞,1)-functors]] this is indeed a [[quasi-category]]-enriched category.

### As an enriched model category

The [[model category]] presenting this [[(∞,2)-category]] is the Joyal [[model structure for quasi-categories]] $sSet_{Joyal}$. Its full [[sSet]]-[[subcategory]] is the [[quasi-category]] enriched category of quasi-categories from above.

## The $(\infty,1)$-category

Sometimes it is useful to consider inside the full $(\infty,2)$-catgeory of $(\infty,1)$-categories just the maximal $(\infty,1)$-category and discarding all non-invertible [[k-morphism|2-morphisms]]. This is the [[(∞,1)-category of (∞,1)-categories]].

### As an $SSet$-category

As an [[SSet]]-[[enriched category]] the [[(∞,1)-category of (∞,1)-categories]] is obtained from the quasi-category-enriched version by picking in each [[hom-object]] simplicial set of $(\infty,1)Cat$ the maximal [[Kan complex]]. 


### As an enriched model category

One [[model category]] structure presenting this is the [[model structure on marked simplicial over-sets|model structure on marked simplicial sets]]. As a plain [[model category]] this is [[Quillen equivalence|Quillen equivalent]] to $sSet_{Joyal}$, but as an [[enriched model category]] it is $sSet_{Quillen}$ enriched, so that its full [[SSet]]-subcategory on fibrant-cofibrant objects presents the $(\infty,1)$-category of $(\infty,1)$-categories.

### Properties

#### Limits and colimits in $(\infty,1)$Cat
 {#LimitsAndColimits}

[[limit in a quasi-category|Limits and colimits]] over a [[(∞,1)-functor]] with values in $(\infty,1)Cat$ may be reformulation in terms of the  [[universal fibration of (infinity,1)-categories]] $Z \to (\infty,1)Cat^{op}$ 

Then let $X$ be any [[(∞,1)-category]] and

$$
  F : X \to (\infty,1)Cat
$$

an [[(∞,1)-functor]]. Recall that the [[Cartesian fibration|coCartesian fibration]] $E_F \to X$ classified by $F$ is the pullback of the [[universal fibration of (∞,1)-categories]] $Z$ along F:

$$
  \array{
    E_F &\to& Z
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{F}{\to}& (\infty,1)Cat
  }
$$

+-- {: .un_prop }
###### Proposition

Let the assumptions be as above. Then:

* The colimit of $F$ is equivalent to $E_F$:

  $$
    E_F \simeq colim F
  $$

* The limit of $F$ is equivalent to the [[(infinity,1)-category of cartesian section]] of $E_F \to X$

  $$
    \Gamma_X(E_F) \simeq lim F
    \,.
  $$

=-- 

+-- {: .proof}
###### Proof

This is [[Higher Topos Theory|HTT, section 3.3]].

=--





#### Automorphisms
 {#Automorphisms}

+-- {: .un_theorem }
###### Theorem

The full subcategory of the [[(∞,1)-category of (∞,1)-categories]] $Func((\infty,1)Cat, (\infty,1)Cat)$ on those [[(∞,1)-functor]]s that are equivalences is equivalent to $\{Id, op\}$: it contains only the identity functor and the one that sends an $(\infty,1)$-category to its [[opposite (infinity,1)-category]].

=--

+-- {: .proof}
###### Proof

This is due to

* [[Bertrand Toen]],  _Vers une axiomatisation de la th&#233;orie des cat&#233;gories sup&#233;rieures_ , K-theory 34 (2005), no. 3,
233-263.

It appears as [[Higher Topos Theory|HTT, theorem 5.2.9.1]] ([arxiv v4+](http://arxiv.org/abs/math.CT/0608040) only)

First of all the statement is true for the ordinary category of [[poset]]s. This is [prop. 5.2.9.14](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=311).

From this the statement is deduced for $(\infty,1)$
-categories by observing that posets are characterized by the fact that two parallel functors into them that are objectwise equivalent are already equivalent, [prop. 5.2.9.11](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=310), which means that posets $C$ are characterized by the fact that

$$
  \pi_0 (\infty,1)Cat(D,C)
  \to 
  Hom_{Set}(
   \pi_0 (\infty,1)Cat(*,D)
   ,
   \pi_0 (\infty,1)Cat(*,C)
  )
$$

is an injection for all $D \in (\infty,1)Cat$.

This is preserved under automorphisms of $(\infty,1)Cat$, hence any such automorphism preserves posets, hence restricts to an automorphism of the category of posets, hence must be either the identity or $(-)^{op}$ there, by the above statement for posets.

Now finally the main point of the proof is to see that the linear posets $\Delta \subset (\infty,1)Cat$ are [[dense functor|dense]] in $(\infty,1)Cat$, i.e. that the identity transformation of the inclusion functor $\Delta \hookrightarrow (\infty,1)Cat$ exhibits $Id_{(\infty,1)Cat}$ as the left [[Kan extension]]

$$
  \array{
    \Delta &\hookrightarrow& (\infty,1)Cat
    \\
    \downarrow & \nearrow_{Lan = \mathrlap{Id}}
    \\
    (\infty,1)Cat
  }
  \,.
$$



=--

## Presentations

[[!include table - models for (infinity,1)-operads]]

## Related concepts

* [[Pos]]

* [[Set]]

* [[Grpd]], [[∞Grpd]]

* [[Cat]], [[Operad]]

* [[2Cat]]

* **$(\infty,1)$Cat**, [[(∞,1)Operad]]

  * [[homotopy 2-category of (∞,1)-categories]]

* [[(∞,n)Cat]]

* [[(infinity, 1)Prof]]

category: category

[[!redirects (∞,1)Cat]]

[[!redirects (∞,1)Categories]]
[[!redirects (infinity,1)Categories]]

