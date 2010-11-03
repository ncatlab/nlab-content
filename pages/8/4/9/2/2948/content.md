
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

If $C$ and $D$ are monoidal categories, an **oplax monoidal functor** $F : C \to D$ is defined to be a [[lax monoidal functor]] $F: C^{op} \to D^{op}$.  So, among other things, tensor products are preseved up to morphisms of the following sort in $D$:

$$\phi_{c,c'} : F(c \otimes c') \to F(c) \otimes F(c')$$

which must satisfy a certain [[coherence law]].

## Properties

An oplax monoidal functor sends [[comonoids]] in $C$ to comonoids in $D$, just as a lax monoidal functor sends [[monoids]] in $C$ to monoids in $D$.  For this reason an oplax monoidal functor is sometimes called a **lax comonoidal functor**.  The other obvious terms, __colax monoidal__ and __lax opmonoidal__, also exist (or at least are attested on Wikipedia).

Note that a *strong* opmonoidal functor --in which the morphisms $\phi$ are required to be [[isomorphisms]]--- is the same thing as a [[strong monoidal functor]].

## Related concepts

* [[monoidal functor]]

* [[strong monoidal functor]]

* [[lax monoidal functor]]

* **oplax monoidal functor**

* [[Frobenius monoidal functor]]


[[!redirects oplax monoidal functors]]

[[!redirects lax comonoidal functor]]
[[!redirects colax monoidal functor]]
[[!redirects comonoidal functor]]

[[!redirects lax comonoidal functors]]
[[!redirects colax monoidal functors]]
[[!redirects comonoidal functors]]