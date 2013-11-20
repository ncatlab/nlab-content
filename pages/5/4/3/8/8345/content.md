> (Beware there are two possible interpretations of this term. One is handled in the entry on [[profinite completion of a group]], being profinite completion of the [[homotopy type]] of a space. The entry  here treats another more purely [[topology|topological]] concept.)

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}
##Idea

The _profinite completion_ functor (on [[topological spaces]]) is the [[left adjoint]] to the inclusion of the category of  [[profinite spaces]] into that of all [[topological spaces]]. It is particularly useful when applied to [[discrete topological spaces]] (i.e. really: [[sets]]!).

## Definition:

Let $X$ be a [[topological space]].  A *profinite completion* of $X$ is a [[profinite space]], $\hat{X}$, together with a [[continuous map]], $\eta_X : X \to \hat{X}$, such that, if given any profinite space, $Y$, and a continuous map, $g : X \to Y$, there is a unique continuous map $\psi : \hat{X}\to Y$ with $\psi \eta_X = g$

## Related concepts

* [[localic reflection]]

## References

* Abolfazl Tarizadeh, _On the category of profinite spaces as a reflective subcategory_ ([arXiv:1207.5963](http://arxiv.org/abs/1207.5963))

[[!redirects profinite reflection]]
