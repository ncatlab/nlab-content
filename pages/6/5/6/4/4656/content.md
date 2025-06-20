
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
#### Directed homotopy type theory
+-- {: .hide}
[[!include directed homotopy type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[category theory]], a __composable pair of morphisms__ in a given [[category]] $C$ consists of [[objects]] $X,Y,Z$ of $C$ and a [[pair]] of [[morphisms]] $f\colon X \to Y$ and $g\colon Y \to Z$. The [[composite]] of this composable pair is the morphism $g \circ f\colon X \to Z$.

A composable pair in $C$ is precisely a [[2-simplex]] in the [[nerve]] of $C$.

Sometimes one defines a composable pair to be a literal [[ordered pair|pair]] $(f,g)$ such that the [[target]] of $f$ is equal to the [[source]] of $g$, but this violates the [[principle of equivalence]].

## The walking composable pair

The **[[walking]] [[composable pair]]** or **(2,1)-[[horn]] category** is the [[category]] $\Lambda_1^2$ which consists of three objects $0, 1, 2 \in \Lambda_1^2$ and two morphisms $h_{01}:\mathrm{hom}_{\Lambda_1^2}(0, 1)$ and $h_{12}:\mathrm{hom}_{\Lambda_1^2}(1, 2)$. 

The category $\Lambda_1^2$ is also called the **(2,1)-horn preorder** or the **(2,1)-horn poset** because $\Lambda_1^2$ can be shown to be a [[poset]]. 

Every composable pair in a category $C$ is represented by a [[functor]] $F:\Lambda_1^2 \to C$ from the walking composable pair to $C$. By definition of a [[category]], we have an [[equivalence of categories]] between the [[functor category]] $C^\Lambda_1^2$ of composable pairs in $C$ and the functor category $C^\Delta^2$ of [[commutative triangles]] in $C$. 

In [[dependent type theory]], given a [[directed interval]] $\mathbb{I}$, the **(2,1)-horn type** representing the walking composable pair is defined as the type of pairs of elements $i, j:\mathbb{I}$ such that $i = 1$ or $j = 0$. 

$$\Lambda_1^2 \coloneqq \sum_{i:\mathbb{I}} \sum_{j:\mathbb{I}} (i = 1) \vee (j = 0)$$

Unlike the case for the other horns representing the [[walking span]] and the [[walking cospan]], the walking composable pair is only a category if there is an axiom stating that every type is a [[Segal type]]. 

## In simplicial type theory

In [[simplicial type theory]], not every composable pair of morphisms has a [[unique composite]] forming a [[commutative triangle]], so one has to distinguish between the notions. 

Let $A$ be a type, and let $\mathbb{I}$ be the [[directed interval]] in simplicial type theory. Recall that the [[hom-type]] is defined as 

$$\mathrm{hom}_A(x, y) \coloneqq \sum_{f:\mathbb{I} \to A} (f(0) = x) \times (f(1) = y)$$

A **composable pair of morphisms** is a [[record]] consisting of 

* elements $x:A$, $y:A$, and $z:A$

* a morphism $f:\mathrm{hom}_A(x, y)$ 

* and a morphism $g:\mathrm{hom}_A(y, z)$. 

The type of composable pairs of morphisms is then the respective [[record type]].

There is another definition involving the $(2,1)$-[[horn]] type $\Lambda^2_1$, defined from the [[directed interval]] as

$$\Lambda^2_1 \coloneqq \sum_{i:\mathbb{I}} \sum_{j:\mathbb{I}} (i = 0) \vee (j = 1)$$

A **composable pair of morphisms** is simply a function $f:\Lambda^2_1 \to A$. 

The type of composable pairs of morphisms is then the [[function type]] $\Lambda^2_1 \to A$. 

## Related concepts

* [[horn]]

* [[hom set]], [[hom type]]

* [[composite]]

* [[commutative triangle]]

* [[unique composite]]

* [[span]], [[cospan]]

* [[Segal type]]

[[!include notions of walking structure]]

## References

* {#RS17} [[Emily Riehl]], [[Mike Shulman]], *A type theory for synthetic ∞-categories*, Higher Structures **1** 1 (2017) &lbrack;[arxiv:1705.07442](https://arxiv.org/abs/1705.07442), [published article](https://higher-structures.math.cas.cz/api/files/issues/Vol1Iss1/RiehlShulman)&rbrack;

* [[Emily Riehl]], *[Could $\infty$-category theory be taught to undergraduates?](https://www.ams.org/journals/notices/202305/noti2692/noti2692.html?adat=May%202023&trk=2692&galt=feature&cat=feature&pdfissue=202305&pdffile=rnoti-p727.pdf)*, Notices of the AMS (May 2023) &lbrack;[published pdf](https://www.ams.org/journals/notices/202305/rnoti-p727.pdf), [arxiv:2302.07855](https://arxiv.org/abs/2302.07855)&rbrack;

* {#CCNW} [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 1.6 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

[[!redirects composable pair]]
[[!redirects composable pairs]]

[[!redirects composable pair of morphisms]]
[[!redirects composable pairs of morphisms]]

[[!redirects pair of composable morphisms]]
[[!redirects pairs of composable morphisms]]

[[!redirects composable morphisms]]

[[!redirects composable pair of arrows]]
[[!redirects composable pairs of arrows]]

[[!redirects pair of composable arrows]]
[[!redirects pairs of composable arrows]]

[[!redirects composable arrows]]

[[!redirects walking composable pair]]
[[!redirects walking composable pairs]]

[[!redirects free-standing composable pair]]
[[!redirects free-standing composable pairs]]

[[!redirects free-living composable pair]]
[[!redirects free-living composable pairs]]

[[!redirects (2,1)-horn category]]
[[!redirects (2,1)-horn categories]]

[[!redirects (2,1)-horn preorder]]
[[!redirects (2,1)-horn preorders]]

[[!redirects (2,1)-horn proset]]
[[!redirects (2,1)-horn prosets]]

[[!redirects (2,1)-horn poset]]
[[!redirects (2,1)-horn posets]]

[[!redirects (2,1)-horn type]]
[[!redirects (2,1)-horn types]]

[[!redirects type of composable pairs]]
[[!redirects types of composable pairs]]

[[!redirects type of composable pairs of morphisms]]
[[!redirects types of composable pairs of morphisms]]

[[!redirects type of pairs of composable morphisms]]
[[!redirects types of pairs of composable morphisms]]

[[!redirects type of composable morphisms]]

[[!redirects type of composable pairs of arrows]]
[[!redirects types of composable pairs of arrows]]

[[!redirects type of pairs of composable arrows]]
[[!redirects types of pairs of composable arrows]]

[[!redirects type of composable arrows]]