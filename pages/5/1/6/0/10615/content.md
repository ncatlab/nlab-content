
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

([UFP (2013, §6.9 & §7.3) ](#UFP13))

(...)

The $(-1)$-truncation in the context is forming the [[bracket type]] [[hProp]].
$n$-truncation is given by a [[higher inductive type]].


## Related concepts

[[!include homotopy n-types - table]]


## References
 {#References}

Discussion of $n$-truncation as a [[higher inductive type]] in [[homotopy type theory]]:

Original textbook account:

* {#UFP13} [[Univalent Foundations Project]], §6.9 & §7.3 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;



Discussion of $n$-truncation as a [[modality]]:

* {#RSS20} [[Egbert Rijke]], [[Mike Shulman]], [[Bas Spitters]], Exp. 1.6 in: *Modalities in homotopy type theory*,  Logical Methods in Computer Science, **16** 1 (2020)  &lbrack;[arXiv:1706.07526](https://arxiv.org/abs/1706.07526), <a href="https://doi.org/10.23638/LMCS-16(1:2)2020">doi:10.23638/LMCS-16(1:2)2020</a>&rbrack;

and in addition via [[lifting properties]] against [[n-spheres]]:

* [[Felix Cherubini]], [[Egbert Rijke]], Thm. 3.10 in: *Modal Descent*, Mathematical Structures in Computer Science **31** 4 (2021) 363-391  &lbrack;[arXiv:2003.09713](https://arxiv.org/abs/2003.09713), [doi:10.1017/S0960129520000201](https://doi.org/10.1017/S0960129520000201)&rbrack;

Earlier discussion (and in view of [[homotopy levels]]):

* [[Nicolai Kraus]], Def. 2.3.8 in: *Truncation levels in Homotopy Type Theory*, Nottingham (2015) &lbrack;[pdf](https://eprints.nottingham.ac.uk/28986/1/thesis.pdf), [eprints:28986](https://eprints.nottingham.ac.uk/28986)&rbrack;

Precursor discussion of the material that became [UFP (2013, §7.3)](#UFP13):

* [[Peter LeFanu Lumsdaine]], *Reducing all HIT's to 1-HIT's* (May 2012) &lbrack;[blog posy](https://homotopytypetheory.org/2012/05/07/reducing-all-hits-to-1-hits/)&rbrack;

* [[Guillaume Brunerie]], *Truncations and higher inductive types* (September 2012) &lbrack;[blog post](http://homotopytypetheory.org/2012/09/16/truncations-and-truncated-higher-inductive-types/)&rbrack; 

and precursur discussion of the material that became [RSS (2020)](#RSS20):

* {#Shulman12} [[Mike Shulman]], _Higher modalities_, talk at [[UF-IAS-2012]] (October 2012)  &lbrack;[pdf](https://ncatlab.org/ufias2012/files/modalitt.pdf)&rbrack;

* [[Mike Shulman]], *All modalities are Higher Inductive Types* (November 2012) &lbrack;[blog post](http://homotopytypetheory.org/2012/11/19/all-modalities-are-hits/)&rbrack; 

Considering the combination of $n$-truncation modality and [[shape modality]]:

* [[David Jaz Myers]], Def. 3.0.1 in: *Orbifolds as microlinear types in synthetic differential cohesive homotopy type theory* ([arXiv:2205.15887](https://arxiv.org/abs/2205.15887))


[[!redirects n-truncation modality]]
[[!redirects n-truncation modalities]]

[[!redirects truncation modality]]
[[!redirects truncation modalities]]