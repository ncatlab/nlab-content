
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


# Zigzags
* table of contents
{: toc}

## Zigzags of morphisms

In a [[category]] $C$ a **zigzag of morphisms** is a finite collection of [[morphism]]s $(f_i)$ in $C$ of the form

$$
  \array{
    && x_1 &&&& x_3 & \cdots
    \\
    & {}^{\mathllap{f_1}}\swarrow && \searrow^{\mathrlap{f_2}}
    && {}^{\mathllap{f_3}}\swarrow
    && \searrow^{\mathrlap{f_4}} & \cdots 
    \\
    x_0 &&&& x_2 &&&& x_4 & \cdots 
  }
  \,.
$$

A zigzag consisting just out of two morphisms is a _roof_ or [[span]].

General such zig-zags of morphisms represent ordinary morphisms in the _groupoidification_ of $C$ -- the [[Kan fibrant replacement]] of its [[nerve]], its [[simplicial localization]] or its 1-categorical [[localization]] at all its morphisms. 

More generally, if in these zig-zags the left-pointing morphisms are restricted to be in a class $S \subset Mor(C)$, then these zig-zags represent morphisms in the simplicial localizaton or localization of $C$ at $S$.

## Related concepts

* [[resolution]], [[derived functor]]

* [[span]], [[correspondence]]

* [[Burnside category]]

* [[zigzag persistence module]]

[[!redirects zigzag]]
[[!redirects zigzags]]
[[!redirects zig-zag]]
[[!redirects zig-zags]]
[[!redirects zig zag]]
[[!redirects zig zags]]
