
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A **finitely complete category** is a [[category]] $C$ which admits all __[[finite limit]]s__, that is all [[limit|limits]] for any [[diagrams]] $F: J \to C$ with $J$ a [[finite category]].  Finitely complete categories are also called **lex categories**.  They are also called (at least by Johnstone in the [[Elephant]]) **[[cartesian categories]]**, although this term more often means a [[cartesian monoidal category]].

Small finitely complete categories form a [[2-category]], [[Lex]].

## Variants

There are several well known reductions of this concept to classes of special limits. For example, a category is finitely complete if and only if:

* It has a [[terminal object]] and admits all binary [[product|products]] and [[equalizer|equalizers]]; or
* It has a [[terminal object]] and admits all [[pullback|binary pullbacks]].

An appropriate notion of morphism between finitely complete categories $C$, $D$ is a left [[exact functor]], or a functor that preserves finite limits (also called a _lex_ functor, a _cartesian_ functor, or a _finitely continuous_ functor). A functor preserves finite limits if and only if:

* it preserves terminal objects, binary products, and equalizers; or
* it preserves terminal objects and binary pullbacks.

Since these conditions frequently come up individually, it may be worthwhile listing them separately: 

* $F: C \to D$ **preserves terminal objects** if $F(t_C)$ is terminal in $D$ whenever $t_C$ is terminal in $C$; 

* $F: C \to D$ **preserves binary products** if the pair of maps 
$$F(c) \stackrel{F(\pi_1)}{\leftarrow} F(c \times d) \stackrel{F(\pi_2)}{\to} F(d)$$ 
exhibits $F(c \times d)$ as a product of $F(c)$ and $F(d)$, where $\pi_1: c \times d \to c$ and $\pi_2: c \times d \to d$ are the product projections in $C$; 

* $F: C \to D$ **preserves equalizers** if the map 
$$F(i): F(e) \to F(c)$$ 
is the equalizer of $F(f), F(g): F(c) \stackrel{\to}{\to} F(d)$, whenever $i: e \to c$ is the equalizer of $f, g: c \stackrel{\to}{\to} d$ in $C$. 

## Properties

In any finitely complete category, the [[kernel pair]] of the [[identity morphism]] $id$ on an object $X$ is the [[diagonal morphism]] $(id,id)$ of $X$ and has a [[coequalizer]] [[isomorphic]] to $X$ itself. 

## Related concepts

* [[locally cartesian category]]

* **cartesian category**, [[cartesian functor]], [[cartesian logic]], [[cartesian theory]]

* [[regular category]], [[regular functor]], [[regular logic]], [[regular theory]], [[regular coverage]], [[regular topos]]

* [[coherent category]], [[coherent functor]], [[coherent logic]], [[coherent theory]], [[coherent coverage]], [[coherent topos]]

* [[geometric category]], [[geometric functor]], [[geometric logic]], [[geometric theory]]



## References

Section A1.2 in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ 

[[!redirects lex category]]
[[!redirects left exact category]]
[[!redirects finitely complete categories]]
[[!redirects lex categories]]
[[!redirects left exact categories]]
[[!redirects category with finite limits]]
[[!redirects categories with finite limits]]
