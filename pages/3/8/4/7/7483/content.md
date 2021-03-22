
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[monoidal model category]] $\mathbf{S}$ with extra properties guaranteeing a particularly good [[homotopy theory]] of $\mathbf{S}$-[[enriched categories]] is referred to in ([Lurie](#Lurie)) as an _excellent model category_.

(The term _excellent model category_ has also been used by [Lumsdaine and Shulman](#LumsdaineShulman) for a slightly different notion; see [[type-theoretic model category]].  This article is about Lurie’s sense.)

## Definition

+-- {: .num_defn }
###### Definition

Let $\mathbf{S}$ be a symmetric [[monoidal model category]]. It is called __excellent__ if

* it is a [[combinatorial model category]];

* the class of [[weak equivalences]] is stable under [[filtered colimits]];

* every monomorphism is a cofibration (hence in particular all objects are [[cofibrant]]);

* the class of cofibrations is closed under [[products]];

=--

This is ([Lurie, def. A.3.2.16](#Lurie)), except that he also includes the "invertibility hypothesis" ([see below](#InvertibilityHypothesis)).

## Examples

* The [[classical model structure on simplicial sets]].

* Any symmetric monoidal, locally presentable category with its [[trivial model structure]].

* The Cartesian model structure on [[marked simplicial sets]], with the cartesian product.

* The [[model structure for quasi-categories]] on simplicial sets.


## Properties

* One of Lurie's important original theorems was that if $\mathbf{S}$ is an excellent model category, $\mathbf{A}$ is a [[combinatorial model category|combinatorial]] $\mathbf{S}$-[[enriched model category]], and $C$ is a small $\mathbf{S}$-[[enriched category]], then the category $[C,\mathbf{A}]$ of enriched functors has both a [[projective model structure]] and an [[injective model structure]], which are both combinatorial.  However, it has since been shown by [MR13, Remark 3.8](#MR13) that excellence is unnecessary for this result.


## The invertibility hypothesis {#InvertibilityHypothesis}

[Lurie](#Lurie) originally included the an additional condition in the definition, called the **invertibility hypothesis**.  Fortunately, it was shown later by [Lawson](#Lawson) that the invertibility hypothesis is redundant: any model category satisfying the other axioms of an excellent model category always satisfies the invertibility hypothesis.

### Description of the invertibility hypothesis

The invertibility hypothesis states:

* for any homotopy equivalence $f$ in an $\mathbf{S}$-[[enriched category]] $C$, the localization functor $C \to C[f^{-1}]$ is a weak equivalence of $\mathbf{S}$-enriched categories.

The invertibility hypothesis requires some more explanation.  Firstly, by a "homotopy equivalence" we mean a morphism that becomes an isomorphism in the homotopy category $h C$, which is defined by applying to the hom-objects of $C$ the monoidal localization functor $\mathbf{S}\to h \mathbf{S}$ from $\mathbf{S}$ to its [[homotopy category]] (defined in the usual way for a model category by inverting its weak equivalences).  This makes $h C$ an $h \mathbf{S}$-enriched category, and we ask that $f$ be invertible in the underlying ordinary category of $h C$.

Secondly, by $C[f^{-1}]$ we mean a *homotopy invariant* notion of "localization".  One way to define this is to assume that $f$ is classified by a functor $[f]:\mathbf{2}_{\mathbf{S}} \to C$ that is a [[cofibration]] in the [[model structure on enriched categories]], where $\mathbf{2}_{\mathbf{S}}$ denotes the $\mathbf{S}$-enriched [[interval category]], and take the ordinary localization which can be defined as a pushout
$$\array{ \mathbf{2}_{\mathbf{S}} & \xrightarrow{[f]} & C \\ \downarrow && \downarrow \\ \mathbf{2}^\cong_{\mathbf{S}} & \to & C\langle f^{-1}\rangle.}$$
Here $\mathbf{2}^\cong_{\mathbf{S}}$ denotes the 2-object contractible groupoid regarded as an $\mathbf{S}$-category.  Another way to define it (without this assumption on $f$) is to factor the functor $\mathbf{2}_{\mathbf{S}}\to \mathbf{2}^\cong_{\mathbf{S}}$ through a cofibration $\mathbf{2}_{\mathbf{S}}\to E$ and weak equivalence $E\to \mathbf{2}^\cong_{\mathbf{S}}$ in the [[model structure on enriched categories]], and take the ordinary pushout
$$\array{ \mathbf{2}_{\mathbf{S}} & \xrightarrow{[f]} & C \\ \downarrow && \downarrow \\ E & \to & C[f^{-1}].}$$

Finally, by a "weak equivalence of $\mathbf{S}$-enriched categories" we mean a weak equivalence in the [[model structure on enriched categories]].


### Simplicial sets satisfy the invertibility hypothesis

We [Lurie](#Lurie) says (A.3.2.18) that this is "one of the main theorems" of [DK80](#DwyerKanLocalizations), but some further details may be helpful to understand how this comes about.  Note that this proof is not subsumed by Lawson's proof that all excellent model categories satisfy the invertibility hypothesis; instead Lawson *uses* this theorem to transfer the property from simplicial sets to all others excellent model categories.

The relevant theorem appears to be Proposition 10.4 of [DK80](#DwyerKanLocalizations) which states

> Let $V\to B\in \mathrm{s} O-Cat$ be a strong cofibration.  Then the induced map $B\to B[V^{-1}]$ is a weak equivalence if and only if every map of $\pi_0 B$ which is in the image of $\pi_0 V$ is invertible.

Here $\mathrm{s} O-Cat$ is the category of simplicially enriched categories with a fixed object set $O$.  Thus this proposition does not apply as written to the map $[f] : \mathbf{2}_{\mathbf{S}}\to C$ from the invertibility hypothesis, since it is not a bijection on objects.  Instead we have to replace $\mathbf{2}_{\mathbf{S}}$ by a simplicially enriched category $\mathbf{2}_{\mathbf{S},O}$ with set of objects $O = ob(C)$ in which the only nonidentity morphism "is" $f$.  Note that $[f]$ being a cofibration implies that it is injective on objects, so that $f$ has distinct domain and codomain; thus in $\mathbf{2}_{\mathbf{S},O}$ the unique nonidentity morphism is not an endomorphism and hence we don't have to worry about any nontrivial composites.

Now the construction of $B[V^{-1}]$ in [DK80](#DwyerKanLocalizations) is essentially the same as the pushout quoted above from [Lurie](#Lurie).  And $\pi_0 B$ denotes taking the homwise set of connected components of a simplicially enriched category, which can be factored as first taking the enriched homotopy category (which is a category enriched over $h(sSet)$) and then its underlying ordinary category; thus the assumption that "every map of $\pi_0 B$ which is in the image of $\pi_0 V$ is invertible" is equivalent to the assumption that $f$ is a homotopy equivalence.

Finally, a "strong cofibration" is defined in [DK80](#DwyerKanLocalizations) to be a cofibration with cofibrant domain, and $\mathbf{2}_{\mathbf{S},O}$ is easily checked to indeed be cofibrant (essentially because the unit object of $sSet$ is cofibrant).


### All excellent model categories satisfy the invertibility hypothesis

[Lawson](#Lawson) now shows that:

1. Cubical sets are monoidally Quillen equivalent to simplicial sets, hence also satisfy the invertibility hypothesis.
1. Any excellent model category admits a monoidal Quillen functor from cubical sets, hence also satisfies the invertibility hypothesis.

## References

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_, Section A.3

* {#DwyerKanLocalizations} [[William Dwyer]], [[Daniel Kan]], _Simplicial localizations of categories_ , J. Pure Appl. Algebra 17 (1980), 267&#8211;284. ([pdf](http://www.nd.edu/~wgd/Dvi/SimplicialLocalizations.pdf))

* {#Lawson} [[Tyler Lawson]], _Localization of enriched categories and cubical sets_, [arXiv:1602.05313](https://arxiv.org/abs/1602.05313)

* {#MR13} [[M. Makkai]], [[J. Rosický]], _Cellular categories_, 2013, [arXiv:1304.7572](https://arxiv.org/abs/1304.7572)

* {#LumsdaineShulman} [[Peter LeFanu Lumsdaine]], [[Mike Shulman]], _Semantics of [[higher inductive types|Higher Inductive Types]], 2017, [arXiv:1705.07088](https://arxiv.org/abs/1705.07088)

[[!redirects excellent model categories]]