
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _monoidal natural transformation_ is a [[natural transformation]] between [[monoidal functors]] that respects the monoidal structure.

## Definition

Let $(\mathcal{C},\otimes_{\mathcal{C}}, 1_{\mathcal{C}})$ and $(\mathcal{D},\otimes_{\mathcal{D}}, 1_{\mathcal{D}})$ be two ([[braided monoidal category|braided monoidal categories]]). Let $(F_i, \mu_i, \epsilon_i)$ for $i \in \{1,2\}$ be two ([[braided monoidal functor|braided]]) [[lax monoidal functors]] $\mathcal{C}\longrightarrow \mathcal{D}$.

Then a [[homomorphism]] $f\;\colon\; (F_1,\mu_1, \epsilon_1) \longrightarrow (F_2,\mu_2, \epsilon_2)$ between two ([[braided monoidal functor|braided]]) [[lax monoidal functors]] is a **monoidal natural transformation**, in that it is

* a [[natural transformation]] $f(x) \;\colon\; F_1(x) \longrightarrow F_2(x)$ of the underlying functors

compatible with the product and the unit in that the following [[commuting diagram|diagrams commute]] for all objects $x,y \in \mathcal{C}$:

$$
  \array{
    F_1(x) \otimes_{\mathcal{D}} F_1(y)
      &\overset{f(x)\otimes_{\mathcal{D}} f(y)}{\longrightarrow}&
    F_2(x) \otimes_{\mathcal{D}} F_2(y)
    \\
    {}^{\mathllap{(\mu_1)_{x,y}}}\downarrow
     &&
    \downarrow^{\mathrlap{(\mu_2)_{x,y}}}
    \\
    F_1(x\otimes_{\mathcal{C}} y)
     &\underset{f(x \otimes_{\mathcal{C}} y ) }{\longrightarrow}&
    F_2(x \otimes_{\mathcal{C}} y)
  }
$$

and 

$$
  \array{
    && 1_{\mathcal{D}}
    \\
    & {}^{\mathllap{\epsilon_1}}\swarrow && \searrow^{\mathrlap{\epsilon_2}}
    \\
    F_1(1_{\mathcal{C}})
     &&\underset{f(1_{\mathcal{C}})}{\longrightarrow}&&
    F_2(1_{\mathcal{C}})
  }
  \,.
$$

## Related concepts

* [[symmetric monoidal natural transformation]]

## References


Exposition includes


* [[John Baez]], _Some definitions everyone should know_, [pdf](http://math.ucr.edu/home/baez/qg-fall2004/definitions.pdf).


[[!redirects monoidal natural transformation]]
[[!redirects monoidal natural transformations]]
[[!redirects monoidal transformation]]
[[!redirects monoidal transformations]]
