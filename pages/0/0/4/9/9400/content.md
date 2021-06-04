
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Van Kampen colimits

* table of contents
{: toc}

## Idea

A [[colimit]] in a [[category]] or [[higher category]] is *van Kampen* if it is both [[universal colimit|universal]] (i.e. [[pullback-stability|stable]] under [[pullback]]) and satisfies [[descent]].  Many [[exactness properties]] can be phrased in terms of certain colimits being van Kampen.

## Definition

Let $C$ be a [[category]] with [[pullbacks]].
Then there is a (pseudo) [[2-functor]]
$$ S : C^{op} \to Cat $$
defined by $S(x) \coloneqq C/x$ (the [[slice category]]), called the [[self-indexing]] of $C$.  Its [[Grothendieck construction]] is the [[codomain fibration]].

+-- {: .num_defn}
###### Definition
A [[colimit]] in $C$ is **van Kampen** if it is [[preserved limit|preserved]] by the functor $S$, i.e. it is taken to a (weak) [[2-limit]] in $Cat$.
=--


### Universality and descent

Let $G:D\to C$ be a diagram with colimit $x$.  Let $D'$ denote the category $D$ with a new [[terminal object]] adjoined, and $G':D'\to C$ the extension of $D$ by the colimiting cocone with vertex $x$.

+-- {: .num_theorem #UniversalityAndDescent}
###### Theorem
Suppose $C$ has all colimits of $D$-shaped diagrams.  Then the colimit $x$ of $G:D\to C$ is van Kampen if and only if the following condition holds: for any diagram $F':D'\to C$ and natural transformation $\alpha':F'\to G'$ whose restriction $\alpha:F\to G$ to $D\subset D$ is [[equifibered natural transformation|equifibered]], the following are equivalent:

1. $\alpha'$ is equifibered.
1. $F'$ is a colimiting cocone.
=--
+-- {: .proof}
###### Proof
First note that the 2-limit of $S\circ G$ is equivalent to the full subcategory of $[D,C]/G$ consisting of the equifibered transformations.  We denote this category by $([D,C] \Downarrow G)$.  Moreover, under this equivalence, the comparison map $S(x) \to \lim (S\circ G)$ is identified with the pullback functor
$$ C/x \to ([D,C] \Downarrow G). $$
Now this functor has a left adjoint given by taking colimits.  Thus, it is an equivalence if and only if the unit and counit of the adjunction are isomorphisms.

The unit is the map from an equifibered transformation over $G$ into the pullback of its colimit.  The latter underlies an equifibered $\alpha'$ by construction, so the unit is an isomorphism just when (2)$\Rightarrow$(1).  Similarly, the counit is the map into an object over $x$ from the colimit of its pullback.  Thus, it is an isomorphism just when (1)$\Rightarrow$(2).
=--

The condition (1)$\Rightarrow$(2) is precisely the statement that the colimit of $G$ is [[universal colimit|universal]], i.e. preserved by pullback.  The condition (2)$\Rightarrow$(1) is a form of [[descent]].

### Colimits in Span

+-- {: .num_theorem #ColimitsInSpan}
###### Theorem
A colimit in $C$ is van Kampen if and only if it is preserved by the inclusion $C\to Span(C)$ into the [[bicategory]] of [[spans]] in $C$.
=--
+-- {: .proof}
###### Proof
See ([SH](#SH)).
=--

## Examples

* A category with pullbacks is [[lextensive category|lextensive]] just when [[coproducts]] are van Kampen.

* A category with pullbacks is [[adhesive category|adhesive]] just when [[pushouts]] of [[monomorphisms]] are van Kampen.

* A category with pullbacks is [[exhaustive category|exhaustive]] just when transfinite unions of monomorphisms are van Kampen.

* In $Set$, the [[pushout]] square
  $$\array{ 2 & \to & 1 \\ \downarrow && \downarrow \\ 1 & \to & 1 }$$
  is not van Kampen.

## In higher categories 
 {#InHigherCategories}

There is an evident generalization of the definition to [[higher category theory|higher categories]], and in particular to [[(∞,1)-categories]].  In the latter case, van Kampen colimits exactly characterize descent.  In particular,we have:

* A [[locally presentable (∞,1)-category]] is an [[(∞,1)-topos]] just when *all* colimits are van Kampen.

If we take Theorem \ref{UniversalityAndDescent} as the definition of "van Kampen colimit", this follows from Theorem 6.1.3.9 of [[HTT]], see also around ([[(infinity,2)-Categories and the Goodwillie Calculus|Lurie 2Cats+Goodwillie, example 1.2.3]]).  The $(\infty,1)$-categorical version of Theorem \ref{UniversalityAndDescent} may not exactly be in the literature, however.  The cited theorem of HTT essentially gives Theorem \ref{UniversalityAndDescent} under the additional global hypothesis that all colimits in $C$ are universal.

In this case, being van Kampen is also equivalent to being preserved by the composite of $S$ with the [[core]] functor $Core : (\infty,1)Cat \to \infty Gpd$.  Thus, the [[adjoint functor theorem]] implies that (assuming all colimits to be universal), all colimits are van Kampen just when all small versions of $Core \circ S$ are [[representable functor|representable]], i.e. when [[object classifiers]] exist.


## Related pages

* [[exactness property]]
* [[object classifier in an (∞,1)-topos]]
* [[descent]] / [[universal colimit]]


## References

* Pawel Sobocinski and Tobias Heindel, *Being Van Kampen is a universal property*, [arXiv:1101.4594](http://arxiv.org/abs/1101.4594)
{#SH}

[[!redirects van Kampen colimits]]
