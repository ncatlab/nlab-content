
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the definition of [[torsors]] and [[principal bundles]] one deals with a [[group action]] $G \times P \to P$ whose [[shear map]] is an [[isomorphism]]. 

Now *if* $P$ is [[inhabited set|inhabited]], this implies a ([[fiber]]-wise) [[free action|free]] and [[transitive action|transitive]] action, which is typically what is understood to characterize [[torsors]]/[[principal bundles]].

However, the condition alone that the [[shear map]] be an isomorphism makes sense (and is then automatically satisfied) also for [[empty set|empty]] $P$, meaning for $P$ a [[strict initial object]] ([[internalization|internal]] to the ambient [[category]]). If that case is meant to be included, one speaks of a *pseudo-torsor*, for emphasis (due to [EGA IV.4 16.5.15](#EGAIV4), see also [StacksProject](#StacksProject), [Moret-Bailly 13, slide 5](#MoretBailly13)).

## Examples

* Even if a $G$-[[equivariant principal bundle]] is an actual [[torsor]] ([[internalization|in]] [[topological G-spaces]] [[slice category|sliced]] over a given base) its [[fixed loci]] will generally only be (similarly internal) pseudo-torsors.

## References

The term seems to be due to:

* {#EGAIV4} [[Alexander Grothendieck]] et al., 16.5.15 in: *[[Éléments de géométrie algébrique]]* : IV. *Étude locale des schémas et des morphismes de schémas (Quatrième partie)*, Publications mathématiques de l’I.H.É.S., tome  32 (1967), p. 5-361 ([numdam:PMIHES_1967__32__5_0](http://www.numdam.org/item/PMIHES_1967__32__5_0))

See also:

* {#StacksProject} [[The Stacks Project]], *Pseudo G-Torsor* ([Definition 03AH](https://stacks.math.columbia.edu/tag/03AH), [Definition 0498](https://stacks.math.columbia.edu/tag/0498))


* {#MoretBailly13} [[Laurent Moret-Bailly]], slide 5 of: *Principal Bundles over Valued Fields*, Oberwolfach 2013 ([[MoretBaillyPrincipalBundlesValuedFields.pdf:file]])

[[!redirects pseudo-torsors]]

[[!redirects pseudo torsor]]
[[!redirects pseudo torsors]]