
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

In [[logic]] and [[type theory]], the **context** of a [[judgement]] (or _[[hypothetical judgement]]_, with [[dependent type|dependence]] on the context) consists of all of the assumptions that are made when that assertion is claimed to be valid; whether an assertion is in fact valid (or even meaningful) may depend on the context.  The precise definition depends on the [[theory]] (or [[doctrine]]) that one is working in.

Generally, a context is thought of as relative to some underlying logical theory.  This underlying theory will contain most of the assumptions of what constitutes validity; the context of an assertion in this theory will then include only those extra assumptions that may be used by that assertion.  On the other hand, one could also think of the entire base theory as part of the context.

## Examples

### Theory of a group

In the theory of a [[group]], it is understood that there is a group $G$, that $G$ has various elements, that two elements of $G$ may be [[equality|equal]], that any two elements of $G$ have as product an element of $G$, and that various equational laws are satisfied (which we will not list here).  That is all taken for granted when discussing a group.  However, the validity and meaningfulness of an assertion that two elements of $G$ commute will depend on (the rest of) the context.

To be more explicit, the assertion that $a$ and $b$ commute does not make sense without the additional context that $a$ and $b$ are elements of $G$.  Even in that context, this assertion, while at least meaningful, is not valid.  However, if we add to the context the assumption that $(a b)^2 = a^2 b^2$, then the assertion is valid.  Written symbolically,
$$ \vdash\; a b = b a $$
is meaningless;
$$ a\colon G,\; b\colon G \;\vdash\; a b = b a $$
is meaningful but invalid; and
\[\label{valid} a\colon G,\; b\colon G,\; (a b)^2 = a^2 b^2 \;\vdash\; a b = b a \]
is valid.

In a sufficiently rich logical language, contexts are unnecessary, which is why contexts are not usually explained in accounts of logic for ordinary reasoning (including in ordinary mathematics).  For example, the two meaningful assertions above may be rewritten thus:
$$ \vdash\; \forall (a\colon G),\; \forall (b\colon G),\; a b = b a$$
and
$$ \vdash\; \forall (a\colon G),\; \forall (b\colon G),\; (a b)^2 = a^2 b^2 \;\Rightarrow\; a b = b a$$
Here the context on the left side is the **[[empty context]]**, consisting of no assumptions whatsoever (beyond those underlying the base theory).

However, these versions involve $\forall$ and $\Rightarrow$, while the previous versions work in weaker logics.  In fact, these assertions make sense (and the valid one may be proved) in the [[internal logic]] of a [[group object]] in a [[finitely complete category]] (and somewhat more generally than that).  Accordingly, they can be interpreted as statements about any group object in any finitely complete category (and the valid one will then be interpreted as a true statement), exactly as they do for groups (which are group objects in the finitely complete category [[Set]]).

Even if one is completely uninterested in [[internalization]] or weak logics, a basic familiarity with contexts may help drive home a point that is important throughout reasoning:  **What you can state and prove depends on your assumptions.**

## Properties

### Category of contexts

The [[category of contexts]] in a [[theory]] forms its [[syntactic category]], which is a [[split model of type theory]] and is important in the [[relation between type theory and category theory]]. See _[Categorical semantics](#CategoricalSemantics)_ below.

### Categorical semantics
 {#CategoricalSemantics}

The [[categorical semantics]] of a context $\Gamma$ in [[type theory]]
is as the [[slice category]] $\mathcal{C}_{/[\Gamma]}$ over the object that interprets $\Gamma$. See at _[categorical semantics -- Definition -- Of dependent type theory -- Contexts and type judgements](http://ncatlab.org/nlab/show/categorical+semantics#ContextsAndTypeJudgements)_.

## Related concepts

* [[antecedent]]

* [[context extension]]

## References

A comprehensive definition of [[categorical semantics]] of contexts in [[homotopy type theory]] in [[type-theoretic model categories]] is in section 2 of 

* [[Mike Shulman]], _The univalence axiom for inverse diagrams_ ([arXiv:1203.3253](http://arxiv.org/abs/1203.3253))
 {#Shulman}


[[!redirects context]]
[[!redirects contexts]]

[[!redirects context enlargement]]
