

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

A **bilax monoidal functor** is a [[functor]] $F : C \to D$ between categories equipped with the structure of [[braided monoidal categories]] that is both a [[lax monoidal functor]] as well as an [[oplax monoidal functor]] with natural transformations

$$
  F(x) \otimes F(y) 
  \stackrel{\overset{\Delta_{x,y}}{\leftarrow}}{\underset{\nabla_{x,y}}{\to}}
  F(x \otimes y)
$$

satisfying two compatibility conditions:

* **braiding** For all $a,b,c,d \in C$ the following diagram commutes

  $$
    \array{
      && F(a \otimes b) \otimes F(c \otimes d)
      \\
      & \swarrow && \searrow
      \\
      F(a \otimes b \otimes c \otimes d)
      &&&&
      F(a) \otimes F(b) \otimes F(c) \otimes F(d)
      \\
      \downarrow &&&& \downarrow
      \\
      F(a \otimes c \otimes b \otimes d)
      &&&&
      F(a) \otimes F(c) \otimes F(b) \otimes F(d)
      \\
      & \searrow && \swarrow
      \\
      && F(a \otimes c) \otimes F(b \otimes d) 
    }
  $$

  

* **unitality** (...)

## Related concepts

* [[monoidal functor]]

* [[strong monoidal functor]]

* [[lax monoidal functor]]

* [[oplax monoidal functor]]

* **bilax monoidal functor**

* [[Frobenius monoidal functor]]


## References

Definition 3.3 in

* [[Marcelo Aguiar]], [[Swapneel Mahajan]], _[[Monoidal Functors, Species and Hopf Algebras]]_
{#AguiarMahajan}



[[!redirects bilax monoidal functors]]