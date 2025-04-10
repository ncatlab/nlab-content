
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

## Idea

The notion of [[composition]] of [[morphisms]] in [[simplicial type theory]].

## Definition

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

## Unique composites

\begin{definition}
A pair of composable morphisms $(f, g)$ is **uniquely composable** if there exists a unique morphism $h:\mathrm{hom}_A(x, z)$ and function $k:\Delta^2 \to A$ such that $k(0, 0) = x$, $k(0, 1) = y$, $k(1, 1) = z$, $k_{(0, 0), (0, 1)} = f$, $k_{(0, 1), (1, 1)} = g$, $k_{(0, 0), (1, 1)} = h$:

$$\mathrm{isUniquelyComposable}(f, g) \coloneqq \mathrm{isContr}\left(\sum_{h:\mathrm{hom}_A(x, z)}\sum_{k:\Delta^2 \to A} \left(
\begin{array}{c}
    (k(0, 0) = x) \times (k(0, 1) = y) \times (k(1, 1) = z) \times \\
    (k_{(0, 0), (0, 1)} = f) \times (k_{(0, 1), (1, 1)} = g) \times (k_{(0, 0), (1, 1)} = h)
\end{array}
\right)\right)$$
\end{definition}

\begin{definition}
A morphism $h:\mathrm{hom}_A(x, z)$ is said to be the **unique composite** of $(f, g)$ if there exists a unique function $k:\Delta^2 \to A$ such that $k(0, 0) = x$, $k(0, 1) = y$, $k(1, 1) = z$, $k_{(0, 0), (0, 1)} = f$, $k_{(0, 1), (1, 1)} = g$, $k_{(0, 0), (1, 1)} = h$ and $(h, k)$ is the [[center of contraction]] of the dependent sum type:

$$\sum_{h:\mathrm{hom}_A(x, z)}\sum_{k:\Delta^2 \to A} \left(
\begin{array}{c}
    (k(0, 0) = x) \times (k(0, 1) = y) \times (k(1, 1) = z) \times \\
    (k_{(0, 0), (0, 1)} = f) \times (k_{(0, 1), (1, 1)} = g) \times (k_{(0, 0), (1, 1)} = h)
\end{array}
\right)$$
\end{definition}

Identity morphisms are always uniquely composable:

* Every morphism $f:\mathrm{hom}_A(x, y)$ is uniquely composable with the [[identity morphism]] $\mathrm{id}_A(x):\mathrm{hom}_A(x, x)$, whose unique composite is the original morphism $f$ itself. 

* The [[identity morphism]] $\mathrm{id}_A(y):\mathrm{hom}_A(y, y)$ is uniquely composable with every morphism $f:\mathrm{hom}_A(x, y)$, whose unique composite is the original morphism $f$ itself. 

## Related concepts

* [[hom-type]]

* [[Segal type]]

* [[composite of morphisms]]

* [[span in simplicial type theory]]

* [[cospan in simplicial type theory]]

[[!redirects pair of composable morphisms]]
[[!redirects pairs of composable morphisms]]

[[!redirects type of pairs of composable morphisms]]
[[!redirects types of pairs of composable morphisms]]

[[!redirects uniquely composable]]

[[!redirects unique composite]]
[[!redirects unique composites]]

[[!redirects unique composition]]

[[!redirects unique composite of morphisms]]
[[!redirects unique composites of morphisms]]

[[!redirects unique composition of morphisms]]

[[!redirects composable morphisms]]