[[!redirects Frobenius monoidal functors]]
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

A [[functor]] $F : C \to D$ between [[monoidal categories]] which is both a [[lax monoidal functor]] and an [[oplax monoidal functor]] is called **Frobenius** if the structure morphisms for the lax monoidal structure

$$
  \nabla_{x,y} : F(x)\otimes F(y) \to F(x \otimes y)
$$

and for the oplax monoidal structure

$$
  \Delta_{x,y} : F(x \otimes y) \to F(x) \otimes F(y)
$$

satisfy the axioms of a [[Frobenius algebra]] in that (in [[string diagram]] notation) for all objects $x,y,z$ in $C$ we have

$$
  \left(
    \array{
      F(x) &&&& F(y \otimes z)
      \\
      \downarrow &&& \swarrow & \downarrow
      \\
     F(x) && F(y)& & F(z)
     \\
     \downarrow & \swarrow &&& \downarrow
     \\
     F(x \otimes y) &&&& F(z)
    }
  \right)
  =
  \left(
  \array{
    F(x) &&&& F(y \otimes z)
    \\
    & \searrow && \swarrow
    \\
    && F(x \otimes y \otimes z)
    \\
    & \swarrow && \searrow
    \\
    F(x \otimes y) &&&& F(y)
  }
  \right)
$$

and

$$
  \left(
    \array{
      F(x \otimes y) &&&& F(z)
      \\
      \downarrow & \searrow && & \downarrow
      \\
     F(x) && F(y)  & & F(z)
     \\
     \downarrow & && \searrow & \downarrow
     \\
     F(x ) &&&& F(y \otimes z)
    }
  \right)
  =
  \left(
  \array{
    F(x \otimes y) &&&& F(z)
    \\
    & \searrow && \swarrow
    \\
    && F(x \otimes y \otimes z)
    \\
    & \swarrow && \searrow
    \\
    F(x) &&&& F(y \otimes z)
  }
  \right)
$$


## Examples

The [[Moore complex]] functor

$$
  C : sAb \to Ch_\bullet^+
$$

from abelian [[simplicial group]]s to connective [[chain complex]]es is Frobenius, as is the normalzed chains complex functor

$$
  N : sAb \to Ch_\bullet^+
  \,.
$$

For more on this see [[monoidal Dold-Kan correspondence]].

## Generalizations

Frobenius monoidal functors are a special case of Frobenius *linear* functors between [[linearly distributive categories]].


## Related concepts

* [[monoidal functor]]

* [[strong monoidal functor]]

* [[lax monoidal functor]]

* [[oplax monoidal functor]]

* [[bilax monoidal functor]]

* **Frobenius monoidal functor**

Beware of the *un*-related terminoilogy:

* [[Frobenius functor]]

## References

Equation (3.26), (3.27) in [p. 81](http://www.math.tamu.edu/~maguiar/a.pdf) of

* [[Marcelo Aguiar]], [[Swapneel Mahajan]], _[[Monoidal Functors, Species and Hopf Algebras]]_
{#AguiarMahajan}
* M. B. McCurdy, [[R. Street]], _What separable Frobenius monoidal functors preserve_, [arxiv/0904.3449](http://arxiv.org/abs/0904.3449) and Cahiers TGDC, 51 (2010)p. 29 - 50.