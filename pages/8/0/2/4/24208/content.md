+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _wedge sum type_ is an [[axiom|axiomatization]] of the [[wedge sum]] in the context of [[homotopy type theory]].

## Definition

The wedge sum of two pointed types $(A,a)$ and $(B,b)$ can be defined as the [[higher inductive type]] with the following constructors:

* Points come from the [[sum type]] $in : A + B \to A \vee B$
* And their base point is glued $path : inl(a) = inr(b)$
Clearly this is pointed.

The wedge sum of two types $A$ and $B$, can also be defined as the [[pushout type]] of the span
$$A \leftarrow \mathbf{1} \rightarrow B$$
where the maps pick the base points of $A$ and $B$. This pushout is denoted $A \vee B$ and has basepoint $\star_{A \vee B} \equiv \mathrm{inl}(\star_A)$

## See also

* [[higher inductive type]]

* [[wedge sum]]

## References ##

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)