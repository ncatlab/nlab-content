
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

If $C$ and $D$ are monoidal categories, an **oplax monoidal functor** $F : C \to D$ is defined to be a [[lax monoidal functor]] $F: C^{op} \to D^{op}$.  So, among other things, tensor products are preserved up to morphisms of the following sort in $D$:

$$\Delta_{c,c'} : F(c \otimes c') \to F(c) \otimes F(c')$$

which must satisfy a certain [[coherence law]].

## Properties

An oplax monoidal functor sends [[comonoids]] in $C$ to comonoids in $D$, just as a lax monoidal functor sends [[monoids]] in $C$ to monoids in $D$.  For this reason an oplax monoidal functor is sometimes called a **lax comonoidal functor**.  The other obvious terms, __colax monoidal__ and __lax opmonoidal__, also exist (or at least are attested on Wikipedia).

Note that a *strong* opmonoidal functor --in which the morphisms $\phi$ are required to be [[isomorphisms]]--- is the same thing as a [[strong monoidal functor]].


+-- {: .num_prop #OplaxAdjointToLax}
###### Proposition

A functor with a [[right adjoint]] is oplax monoidal if and only if that right adjoint is a [[lax monoidal functor]].  

=--

+-- {: .proof}
###### Proof

This is a special case of the statement of [[doctrinal adjunction]] for the case of the [[2-monad]] whose algebras are monoidal categories, 

=--

Here is the explicit construction of the oplax monoidal structure from a lax monoidal structure on a right adjoint:

Let $(L \dashv R) : C \stackrel{\overset{L}{\leftarrow}}{\underset{R}{\to}} D$ be a pair of [[adjoint functor]]s and let $(C,\otimes)$ and $(D,\otimes)$ be structures of [[monoidal categories]]. 

Then if $R$ is a [[lax monoidal functor]] $L$ becomes an oplax monoidal functor with oplax unit


$$
  L(I_D) \to I_C
$$

the [[adjunct]] of the lax unit $I_D \to R(I_D)$ of $R$ and with oplax monoidal transformation 

$$
    (L (x \otimes y) \stackrel{\Delta_{x,y}}{\to} L(x) \otimes L(y)) 
$$

given by the [[adjunct]] of

$$
  x \otimes y \stackrel{\eta_x \otimes \eta_y}{\to}
  R L x \otimes R L y
  \stackrel{\nabla_{L x, L y}}{\to}
  R(L x \otimes L y)
  \,.
$$

By the formula for [[adjuncts]] in terms of the [[adjunction counit]] ([this prop.](adjunct#AdjunctionCoUnitGiveesAllAdjuncts)) this adjunct is the composite

$$
  L(x \otimes y) 
    \stackrel{L(\eta_x \otimes \eta_y)}{\longrightarrow}
  L(R L x \otimes R L y)
    \stackrel{L(\nabla_{L x, L y})}{\longrightarrow}
  L R(L x \otimes L y)
    \stackrel{\epsilon_{L x \otimes L y}}{\longrightarrow}
  L x \otimes L y
  \,.
$$

This appears for instance on [p. 17](http://arxiv.org/PS_cache/math/pdf/0209/0209342v2.pdf#page=17) of ([SchwedeShipley](#SchwedeShipley)).

## Related concepts

* [[monoidal functor]]

* [[strong monoidal functor]]

* [[lax monoidal functor]]

* **oplax monoidal functor**

* [[bilax monoidal functor]]

* [[Frobenius monoidal functor]]

## References

The construction of oplax monoidal functors from right adjoint lax monoidal functors is considered for instance around page 17 of

* [[Stefan Schwede]], [[Brooke Shipley]], _Equivalences of monoidal model categories_ , Algebr. Geom. Topol. 3 (2003), 287--334 ([arXiv](http://arxiv.org/abs/math.AT/0209342))
{#SchwedeShipley}


[[!redirects oplax monoidal functors]]

[[!redirects lax comonoidal functor]]
[[!redirects colax monoidal functor]]
[[!redirects comonoidal functor]]

[[!redirects lax comonoidal functors]]
[[!redirects colax monoidal functors]]
[[!redirects comonoidal functors]]