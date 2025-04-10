
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

The concept of a [[cospan]] in [[simplicial type theory]]. Note that in the context of simplicial type theory, cospans make sense for any type, not just the [[Segal types]]. 

## Definition

### Using morphisms

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. A **cospan** of $x:A$ and $y:A$ is a [[record]] consisting of 

* an element $z:A$, 

* a morphism $p_x:\mathrm{hom}_A(y, z)$, 

* and a morphism $p_y:\mathrm{hom}_A(x, z)$, 

The type of cospans $\mathrm{cospan}_A(x, y)$ between $x:A$ and $y:A$ is then the respective [[record type]].

### Using functions from shapes

Let $\Lambda^2_0$ denote the $(2,0)$-[[horn]] type. 

Let $A$ be a type in [[simplicial type theory]], and let $x:A$ and $y:A$ be two elements in $A$. A **cospan** of $x:A$ and $y:A$ is a [[record]] consisting of 

* a function $f:\Lambda^2_0 \to A$, 

* an identification $p_x:f(0) = x$, 

* and an identification $p_y:f(1) = y$, 

The type of cospans $\mathrm{cospan}_A(x, y)$ between $x:A$ and $y:A$ is then the respective [[record type]].

## Morphisms of cospans

### Using morphisms

Given elements $x:A$ and $y:A$ and cospans $f:\mathrm{cospan}_A(x, y)$ and $g:\mathrm{cospan}_A(x, y)$, a morphism of cospans between $f$ and $g$ is a [[record]] consisting of 

* a morphism $h:\mathrm{hom}_A(\mathrm{pr}_1(f), \mathrm{pr}_1(y))$ 

* a witness that $\mathrm{pr}_2(g)$ is the [[unique composite]] of $h$ and $\mathrm{pr}_2(f)$ and $h$ 

* a witness that $\mathrm{pr}_3(g)$ is the [[unique composite]] of $h$ and $\mathrm{pr}_3(f)$. 

The type of morphisms of spans $\mathrm{homcospan}_A(x, y, f, g)$ is then the respective [[record type]].

If $A$ is a [[Segal type]], then the record consists of fields

* a morphism $h:\mathrm{hom}_A(\mathrm{pr}_1(f), \mathrm{pr}_1(y))$ 

* an identification $\mathrm{pr}_2(g) = h \circ \mathrm{pr}_2(f) \circ h$ 

* an identification $\mathrm{pr}_3(g) = h \circ \mathrm{pr}_3(f)$. 

### Using functions from shapes

Given elements $x:A$ and $y:A$ and cospans $f:\mathrm{cospan}_A(x, y)$ and $g:\mathrm{cospan}_A(x, y)$, a morphism of cospans between $f$ and $g$ is a [[record]] consisting of 

* a function $h:\mathbb{I} \to A$

* an identification $p_x:h(0) = \mathrm{pr}_1(f)$, 

* an identification $p_y:h(1) = \mathrm{pr}_1(g)$, 

* a function $j:\Delta^2 \to A$, 

* a witness that $j$ is the unique element of the fiber of the canonical function $(\Delta^2 \to A) \to (\Lambda^2_0 \to A)$ at $f$

* a witness that $j$ is the unique element of the fiber of the canonical function $(\Delta^2 \to A) \to (\Lambda^2_0 \to A)$ at $g$

The type of morphisms of cospans $\mathrm{homcospan}_A(x, y, f, g)$ is then the respective [[record type]].

## Related concepts

* [[simplicial type theory]]

* [[cospan]]

* [[cospan in an (infinity,1)-category]]

* [[span in simplicial type theory]]

* [[coproduct in simplicial type theory]]

* [[quasigroupoid type]]

[[!redirects cospan in simplicial type theory]]
[[!redirects cospans in simplicial type theory]]

[[!redirects cospan in a Segal type]]
[[!redirects cospans in a Segal type]]

[[!redirects cospan in a complete Segal type]]
[[!redirects cospans in a complete Segal type]]

[[!redirects cospan in a Rezk type]]
[[!redirects cospans in a Rezk type]]

[[!redirects type of cospans in simplicial type theory]]
[[!redirects types of cospans in simplicial type theory]]

[[!redirects type of cospans in a Segal type]]
[[!redirects types of cospans in a Segal type]]

[[!redirects type of cospans in a complete Segal type]]
[[!redirects types of cospans in a complete Segal type]]

[[!redirects type of cospans in a Rezk type]]
[[!redirects types of cospans in a Rezk type]]

[[!redirects morphism of cospans in simplicial type theory]]
[[!redirects morphisms of cospans in simplicial type theory]]

[[!redirects morphism of cospans in a Segal type]]
[[!redirects morphisms of cospans in a Segal type]]

[[!redirects morphism of cospans in a complete Segal type]]
[[!redirects morphisms of cospans in a complete Segal type]]

[[!redirects morphism of cospans in a Rezk type]]
[[!redirects morphisms of cospans in a Rezk type]]

[[!redirects type of morphisms of cospans in simplicial type theory]]
[[!redirects types of morphisms of cospans in simplicial type theory]]

[[!redirects type of morphisms of cospans in a Segal type]]
[[!redirects types of morphisms of cospans in a Segal type]]

[[!redirects type of morphisms of cospans in a complete Segal type]]
[[!redirects types of morphisms of cospans in a complete Segal type]]

[[!redirects type of morphisms of cospans in a Rezk type]]
[[!redirects types of morphisms of cospans in a Rezk type]]
