+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In set theory, a [[setoid]] is usually described as a *set* with a [[pseudo-equivalence relation]]. However, in [[homotopy type theory]] or more generally in [[intensional type theory]], there are multiple different ways to define the concept of a "[[collection]] with a pseudo-equivalence relation". Presetoids arise from the most general possible notion of "[[collection]] with a pseudo-equivalence relation" in homotopy type theory , in the same way that the notion of [[precategory]] and [[pregroupoid]] arise when defining categories and groupoids. 

## Definition

A **pseudo-equivalence relation** on a type $A$ is a family of sets $Hom(a, b)$ of **morphisms** for each element $a:A$ and $b:A$, which comes with the following additional structure 

* for each element $a:A$ a family of morphisms 
$$\mathrm{id}(a):Hom(a, a)$$ 

* for each object $a:A$ and $b:A$ a family of functions
$$\mathrm{dagger}(a, b):Hom(a, b) \to Hom(b, a)$$

* for each object $a:A$, $b:A$, and $c:A$, a family of functions
$$\mathrm{comp}(a, b, c):(Hom(a, b) \times Hom(b, c)) \to Hom(a, c)$$

A **presetoid** $A$ consists of a type $Ob(A)$ of **objects** and a pseudo-equivalence relation $(\mathrm{Hom}, \mathrm{id}, \mathrm{dagger}, \mathrm{comp})$. 

## Dagger functors 

The structure-preserving maps between two presetoids are called **dagger-functors**. A dagger-functor $F:A \to B$ between two presetoids $A$ and $B$ consists of 

* a function $f_{Ob}:\mathrm{Ob}(A) \to \mathrm{Ob}(B)$ 

* a family of functions $f_{hom}(a, b):\mathrm{Hom}_A(a, b) \to \mathrm{Hom}_B(f_{Ob}(a), f_{Ob}(b))$

* and [[identifications]] indicating that the identity morphism, dagger, and the composition operation are preserved:

$$\mathrm{idpreserve}(a):f_{Hom}(a, a)(\mathrm{id}_A(a)) = \mathrm{id}_B(f_{Ob}(a))$$
$$\mathrm{daggerpreserve}(a, b, f):f_{Hom}(a, b)(\mathrm{dagger}_A(a, b)(f)) = \mathrm{dagger}_B(f_{Ob}(a), f_{Ob}(b))(f_{Hom}(a, b)(f))$$
$$\mathrm{comppreserve}(a, b, c, f, g):f_E(a, c)(\mathrm{comp}_A(f,g)) = \mathrm{comp}_B(f_{Hom}(a, b)(f), f_{Hom}(b, c)(g)$$

An dagger functor between two presetoids is **faithful** if every morphism function $f_{Hom}(a, b):\mathrm{Hom}_A(a, b) \to \mathrm{Hom}_B(f_{Ob}(a), f_{Ob}(b))$ is an [[injection]]. A dagger functor is **embedding-on-objects** if the object function $f_V:V_A \to V_B$ is an [[embedding]], and **equivalent-on-objects** if the object function is a [[equivalence in homotopy type theory|equivalence of types]]. 

## Core of a presetoid

A subpresetoid $G$ of a presetoid $A$ is a presetoid $G$ with an faithful embedding-on-objects dagger functor $f:G \to A$. A subpresetoid $G$ of $A$ is a subpregroupoid if the pseudo-equivalence relation of $G$ additionally come with: 

* for every object $a:Ob(G)$, $b:Ob(G)$, $c:Ob(G)$, and $d:Ob(G)$ and morphism $f:Hom_G(a, b)$, $g:Hom_G(b, c)$, and $h:Hom_G(c, d)$, an identification
$$\mathrm{assoc}(a, b, c, d, f 
g, h):\mathrm{comp}(a, b, d)(f, \mathrm{comp}(b, c, d)(g, h)) = \mathrm{comp}(a, c, d)(\mathrm{comp}(a, b, c)(f, g), h)$$

* for every object $a:Ob(G)$, $b:Ob(G)$ and morphism $f:Hom_G(a, b)$, an identification
$$\mathrm{runital}(a, b, f):\mathrm{comp}(a, b, b)(f, \mathrm{id}(b)) = f$$

* for every object $a:Ob(G)$, $b:Ob(G)$ and morphism $f:Hom_G(a, b)$, an identification
$$\mathrm{lunital}(a, b, f):\mathrm{comp}(a, a, b)(\mathrm{id}(a), f) = f$$

* for every object $a:Ob(G)$, $b:Ob(G)$ and morphism $f:Hom_G(a, b)$, an identification
$$\mathrm{sec}(a, b, f):\mathrm{comp}(a, b, a)(f, \mathrm{dagger}(a, b)(f)) = \mathrm{id}(a)$$

* for every object $a:Ob(G)$, $b:Ob(G)$ and morphism $f:Hom_G(a, b)$, an identification
$$\mathrm{ret}(a, b, f):\mathrm{comp}(b, a, b)(\mathrm{dagger}(a, b)(f), f) = \mathrm{id}(b)$$

A subpregroupoid $G$ of a presetoid $A$ is a maximal subpregroupoid if the dagger functor $f:G \to A$ is equivalent-on-objects, and additionally if, for every other subgroupoid $H$ of $A$ with a faithful embedding-on-objects dagger functor $g:H \to A$, the type of faithful embedding-on-objects dagger functors $h:H \to G$ with an identification $\mathrm{up}(f, g, h):h \circ f = g$ is [[contractible type|contractible]]. 

The **core [[pregroupoid]]** $Core(A)$ of a setoid $A$ is the maximal subpregroupoid of $A$. Since the core is a pregroupoid, every morphism in the core is an isomorphism, and the type of morphisms between two objects $a$ and $b$ in the core of $A$ is denoted as $a \cong_A b$. 

## Univalent setoids

There are two ways to show that two objects of a presetoid are identified with each other: by way of the [[identity type]], and by way of the type of [[isomorphisms]] in the [[core]] [[pregroupoid]] of a presetoid. Univalent setoids are precisely the presetoids which the two notions of identifying objects with each other coincide. 

For each object $a:Ob(A)$ and $b:Ob(A)$ of a presetoid $A$, there is a function 
$$\mathrm{idtoiso}(a, b):(a =_A b) \to (a \cong_A b)$$
from the [[identity type]] to the type of isomorphisms in the [[core]] [[pregroupoid]] $\mathrm{Core}(A)$ of $A$. A presetoid is a **univalent setoid** if for each object $a:Ob(A)$ and $b:Ob(A)$ the function 
$$\mathrm{idtoiso}(a, b):(a =_A b) \simeq (a \cong_A b)$$
is an equivalence of types. 

Since every type of morphisms in the core of the presetoid is a [[h-set]], this means that every univalent setoid is an [[h-groupoid]]. 

## See also

* [[setoid]]
* [[univalent setoid]]
* [[pregroupoid]]