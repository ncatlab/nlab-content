
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _strict $\omega$-groupoid_ is an [[algebraic definition of higher categories|algebraic model]] for certain simple [[homotopy types]]/[[∞-groupoids]] based on [[globular sets]]. It is almost like a [[chain complex]] of [[abelian groups]] (under [[Dold-Kan correspondence]]) except that the [[fundamental group]] is allowed, more generally, to be non-abelian and to act on all the other [[homotopy groups]]. In fact, strict $\omega$-groupoids are [[equivalence of categories|equivalent]] to [[crossed complexes]].

The strict $\omega$-groupoids form an (∞,1)-category [[StrωGrpd]].

## Definition

A **strict $\omega$-groupoid** or **strict $\infty$-groupoid** is a [[strict ∞-category]] in which all [[k-morphisms]] have a strict [[inverse]] for all $k \in \mathbb{N}$

Equivalently, it is a [[globular set]] $X_\bullet$ equipped with a [[unit law|unital]] and [[associativity|associative]] [[composition]] in each degree such that for all pairs of degrees $(k_1 \lt k_2)$ it induces on the 2-graph $X_{k_2} \stackrel{\to}{\to} X_{k_1} \stackrel{\to}{\to} X_0$ the structure of a [[strict 2-groupoid]]. 

## Properties

### Relation to crossed complexes

Following work of [[J. H. C. Whitehead]], in  ([Brown-Higgins](#BrownHiggins)) it is shown that the [[1-category]] of strict $\omega$-groupoids is equivalent to that of [[crossed complexes]]. This equivalence is a generalization of the [[Dold-Kan correspondence]] to which it reduces when restricted to crossed complexes whose fundamental group is abelian and acts trivially. More details in this are at _[[Nonabelian Algebraic Topology]]_.

Strict $\infty$-groupoids form one of the vertices of the [[cosmic cube]] of [[higher category theory]].

### Model structure

There is a [[model structure on strict ∞-groupoids]]. 

This should [[presentable (∞,1)-category|present]] the full [[sub-(∞,1)-category]] of [[∞Grpd]] of strict $\infty$-groupoids.

## Related concepts

* [[weak ∞-groupoid]], [[weak ∞-category]]

* [[hypercrossed complex]]

## References

A textbook reference is

* [[Ronnie Brown]],  [[Philip Higgins]], [[Rafael Sivera]], _[[Nonabelian Algebraic Topology]]_ 
 {#BrownHigginSivera}

The equivalence of strict $\omega$-groupoids and [[crossed complex]]es is discussed in 

* [[Ronnie Brown]], [[Philip Higgins]], _The equivalence of $\infty$-groupoids and crossed complexes_ , Cah. Top. G&#233;om. Diff. 22, 371-386, 1981. ([pdf](http://www.bangor.ac.uk/~mas010/pdffiles/x-comp.pdf))
 {#BrownHiggins} 

Notice that this article says "$\infty$-groupoid" for _strict globular $\infty$-groupoid_ and "$\omega$-groupoid" for _strict cubical $\infty$-groupoid_, and also contains  definitions  of $n$-fold categories, and of what are now called  [[globular sets]].

[[!redirects strict omega-groupoids]]
[[!redirects strict ∞-groupoid]]
[[!redirects strict ∞-groupoids]]
[[!redirects strict infinity-groupoid]]
[[!redirects strict infinity-groupoids]]
