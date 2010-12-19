
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Two-sided fibrations

* table of contents
{:toc}

## Idea

Just as a [[Grothendieck fibration]] $E\to B$ is an alternate way to encode a [[pseudofunctor]] $B^{op}\to $ [[Cat]], a *two-sided fibration* $A \leftarrow E \to B$ is a way to encode a pseudofunctor $A\times B^{op}\to Cat$.

## Definition


+-- {: .un_defn}
###### Definition

A **two-sided discrete fibration** is a [[span]] $q \colon E \to A$, $p \colon E \to B$ of [[categories]] and [[functors]] such that 
1. each $b \to p e$ in $B$ has a unique lift in $E$ that has codomain $e$ and is in the fiber over $q e$
1. each $q e \to a$ in $A$ has a unique lift in $E$ that has domain $e$ and is in the fiber over $p e$
1. for each $f\colon e \to e'$ in $E$, the codomain of the lift of $q f$ equals the domain of the lift of $p f$ and their composite is $f$.

Write 

$$
  DFib(A,B) \subset Span(A,B)
$$ 

for the full [[subcategory]] on the category of  [[span]]s on the 2-sided discrete fibrations.

=--



+-- {: .un_defn}
###### Definition


A **two-sided fibration** is a span $q \colon E \to A$, $p \colon E \to B$ such that
1. each $b \to p e$ in $B$ has a [[cartesian morphism|cartesian]] lift in $E$ with codomain $e$ and lying in the fiber over the identity at $q e$
1. each $q e \to a$ in $A$ has an opcartesian lift in $E$ with domain $e$ and lying in the fiber over the identity at $p e$
1. for each $f \colon e \to e'$ in $E$ the canonical arrow between the codomain of any opcartesian lift of $q f$ as in (2) and the domain of the cartesian lift of $pf$ as in (1) is an [[isomorphism]].

=--

## Properties

(...)

## Related concepts

* [[Grothendieck fibration]], **two-sided fibration**,

* [[Cartesian fibration]]

## References

The notion is originally discussed in

* [[Ross Street]], Ross Street. Fibrations and Yoneda's lemma in a 2-category. In Category Seminar (Proc. Sem., Sydney, 1972/1973), pages 104  133. Lecture Notes in Math., Vol. 420. Springer, Berlin, 1974.

* [[Ross Street]], _Fibrations in bicategories_ Cahiers Topologie G&#233;om. Diff&#233;rentielle,
21(2):111{160, 1980. (Corrections in 28(1):53{56, 1987)

A useful review is in

* [[Emily Riehl]], _Two-sided discrete fibrations in 2-categories and bicategories_ 2010 ([pdf](http://math.uchicago.edu/~eriehl/fibrations.pdf))
{#Riehl}

[[!redirects two-sided fibrations]]
[[!redirects two-sided discrete fibration]]
[[!redirects two-sided discrete fibrations]]


[[!redirects 2-sided fibration]]
[[!redirects 2-sided fibrations]]
[[!redirects 2-sided discrete fibration]]
[[!redirects 2-sided discrete fibrations]]
