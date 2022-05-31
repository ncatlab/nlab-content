
> This entry is about the concept related to [[homotopy pullbacks]]. For a different concept of the same name see at _[[sharp modality]]_.

#Contents#
* table of contents
{:toc}

## Idea

In a [[right proper model category]] a morphism is called _sharp_ if its [[pullback]] along any other morphism is already a [[homotopy pullback]]. In a general [[model category]] a morphism is sharp if all its pullbacks preserve weak equivalences under (further) pullback.

Other terms used for sharp morphisms include _right proper morphism_, _$h$-fibration_, and _$W$-fibration_; see the references.

## Definition

In a [[model category]] $\mathcal{M}$, a **sharp map** is a morphism $p : X \to Y$ satisfying the following condition: for any commutative diagram in $\mathcal{M}$ of the form below,
$$
  \array{
    X'' & \stackrel{f}{\longrightarrow} & X' & \longrightarrow & X \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{p}} \\
    Y'' & \stackrel{g}{\longrightarrow} & Y' & \longrightarrow & Y
  }
$$
if $g \colon Y'' \to Y'$ is a weak equivalence and both squares are pullback diagrams, then  $f \colon X'' \to X'$ is also a weak equivalence.

## Properties

A model category is [[right proper model category|right proper]] if and only if every fibration is sharp. ([Rezk 98, prop. 2.2](#Rezk98))

In a [[right proper model category]], the sharp maps in the full subcategory on sharp-fibrant objects form the fibrations of a [[category of fibrant objects]]. See there the section _[Examples -- Right proper model categories](category+of+fibrant+objects#RightProperModelCategories)_.

## Related concepts

* The dual notion is (most commonly) known as “[[h-cofibration]]”.

## References

The concept was introduced in 

* {#Rezk98} [[Charles Rezk]], _Fibrations and homotopy colimits of simplicial sheaves_ ([arXiv:9811038](http://arxiv.org/abs/math/9811038)), 1998

The terminology arises by dualization of "flat morphism" which was used by Hopkins for the dual concept, which is presumably motivated by the fact that a [[ring homomorphism]] is flat if tensoring with it is exact, hence preserves weak equivalences of [[chain complexes]].

The notion was rediscovered and renamed by various other authors.  In

* [[Andrei Radulescu-Banu]], _Cofibrations in Homotopy Theory_, [arxiv](https://arxiv.org/abs/math/0610009), 2006

it was called a "right proper morphism" (with focus on the dual notion of "left proper morphism"), presumably due to the connection with right proper model categories.  In

* [[Denis-Charles Cisinski]], _Invariance de la K-théorie par équivalences dérivées_, 2010

sharp maps were renamed "weak fibrations".  The authors of

* [[Clark Barwick]] and [[Daniel Kan]], *Quillen Theorems Bn for homotopy pullbacks of (infinity, k)-categories*, [arxiv](https://arxiv.org/abs/1208.1777), 2012

chose instead to rename them to "fibrillations", because it sounds more like "fibration".  Whereas the authors of

* [[Michael Batanin]] and [[Clemens Berger]], _Homotopy theory for algebras over polynomial monads_, [arxiv](https://arxiv.org/abs/1305.0086), 2013

chose to rename the dual notion to "$h$-cofibrations", with reference to the use of that term for the related --- but nevertheless distinct --- notion of [[Hurewicz cofibration]] by [[Peter May]] and collaborators such as [[Johann Sigurdsson]] and [[Kate Ponto]].  In

* [[Dimitri Ara]] and [[Georges Maltsiniotis]], _Towards a Thomason model structure on the category of strict $n$-categories_, [arxiv](https://arxiv.org/abs/1305.5086), 2013

the dual notion was called a "$W$-cofibration", where $W$ is the [[category with weak equivalences|relevant class of weak equivalences]] (note that the definition only depends on the weak equivalences, not the whole model structure); apparently this terminology dates back to unpublished work of Grothendieck.

Some discussion about these various names was had at

* [[Mike Shulman]], _Pullbacks That Preserve Weak Equivalences_, [blog post](https://golem.ph.utexas.edu/category/2014/07/pullbacks_that_preserve_weak_e.html)


[[!redirects sharp maps]]
[[!redirects sharp morphism]]
[[!redirects sharp morphisms]]
[[!redirects W-fibration]]
[[!redirects W-cofibration]]
[[!redirects W-fibrations]]
[[!redirects W-cofibrations]]
