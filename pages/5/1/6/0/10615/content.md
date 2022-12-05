
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For all $n \in \{-2, -1, 0,1,2,3, \cdots\}$, [[truncated object in an (infinity,1)-category|n-truncation]] is a [[modality]] (in [[homotopy type theory]]).

## Defintion

Let us work in a [[dependent type theory]] with [[suspension types]] and [[localizations]]. Starting with the $(-1)$-dimensional [[sphere type]], which is the [[empty type]] $S^{-1} \coloneqq \mathbb{0}$, the $(n + 1)$-dimensional sphere type $S^{n + 1}$ is the suspension of the $n$-dimensional sphere type $S^{n + 1} \coloneqq \Sigma S^n$. 

The $n$-truncation modality is the [[localization of a type at a family of functions|localization at the unique function]] from the $(n + 1)$-dimensional sphere type to the [[unit type]] $S^{n + 1} \to \mathbb{1}$

$$\left[A\right]_n \coloneqq L_{S^{n + 1}}(A)$$

By definition, the type of functions $(\mathbb{1} \to \left[A\right]_n) \to (S^{n + 1} \to \left[A\right]_n)$ is an [[equivalence of types]]. 

## Properties

### In low degree

$(-2)$-truncation is the [[unit type]] modality ([[constant map|constant]] on the unit type).

$(-1)$-truncation is given by forming _[[bracket types]]_, turning types into genuine [[propositions]]. 

[[classical logic|Classically]], this is the same as the [[double negation modality]]; in general, the bracket type ${\|A\|_{-1}}$ only entails the double negation $\neg(\neg{A})$:
there is a canonical [[function]]

$$
  {\|A\|_{-1}} \longrightarrow \neg(\neg{A})
$$

and this is a [[1-epimorphism]] precisely if the [[law of excluded middle]] holds.

### In homotopy type theory
 {#InHomotopyTypeTheory}

([HoTT Book, section 6.9](#HoTTBook))

(...)

The $(-1)$-truncation in the context is forming the [[bracket type]] [[hProp]].
$n$-truncation is given by a [[higher inductive type]].


## Related concepts

[[!include homotopy n-types - table]]


## References

* [[Mike Shulman]], _Higher modalities_, talk at [[UF-IAS-2012]], October 2012  ([pdf](http://uf-ias-2012.wikispaces.com/file/view/modalitt.pdf))
 {#Shulman}

* [[Mike Shulman]], _[All modalities are Higher Inductive Types](http://homotopytypetheory.org/2012/11/19/all-modalities-are-hits/)_

* [[Guillaume Brunerie]], _[Truncations and higher inductive types](http://homotopytypetheory.org/2012/09/16/truncations-and-truncated-higher-inductive-types/)_.

* {#HoTTBook} [[Univalent Foundations Project]], section 6.9 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

For [[n-truncations]] as [[localizations]] at [[sphere types]], see:

* [[David Jaz Myers]], Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory ([arXiv:2205.15887](https://arxiv.org/abs/2205.15887))

[[!redirects n-truncation modality]]
[[!redirects n-truncation modalities]]

[[!redirects truncation modality]]
[[!redirects truncation modalities]]