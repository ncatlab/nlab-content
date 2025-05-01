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

The concept of Frobenius monoidal functors is related to that of

* [[Frobenius functors]],

albeit in a nontrivial way. See Theorem 3.18 of ([Flake et al 2024](#FLP24)) for more on this.

## References

* {#AguiarMahajan} [[Marcelo Aguiar]], [[Swapneel Mahajan]], (3.26), (3.27) on [p. 81](http://www.math.tamu.edu/~maguiar/a.pdf) of: _[[Monoidal Functors, Species and Hopf Algebras]]_, CRM Monograph Series __29__, Amer. Math. Soc. (2010) &lbrack;[ISBN:978-0-8218-4776-3](https://bookstore.ams.org/crmm-29/), [pdf](http://www.math.cornell.edu/~maguiar/a.pdf)&rbrack;

* M. B. McCurdy, [[R. Street]], *What separable Frobenius monoidal functors preserve*, [[Cahiers]] TGDC **51** (2010) 29-50 &lbrack;[arxiv/0904.3449](http://arxiv.org/abs/0904.3449)&rbrack; .


Relation to [[Drinfeld centers]]:

* {#FLP24} Johannes Flake, Robert Laugwitz, Sebastian Posur: *Frobenius monoidal functors from ambiadjunctions and their lifts to Drinfeld centers* &lbrack;[arXiv:2410.08702](https://arxiv.org/abs/2410.08702)&rbrack;


[[!redirects Frobenius monoidal functors]]

