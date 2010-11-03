
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
* automatic table of contents goes here
{:toc}


## Idea

A _monoidal functor_ is a [[functor]] between [[monoidal categories]] that preserves the monoidal structure.

## Definition ##

A [[functor]] $F : C \to D$ between [[monoidal categories]] $(C,\otimes)$ and $(D,\otimes)$ is called **lax monoidal** if it is equipped with a morphism

$$
  \epsilon : I_D \stackrel{}{\to} F(I_C)  
$$

and a [[natural transformation]]

$$
  \mu_{x,y} : F(x) \otimes_D F(y) \to F(x \otimes_C y)
$$

satisfying the following conditions

* **[[associativity]]** For all $x,y,z \in C$ we have a [[commuting diagram]]

  $$
    \array{
      F(x) \otimes F(y) \otimes F(z) &\stackrel{Id \otimes \mu_{y,z}}{\to}&
      F(x) \otimes F(y \otimes z)
      \\
      {}^{\mathllap{\mu_{x,y} \otimes Id}}\downarrow
      && \downarrow^{\mathrlap{\mu_{x,y \otimes z}}}
      \\
      F(x \otimes y) \otimes F(z)
      &\stackrel{\mu_{x \otimes y, z}}{\to}&
      F(x \otimes y \otimes z)
    }
  $$

* **[[unitality]]** For all $x \in C$ we have

  $$
    \array{
      I_D  \otimes F(x) &\stackrel{l_{F(x)}}{\leftarrow}& F(x)
      \\
      {}^{\mathllap{\epsilon \otimes Id}}\downarrow && \downarrow^{\mathrlap{F(l_x)}}
      \\
      F(I_C) \otimes F(x)
      &\stackrel{\mu_{I,x}}{\to}& F(I_C \otimes x)
    }
  $$

  and

  $$
    \array{
      F(x) \otimes I_D &\stackrel{r_{F(x)}}{\leftarrow}& F(x)
      \\
      {}^{\mathllap{Id \otimes \epsilon }}\downarrow && \downarrow^{\mathrlap{F(r_x)}}
      \\
      F(x) \otimes F(I_C)
      &\stackrel{\mu_{x,I}}{\to}& F(x \otimes I_C)
    }
  $$


If $\epsilon$ and $\mu_{x,y}$ are [[isomorphism]]s then $F$ is called a **strong monoidal functor**. If they are even identities it is called a **strict monoidal functor**. 

In contrast to this, a strong monoidal functor may also be called a **weak monoidal functor**.  Sometimes the plain term "monoidal functor" is used to mean a *strong* monoidal functor, in which case the general situation is called a **lax monoidal functor**.

An __[[oplax monoidal functor]]__ (with various alternative names including **comonoidal**), is a monoidal functor from the [[opposite categories]] $C^{op}$ to $D^{op}$.

A [[homomorphism]] between monoidal functors is a [[natural transformation]] that respects the extra structure in an obvious way (...).


## Properties

Lax monoidal functors send [[monoid]]s to monoids.

Oplax monoidal functors send [[comonoids]] to comonoids. 


If we pass to the [[delooping]] [[2-category|2-categories]] $\mathbf{B}C$ and $\mathbf{B}D$ of the monoidal categories $C$ and $D$ then a lax monoidal functor corresponds to a [[lax 2-functor]] 

$$
  \mathbf{B}F : \mathbf{B}C \to \mathbf{B}D
  \,.
$$

If $F$ is strong monoidal then this is an ordinary [[2-functor]]. If it is strict monoidal, then this is a [[strict 2-functor]].

## String diagrams

Just like monoidal categories, monoidal functors have a [[string diagram]] calculus; see [these slides](http://web.science.mq.edu.au/~mmccurdy/cms2010talk.pdf) for some examples.

## Related concepts

* **monoidal functor**

* [[strong monoidal functor]]

* [[lax monoidal functor]]

* [[oplax monoidal functor]]

* [[bilax monoidal functor]]

* [[Frobenius monoidal functor]]

* [[braided monoidal functor]]

* [[symmetric monoidal functor]]

[[!redirects lax monoidal functor]]
[[!redirects strict monoidal functor]]
[[!redirects strong monoidal functor]]
[[!redirects weak monoidal functor]]
[[!redirects monoidal functors]]
[[!redirects lax monoidal functors]]
[[!redirects strict monoidal functors]]
[[!redirects strong monoidal functors]]
[[!redirects weak monoidal functors]]