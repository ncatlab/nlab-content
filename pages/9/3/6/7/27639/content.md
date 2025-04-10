
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

## Idea

The concept of a [[span]] in [[simplicial type theory]]. Note that in the context of simplicial type theory, spans make sense for any type, not just the [[Segal types]]. 

## Definition

### Using morphisms

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. A **span** of $x:A$ and $y:A$ is a [[record]] consisting of 

* an element $z:A$, 

* a morphism $p_x:\mathrm{hom}_A(z, x)$, 

* and a morphism $p_y:\mathrm{hom}_A(z, y)$, 

The type of spans $\mathrm{span}_A(x, y)$ between $x:A$ and $y:A$ is then the respective [[record type]].

### Using functions from shapes

Let $\Lambda^2_2$ denote the $(2,2)$-[[horn]] type. 

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. A **span** of $x:A$ and $y:A$ is a [[record]] consisting of 

* a function $f:\Lambda^2_2 \to A$, 

* an identification $p_x:f(0, 1) = x$, 

* and an identification $p_y:f(1, 1) = y$, 

The type of spans $\mathrm{span}_A(x, y)$ between $x:A$ and $y:A$ is then the respective [[record type]].

## Morphisms of spans

### Using morphisms

Given elements $x:A$ and $y:A$ and spans $f:\mathrm{span}_A(x, y)$ and $g:\mathrm{span}_A(x, y)$, a morphism of spans between $f$ and $g$ is a [[record]] consisting of 

* a morphism $h:\mathrm{hom}_A(\mathrm{pr}_1(f), \mathrm{pr}_1(y))$ 

* a witness that $\mathrm{pr}_2(g)$ is the [[unique composite]] of $\mathrm{pr}_2(f)$ and $h$ 

* a witness that $\mathrm{pr}_3(g)$ is the [[unique composite]] of $\mathrm{pr}_3(f)$ and $h$. 

The type of morphisms of spans $\mathrm{homspan}_A(x, y, f, g)$ is then the respective [[record type]].

If $A$ is a [[Segal type]], then the record consists of fields

* a morphism $h:\mathrm{hom}_A(\mathrm{pr}_1(f), \mathrm{pr}_1(y))$ 

* an identification $\mathrm{pr}_2(g) = \mathrm{pr}_2(f) \circ h$ 

* an identification $\mathrm{pr}_3(g) = \mathrm{pr}_3(f) \circ h$. 

### Using functions from shapes

Given elements $x:A$ and $y:A$ and spans $f:\mathrm{span}_A(x, y)$ and $g:\mathrm{span}_A(x, y)$, a morphism of spans between $f$ and $g$ is a [[record]] consisting of 

* a function $h:\mathbb{I} \to A$

* an identification $p_x:h(0) = \mathrm{pr}_1(f)$, 

* an identification $p_y:h(1) = \mathrm{pr}_1(g)$, 

* a function $j:\Delta^2 \to A$, 

* a witness that $j$ is the unique element of the fiber of the canonical function $(\Delta^2 \to A) \to (\Lambda^2_2 \to A)$ at $f$

* a witness that $j$ is the unique element of the fiber of the canonical function $(\Delta^2 \to A) \to (\Lambda^2_2 \to A)$ at $g$

The type of morphisms of spans $\mathrm{homspan}_A(x, y, f, g)$ is then the respective [[record type]].

## Left quotients

Given a span $x:A$, $y:A$, $z:A$, $f:\mathrm{hom}_A(z, x)$ and $g:\mathrm{hom}_A(z, y)$, a **left quotient** is a unique morphism $g / f:\mathrm{hom}_A(x, y)$ such that $g$ is the [[unique composite]] of $f$ and $g / f$. A span is said to be **left divisible** if there exists a unique morphism $g / f:\mathrm{hom}_A(x, y)$ such that $g$ is the [[unique composite]] of $f$ and $g / f$. 

## Related concepts

* [[simplicial type theory]]

* [[span]]

* [[span in an (infinity,1)-category]]

* [[cospan in simplicial type theory]]

* [[pair of composable morphisms]]

* [[composite of morphisms]]

* [[product in simplicial type theory]]

[[!redirects span in simplicial type theory]]
[[!redirects spans in simplicial type theory]]

[[!redirects span in a Segal type]]
[[!redirects spans in a Segal type]]

[[!redirects span in a complete Segal type]]
[[!redirects spans in a complete Segal type]]

[[!redirects span in a Rezk type]]
[[!redirects spans in a Rezk type]]

[[!redirects type of spans in simplicial type theory]]
[[!redirects types of spans in simplicial type theory]]

[[!redirects type of spans in a Segal type]]
[[!redirects types of spans in a Segal type]]

[[!redirects type of spans in a complete Segal type]]
[[!redirects types of spans in a complete Segal type]]

[[!redirects type of spans in a Rezk type]]
[[!redirects types of spans in a Rezk type]]

[[!redirects morphism of spans in simplicial type theory]]
[[!redirects morphisms of spans in simplicial type theory]]

[[!redirects morphism of spans in a Segal type]]
[[!redirects morphisms of spans in a Segal type]]

[[!redirects morphism of spans in a complete Segal type]]
[[!redirects morphisms of spans in a complete Segal type]]

[[!redirects morphism of spans in a Rezk type]]
[[!redirects morphisms of spans in a Rezk type]]

[[!redirects type of morphisms of spans in simplicial type theory]]
[[!redirects types of morphisms of spans in simplicial type theory]]

[[!redirects type of morphisms of spans in a Segal type]]
[[!redirects types of morphisms of spans in a Segal type]]

[[!redirects type of morphisms of spans in a complete Segal type]]
[[!redirects types of morphisms of spans in a complete Segal type]]

[[!redirects type of morphisms of spans in a Rezk type]]
[[!redirects types of morphisms of spans in a Rezk type]]

[[!redirects left quotient in simplicial type theory]]
[[!redirects left quotients in simplicial type theory]]

[[!redirects left quotient in a Segal type]]
[[!redirects left quotients in a Segal type]]

[[!redirects left quotient in a complete Segal type]]
[[!redirects left quotients in a complete Segal type]]

[[!redirects left quotient in a Rezk type]]
[[!redirects left quotients in a Rezk type]]

[[!redirects left divisible span in simplicial type theory]]
[[!redirects left divisible spans in simplicial type theory]]

[[!redirects left divisible span in a Segal type]]
[[!redirects left divisible spans in a Segal type]]

[[!redirects left divisible span in a complete Segal type]]
[[!redirects left divisible spans in a complete Segal type]]

[[!redirects left divisible span in a Rezk type]]
[[!redirects left divisible spans in a Rezk type]]

[[!redirects left divisibility in simplicial type theory]]
[[!redirects left divisible in simplicial type theory]]

[[!redirects left divisibility in a Segal type]]
[[!redirects left divisible in a Segal type]]

[[!redirects left divisibility in a complete Segal type]]
[[!redirects left divisible in a complete Segal type]]

[[!redirects left divisibility in a Rezk type]]
[[!redirects left divisible in a Rezk type]]