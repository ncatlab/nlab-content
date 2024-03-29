
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

For $F\colon C \to D$ a [[functor]] between [[categories]] that are equipped with the structure of [[monoidal categories]] $(C, \otimes)$, $(D,\otimes)$, a **lax monoidal structure map** is a [[natural transformation]]
$$
  \nabla_{x,y}\colon F(x) \otimes F(y) \to F(x \otimes y)
$$
that equips $F$ with the structure of a [[lax monoidal functor]].

Similarly, an **oplax monoidal structure map**, or **lax comonoidal structure map** is a [[natural transformation]]
$$
  \Delta_{x,y}\colon F(x \otimes y) \to F(x) \otimes F(y)
$$
that equips $F$ with the structure of an [[oplax monoidal functor]].

An (op)lax (co)monoidal structure map is sometimes called an __(op)lax (co)monoidal transformation__; however, this is *not* a laxification (a directed weakening) of any strong notion of [[monoidal natural transformation]] (which has nothing to laxify).


[[!redirects monoidal structure map]]
[[!redirects monoidal structure maps]]

[[!redirects lax monoidal structure map]]
[[!redirects lax monoidal structure maps]]
[[!redirects lax monoidal transformation]]
[[!redirects lax monoidal transformations]]

[[!redirects oplax monoidal structure map]]
[[!redirects oplax monoidal structure maps]]
[[!redirects lax comonoidal structure map]]
[[!redirects lax comonoidal structure maps]]
[[!redirects oplax monoidal transformation]]
[[!redirects oplax monoidal transformations]]
[[!redirects lax comonoidal transformation]]
[[!redirects lax comonoidal transformations]]
