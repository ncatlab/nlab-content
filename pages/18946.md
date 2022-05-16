

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Graph theory
+-- {: .hide}
[[!include graph theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[graph theory]] a _pseudograph_ is a particular type of [[graph]]. A pseudograph is a [[set]] of [[vertices]] and for each unordered pair of vertices a set of [[edges]] between these.

A [[directed graph|directed]] pseudograph is also called a _[[quiver]]_.

The terminology is used in distinction to:

1. _[[multigraphs]]_, which are like pseudographs but not admitted to have "[[loops]]" in the sense of [[edges]] between a vertex and itself;

1. _[[simple graphs]]_, which are multigraphs with at most one edge between any unordered pair of distinct vertices.

Beware that the terminology is not completely consistent across different authors. Some authors may allows [[loops]] when they speak of multigraphs.

From yet another perspective, pseudographs are also like [[small categories|small]] [[dagger categories]] with [[identity morphisms]] and [[composition]] forgotten. Conversely, a [[small category|small]] [[dagger category]] may be regarded as a pseudograph equipped with [[extra structure]]. Formally this is witnessed by a [[forgetful functor]] 

$$U\colon DagCat \to Pseudograph$$

where Pseudograph is the category of pseudographs and [[DagCat]] is the category of ([[small category|small]] [[strict category|strict]]) dagger categories.  Moreover, this forgetful functor has a [[left adjoint]] 

$$F\colon Pseudograph \to DagCat $$

sending each pseudograph to the [[free object|free dagger category]] on that pseudograph.

## Definition

### Slick definition 

A **pseudograph** is a [[quiver]] $G$ with a contravariant quiver homomorphism $(-)^\dagger:G \to G^\op$ from $G$ to the opposite quiver $G^\op$ which 

1. is the identity on [[objects]], 

1. is an [[involution]] $\dagger \circ \dagger = \mathrm{id}_G$.

### Nuts and bolts definition 

A **pseudograph** is a [[quiver]] $(E, V, s, t)$ with a function $(-)^\dagger:E \to E$ such that for any edge $f:E$, $s(f) = t(f^\dagger)$, $t(f) = s(f^\dagger)$, and $(f^\dagger)^\dagger = f$. 

## See also

* [[dagger category]]

## References

* Wikipedia, _[Pseudograph](https://en.wikipedia.org/wiki/Pseudograph)_


[[!redirects pseudographs]]


