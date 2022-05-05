
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

## Definition

By comparing the notions of [[regular epimorphism]] and [[effective epimorphism]] with that of [[effective epimorphism in an (∞,1)-category]], we propose to call a morphism $f : c \to d$ in an [[(∞,1)-category]] a **regular epimorphism** if it is the [[colimit]] of some simplicial diagram, i.e. if there exists a functor $c : \Delta^{op} \to C$, such that $f$  is the [[colimit in a quasi-category|colimiting cocone]]

$$
  \cdots c_2 \stackrel{\to}{\stackrel{\to}{\to}} c_1 \stackrel{\to}{\to} c \stackrel{f}{\to} d
$$

over this diagram.

Equivalently, this is a morphism such that for all objects $e \in C$ the induced morphism $f^* : C(d,e) \to C(c,e)$ is a [[regular monomorphism in an (∞,1)-category]] in the [[(∞,1)-category]] [[∞Grpd]].

**Warning**. Such a morphism may not be an [[epimorphism in an (∞,1)-category]] (i.e. a [[monomorphism in an (∞,1)-category|monomorphism]] in the opposite category).

## Questions

* If $f$ has a [[Cech nerve]] and is a regular epimorphism above, does it follow that it is the colimit of its Cech nerve (that is, that it is an [[effective epimorphism in an (∞,1)-category]])?

* Is there a notion of a [[strict epimorphism]] in an [[(∞,1)-category]]?

[[!redirects regular epimorphism in an (∞,1)-category]]
[[!redirects regular epimorphisms in an (infinity,1)-category]]
[[!redirects regular epimorphisms in an (∞,1)-category]]
