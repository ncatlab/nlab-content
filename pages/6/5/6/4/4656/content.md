
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[category theory]], a __composable pair of morphisms__ in a given [[category]] $C$ consists of [[objects]] $X,Y,Z$ of $C$ and a [[pair]] of [[morphisms]] $f\colon X \to Y$ and $g\colon Y \to Z$. The [[composite]] of this composable pair is the morphism $g \circ f\colon X \to Z$.

A composable pair in $C$ is precisely a [[2-simplex]] in the [[nerve]] of $C$.

Sometimes one defines a composable pair to be a literal [[ordered pair|pair]] $(f,g)$ such that the [[target]] of $f$ is equal to the [[source]] of $g$, but this violates the [[principle of equivalence]].

## The walking composable pair

The **[[walking]] [[composable pair]]** or **2-1-horn** is the [[reflexive graph]] $\Lambda_1^2$ which consists of three objects $0, 1, 2 \in \Lambda_1^2$ and two morphisms $h_{01}:\mathrm{hom}_{\Lambda_1^2}(0, 1)$ and $h_{12}:\mathrm{hom}_{\Lambda_1^2}(1, 2)$. 

> Note that this is different from the *category* $\Delta^2$ consisting of three objects $0, 1, 2 \in \Delta^2$ and two morphisms $h_{01}:\mathrm{hom}_{\Delta^2}(0, 1)$ and $h_{12}:\mathrm{hom}_{\Delta^2}(1, 2)$, which is the [[2-simplex category]] by the definition of a [[category]]. 

Every composable pair in a category $C$ is represented by a [[graph]] [[homomorphism]] $F:\Lambda_1^2 \to C$ from the walking composable pair to $C$ that preserves identity morphisms. By definition of a [[category]], we have an [[equivalence of categories]] between the [[functor category]] $C^\Lambda_1^2$ of composable pairs in $C$ and the functor category $C^\Delta^2$ of [[commutative triangles]] in $C$. 

On the other hand, the walking composable pair is typically used in the definition of a category, especially in i.e. [[synthetic (infinity,1)-category theory|synthetic $(\infty,1)$-category theory]]: 

> $C$ is a [[category]] [[if and only if]] for every composable pair of morphisms $F:\Lambda_1^2 \to C$ [[there exists a unique]] [[commutative triangle]] $G:\Delta^2 \to C$ whose composable pair is $F$ itself. 

## In simplicial type theory

In [[simplicial type theory]], not every composable pair of morphisms has a [[unique composite]] forming a [[commutative triangle]], so one has to distinguish between the notions. 

### Using morphisms

Let $A$ be a type in [[simplicial type theory]]. Recall that the [[hom-type]] is defined as 

$$\mathrm{hom}_A(x, y) \coloneqq \sum_{f:\mathbb{I} \to A} (f(0) = x) \times (f(1) = y)$$

Given $x:A$, $y:A$, and $z:A$, a **pair of composable morphisms** from $x:A$ through $y:A$ to $z:A$ is a [[record]] consisting of 

* a morphism $f:\mathrm{hom}_A(x, y)$ 

* and a morphism $g:\mathrm{hom}_A(y, z)$. 

The type of pairs of composable morphisms between $x:A$, $y:A$, and $z:A$ is then the respective [[record type]].

### Using functions from shapes

Let $A$ be a type in [[simplicial type theory]], and let $\Lambda^2_1$ denote the $(2,1)$-[[horn]] type. Given elements $x:A$, $y:A$, and $z:A$, a composite of morphisms from $x:A$ through $y:A$ to $z:A$ is a [[record]] consisting of

* a function $f:\Lambda^2_1 \to A$

* an identification $p_x:f(0, 0) = x$

* an identification $p_y:f(0, 1) = y$

* an identification $p_z:f(1, 1) = z$

The type of composites of morphisms $\mathrm{comp}_A(x, y, z)$ between $x:A$, $y:A$, and $z:A$ is then the respective [[record type]].

## Related concepts

* [[commutative triangle]]

* [[unique composite]]

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