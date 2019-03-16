
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

$Spin(4)$ is the [[spin group]] in dimension 4.

## Properties

### Exceptional isomorphisms
 {#ExceptionalIsomorphisms}

Let $\mathbb{H}$ be the [[real vector space]] underlying the [[quaternions]]. Notice that [[Spin(3)]] is the group of unit quaternions under quaternion multiplication 

$$
  Spin(3) \simeq S(\mathbb{H})
  \,.
$$

This induces a [[group homomorphism]]

\[
  \label{Spin3SquareToO4}
  \array{
    Spin(3) \times Spin(3)
    &\longrightarrow&
    O(4)
    \\
    (e_1, e_2)
    &\mapsto&
    \big(
      q 
      \mapsto
       e_1 \cdot q \cdot \overline{e_2}
    \big)
  }
\]

+-- {: .num_example}
###### Example

The [[group homomorphism]] (eq:Spin3SquareToO4) is a [[double cover]] and hence exhibits an [[isomorphism]] between [[Spin(4)]] and the [[direct product group]] of [[Spin(3)]] with itself:

\[
  \label{Spin3SquareIsSpin4}
  \vartheta \;\colon\;
  Spin(3) \times Spin(3)
  \overset{\simeq}{\longrightarrow}
   Spin(4)
\]

Since the [[action]] of [[Spin(3)]] on the [[imaginary part|imaginary]] [[quaternions]] $\mathbb{H}_{im} \simeq_{\mathbb{R}} \mathbb{R}^3$ is the [[conjugation action]] by unit quaternions, it follows in particular, that the canonical inclusion of [[Spin(3)]] into [[Spin(4)]] is given by the [[diagonal]] morphsm with respect to the identification (eq:Spin3SquareIsSpin4):

\[
  \label{Spin3Diagonally}
  \array{
    Spin(3)
    &\hookrightarrow&
    Spin(4)
    \\
    &
    {}_{\mathllap{\Delta}}\searrow
    &
    \Big\downarrow^{ \mathrlap{\simeq} }
    \\
    && Spin(3) \times Spin(3)

  }
\]

=--

(e.g. [Garrett 13](#Garrett13))

<br/>

### Euler class and Pontryagin class

+-- {: .num_prop #IntegralCohomologyOfClassifyingSpace}
###### Proposition
**([[integral cohomology]] of [[classifying space]]/[[universal characteristic classes]])**

The [[integral cohomology|integral]] [[cohomology ring]] of the [[classifying space]] of [[Spin(3)]] is [[polynomial ring|freely generated]] from $1/4$th of the [[first Pontryagin class]]:

$$
  H^\bullet
  \big(
    B Spin(3),
    \mathbb{Z}
  \big)
  \;\simeq\;
  \mathbb{Z}
  \big[
    \tfrac{1}{4}p_1
  \big]
$$


Moreover, the [[integral cohomology|integral]] [[cohomology ring]] of the [[classifying space]] of [[Spin(4)]] is [[polynomial ring|freely generated]] from the [[first fractional Pontryagin class]] $\tfrac{1}{2}p_1$ and the combination $\tfrac{1}{2}\big( \chi + \tfrac{1}{2}p_1 \big)$, where $\chi$ is the [[Euler class]]:

$$
  H^\bullet
  \big(
    B Spin(4),
    \mathbb{Z}
  \big)
  \;\simeq\;
  \mathbb{Z}
  \big[
    \tfrac{1}{2}p_1
    \,,
    \tfrac{1}{2}\big(  \chi+ \tfrac{1}{2}p_1 \big)
  \big]
$$

Finally, under the exceptional isomorphism (eq:Spin3SquareToO4) $\vartheta \;\colon\; Spin(3) \times Spin(3) \overset{\simeq}{\to} Spin(4)$ these classes are related by

$$
  \begin{aligned}
    \vartheta^\ast
    \left(
      \tfrac{1}{2}p_1
    \right)
    & 
    =
    \phantom{-}
    \tfrac{1}{4}p_1 \otimes 1
    +
    1 \otimes \tfrac{1}{4} p_1
    \\
    \vartheta^\ast
    \Big(
      \tfrac{1}{2}
      \big(
        \chi 
        + 
        \tfrac{1}{2} p_1
      \big)
    \Big)
    & 
    = 
    \phantom{-}
    \phantom{
      1 \otimes \tfrac{1}{4}p_1
      +
    }
    1 \otimes \tfrac{1}{4}p_1
    \\
    \text{hence}
    \phantom{AAAA}
    \vartheta^\ast\big( \chi \big)
    \phantom{
          + 
          \tfrac{1}{2} p_1
        \big)
      \Big)
    }
    & =
    -
    \tfrac{1}{4}p_1 \otimes 1
    +
    1 \otimes \tfrac{1}{4} p_1
    
  \end{aligned}
$$

Therefore, under the canonical [[diagonal]] inclusion $\iota \colon Spin(3) \overset{\Delta}{\hookrightarrow} Spin(3) \times Spin(3) \simeq Spin(4)$ (eq:Spin3Diagonally) we have

$$
  \begin{aligned}
    \iota^\ast
    \left(
      \tfrac{1}{2}p_1
    \right)
    & 
    =
    \tfrac{1}{2}p_1
    \\
    \iota^\ast
    \big(
      \chi
    \big)
    & 
    =
    0
  \end{aligned}
$$


=--

(e.g. [Čadek-Vanžura 98, Lemma 2.1](#CadekVanzura98))


## References


* {#CadekVanzura98} [[Martin Čadek]],  Jiří Vanžura, _On 4-fields and 4-distributions in 8-dimensional vector bundles over 8-complexes_,  Colloquium Mathematicum 1998, 76 (2), pp 213-228 ([web](http://pldml.icm.edu.pl/pldml/element/bwmeta1.element.bwnjournal-article-cmv76z2p213bwm))

* {#Garrett13} [[Paul Garrett]], _Sporadic isogenies to orthogonal groups_, July 2013 ([pdf](http://www.math.umn.edu/~garrett/m/v/sporadic_isogenies.pdf))

[[!redirects Spin4]]
