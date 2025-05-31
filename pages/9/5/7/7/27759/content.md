
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
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

\begin{definition}
The **[[walking]] [[commutative triangle]]** or **[[triangle]] category** or **[[2-simplex]] category** is the category $\Delta^2$ which consists of three objects $0, 1, 2 \in \Delta^2$ and three morphisms $h_{01}:\mathrm{hom}_{\Delta^2}(0, 1)$, $h_{02}:\mathrm{hom}_{\Delta^2}(0, 2)$, $h_{12}:\mathrm{hom}_{\Delta^2}(1, 2)$, such that $h_{02} = h_{12} \circ h_{01}$.
\end{definition}

$\Delta^2$ is also called the **2-simplex poset** or **triangle poset** because $\Delta^2$ is a [[thin category]] and thus a [[poset]]. 

Every [[commutative triangle]] in a category $C$ is represented by a [[functor]] $F:\Delta^2 \to C$ from the walking commutative triangle to $C$. By definition of a [[category]], we have an [[equivalence of categories]] between the [[functor category]] $C^\Lambda_1^2$ of [[composable pairs]] in $C$ and the functor category $C^\Delta^2$ of commutative triangles in $C$. 

### In simplicial type theory

In [[simplicial type theory]], given a [[directed interval]] $\mathbb{I}$, the **2-simplex type** representing the walking commutative triangle is defined as the type of pairs of elements of $\mathbb{I}$ such that $i \leq j$

$$\Delta^2 \coloneqq \sum_{i:\mathbb{I}} \sum_{j:\mathbb{I}} i \leq j$$

## Properties

The walking commutative triangle is [[equivalence of categories|equivalent]] to the [[endofunctor category]] $I^I$ of the [[walking morphism]] $I$ to itself. 

## Related concepts

* [[walking structure]]

  * [[walking pair of objects]]

  * [[walking morphism]]

  * [[walking parallel pair]]

  * **walking commutative triangle**

  * [[walking isomorphism]]

  * [[walking equivalence]]

* [[triangle]], [[2-simplex]]

* [[commutative triangle]]

## References

The phrase "walking commutative triangle" appears in:

* {#CCNW} [[Denis-Charles Cisinski]], [[Bastiaan Cnossen]], [[Hoang Kim Nguyen]], [[Tashi Walde]], section 1.5.1 of: *Formalization of Higher Categories*, work in progress ([pdf](https://drive.google.com/file/d/1lKaq7watGGl3xvjqw9qHjm6SDPFJ2-0o/view))

The phrase "2-simplex" appears in 

* {#RS17} [[Emily Riehl]], [[Mike Shulman]], *A type theory for synthetic ∞-categories*, Higher Structures **1** 1 (2017) &lbrack;[arxiv:1705.07442](https://arxiv.org/abs/1705.07442), [published article](https://higher-structures.math.cas.cz/api/files/issues/Vol1Iss1/RiehlShulman)&rbrack;

* {#GWB24} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *Directed univalence in simplicial homotopy type theory* ([arXiv:2407.09146](https://arxiv.org/abs/2407.09146))

* {#GWB25} [[Daniel Gratzer]], [[Jonathan Weinberger]], [[Ulrik Buchholtz]], *The Yoneda embedding in simplicial type theory* ([arXiv:2501.13229](https://arxiv.org/abs/2501.13229))

[[!redirects walking commutative triangle]]
[[!redirects walking commutative triangles]]

[[!redirects walking commutative triangle category]]
[[!redirects walking commutative triangle categories]]

[[!redirects free-standing commutative triangle]]
[[!redirects free-standing commutative triangles]]

[[!redirects free-standing commutative triangle category]]
[[!redirects free-standing commutative triangle categories]]

[[!redirects free-living commutative triangle]]
[[!redirects free-living commutative triangles]]

[[!redirects free-living commutative triangle category]]
[[!redirects free-living commutative triangle categories]]

[[!redirects 2-simplex category]]
[[!redirects 2-simplex categories]]

[[!redirects triangle category]]
[[!redirects triangle categories]]

[[!redirects triangle preorder]]
[[!redirects triangle preorders]]

[[!redirects triangle proset]]
[[!redirects triangle prosets]]

[[!redirects triangle poset]]
[[!redirects triangle posets]]