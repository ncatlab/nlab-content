


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


## Definition

A __weak model category__ is a [[premodel category]] that satisfies the following two [[axioms]]:

1. __Cylinder axiom__: Every [[cofibration]] $A\to X$ from a [[cofibrant object]]
to a [[fibrant object]] admits a __relative strong cylinder object__ 
$$X\sqcup_A X\to I_A X\to X,$$ 
where the left map is a [[cofibration]] and its first component $X\to I_A X$
is an [[acyclic cofibration]].

1. __Path object axiom__: Every [[fibration]] $A\to X$ from a [[cofibrant object]] to a [[fibrant object]] admits a __relative strong path object__
$$A\to P_X A\to A\times_X A,$$
where the right map is a [[fibration]] and its first component $P_X A\to A$ is an [[acyclic fibration]].

## Relation to model categories

[[model category|Model categories]] can be singled out from weak model categories
by adding the following properties:

1.  Every [[fibrant object]] 
admits a strong path object and every [[cofibrant object]] admits a strong [[cylinder object]].

1.  All [[acyclic cofibrations]] are [[trivial cofibrations]]
and all [[acyclic fibrations]] are [[trivial fibrations]].
(Trivial maps are given as data for a [[premodel category]],
whereas acyclic (co)fibrations are defined as (co)fibrations
that satisfy a right (left) lifting property with respect to the class of cofibrations with cofibrant source (respectively fibrations with fibrant target.)

1.  The two classes of [[weak equivalence]] corresponding
to the left and right induced [[semimodel structures]] coincide.


## References

* [[Simon Henry]], _Weak model categories in classical and constructive mathematics_ ([arXiv:1807.02650](https://arxiv.org/abs/1807.02650))

* [[Simon Henry]], _Combinatorial and accessible weak model categories_ ([arXiv:2005.02360](https://arxiv.org/abs/2005.02360))

[[!redirects weak model categories]]
