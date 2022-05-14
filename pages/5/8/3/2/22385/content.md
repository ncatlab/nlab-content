+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
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

# Setoids
* table of contents
{: toc}

## Idea

A **setoid** is a collection of things (which could be a [[set]], a [[type]], or a [[preset]] depending on the chosen [[foundations]]) equipped with an [[equivalence relation]] or a [[pseudo-equivalence relation]]. Setoids are commonly used in "impoverished" foundations of mathematics that lack a primitive notion of [[quotient]]; see for instance [[Bishop set]].

## Definition 

### In graph theory

A **setoid** is a [[loop digraph object|loop]] [[digraph]] $(V, E, s:E \to V, t:E \to V)$ with functions $refl:V \to E$, $sym:E \to E$, and  
$$tr:\{(f,g) \in E \times E \vert t(f) =_V s(g)\} \to E$$ 
such that 

* for every $a \in V$, $s(refl(a)) =_E a$
* for every $a \in V$, $t(refl(a)) =_E a$
* for every $f \in E$, $s(f) =_V t(sym(f))$
* for every $f \in E$, $t(f) =_V s(sym(f))$
* for every $f \in E$, $sym(sym(f)) =_E f$
* for every $a \in V$, $sym(refl(a)) =_E refl(a)$
* for every $f \in E$, $s(tr(g,f)) =_E s(f)$ 
* for every $f \in E$, $t(tr(g,f)) =_E t(g)$
* for every $f \in E$, $tr(f, refl(s(f))) =_E f$ 
* for every $f \in E$, $tr(refl(t(f)), f) =_E f$ 
* for every $f \in E$ and $g \in E$ such that $t(f) =_V s(g)$, $sym(tr(g,f)) =_E tr(sym(f),sym(g)$. 
* for every $f \in E$, $g \in E$, and $h \in E$ such that $t(f) =_V s(g)$ and $t(g) =_V s(h)$, $tr(h,tr(g,f)) =_E tr(tr(h,g),f)$

### In category theory

A **setoid** is a [[thin category|thin]] [[dagger category]], or a dagger category [[enriched category|enriched]] in [[truth values]]. 

The [[groupoidal categorification]] of a setoid is a [[dagger category]]. 

### In type theory

A setoid is a type $T$ equipped with an [[equivalence relation]] $\equiv$. Setoids are commonly used in type theories that lack [[quotient sets]].

## See also 

* [[directed graph]]
* [[thin category]]
* [[equivalence relation]]
* [[extensional function]]
* [[univalent setoid]]
* [[stable setoid]]

[[!redirects setoids]]
