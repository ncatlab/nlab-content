
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

$Spin(4)$ is the [[spin group]] in dimension 4, the [[double cover]] of [[SO(4)]].


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

+-- {: .num_prop #ExceptionalIsoWithSpin3TimesSpin3}
###### Proposition

The [[group homomorphism]] (eq:Spin3SquareToO4) is a [[double cover]] and hence exhibits an [[isomorphism]] between [[Spin(4)]] and the [[direct product group]] of [[Spin(3)]] with itself:

\[
  \label{Spin3TimesSpin3IsSpin4}
  \vartheta \;\colon\;
  Spin(3) \times Spin(3)
  \overset{\simeq}{\longrightarrow}
   Spin(4)
\]

Since the [[action]] of [[Spin(3)]] on the [[imaginary part|imaginary]] [[quaternions]] $\mathbb{H}_{im} \simeq_{\mathbb{R}} \mathbb{R}^3$ is the [[conjugation action]] by unit quaternions, it follows in particular, that the canonical inclusion of [[Spin(3)]] into [[Spin(4)]] is given by the [[diagonal]] morphsm with respect to the identification (eq:Spin3TimesSpin3IsSpin4):

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

(e.g. [Berger 87, Thm. 8.9.8](#Berger87), [Garrett 13](#Garrett13))

In summary:


+-- {: .num_prop }
###### Proposition

There is a [[commuting diagram]] of [[Lie groups]] of the form

$$
  \array{
    ( q_1, q_2 )
    &\mapsto&
    (x \mapsto q_1 \cdot x \cdot \overline{q}_2) 
    \\
    Sp(1) \times Sp(1) 
    &\overset{\simeq}{\longrightarrow}&
    Spin(4)
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    Sp(1)\cdot Sp(1)
    &\overset{\simeq}{\longrightarrow}&
    SO(4)
  }
$$

where

1. in the top left we have [[Sp(1)]] = [[Spin(3)]],

1. in the top right we have [[Spin(4)]],

1. in the bottom left we have [[Sp(n).Sp(1)|Sp(1).Sp(1)]]

1. in the bottom right we have [[SO(4)]]

1. the horizontal morphism assigns the [[conjugation action]] of unit [[quaternions]], as indicated,

1. the right vertical morphism is the defining [[double cover]],

1. the left vertical morphism is the defining [[quotient group]]-projection.

=--

+-- {: .num_remark #ExceptionalIsoViaDynkinDiagrams}
###### Remark
**(exceptional isomorphism via Dynkin diagrams)**

Under the [[classification of simple Lie groups]] via [[Dynkin diagrams]], 
and via the further exceptional isomorphism [[Spin(3)]] $\simeq$ [[SU(2)]], the exceptional isomorphism (eq:Spin3TimesSpin3IsSpin4) corresponds to the coincidence of the [[D3]] with the [[A3]] diagrams, both with their central node removed:



\begin{tikzpicture}

  \node at (0,1.4)  {$\mathrm{Spin}(4)$};
  \node at (3.4,1.4)  {$\mathrm{SU}(2) \times \mathrm{SU}(2)$};

  \node at (1.7,1.4) {$\simeq$};

  \node (center) at (0,0) {};
  \node (topright) at (30:1) {};
  \node (left) at (180-30:1) {};
  \node (botright) at (0,-1) {};
  %\node (D5) at (-2,0) {};
  %\node (D6) at (-3,0) {};
  
  \draw[draw=lightgray, fill=lightgray] (center) circle (.1);
  \draw[fill=black] (topright) circle (.1);
  \draw[draw=lightgray, fill=lightgray] (botright) circle (.1);
  \draw[fill=black] (left) circle (.1);

  %\draw[fill=black] (D5) circle (.1);
  %\draw[fill=black] (D6) circle (.1);

  \draw[lightgray] (center) to (topright);
  \draw[lightgray] (center) to (botright);
  \draw[lightgray] (center) to (left);
  
  %\draw (D5) to (left);
  %\draw (D6) to (D5);
  
  \begin{scope}[shift={(3.4,0)}]
  \node (center) at (0,0) {};
  \node (left) at (-1,0) {};
  \node (right) at (+1,0) {};

  \draw[draw=lightgray, fill=lightgray] (center) circle (.1);
  \draw[fill=black] (left) circle (.1);
  \draw[fill=black] (right) circle (.1);

  \draw[lightgray] (center) to (left);
  \draw[lightgray] (center) to (right);
  \end{scope}
\end{tikzpicture}

=--


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

Finally, under the [[exceptional isomorphism]] (eq:Spin3SquareToO4) $\vartheta \;\colon\; Spin(3) \times Spin(3) \overset{\simeq}{\to} Spin(4)$ these classes are related by

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

linebreak

## Related concepts

[[!include low dimensional rotation groups -- table]]

\linebreak

## References

* {#Berger87} [[Marcel Berger]], Section 8.9 of: *Geometry I*, Springer 1987 ([doi:10.1007/978-3-540-93815-6](https://doi.org/10.1007/978-3-540-93815-6))


* {#CadekVanzura98} [[Martin Čadek]], [[Jiří Vanžura]], _On 4-fields and 4-distributions in 8-dimensional vector bundles over 8-complexes_,  Colloquium Mathematicum 1998, 76 (2), pp 213-228 ([web](http://pldml.icm.edu.pl/pldml/element/bwmeta1.element.bwnjournal-article-cmv76z2p213bwm))

* {#Garrett13} [[Paul Garrett]], _Sporadic isogenies to orthogonal groups_, July 2013 ([pdf](http://www.math.umn.edu/~garrett/m/v/sporadic_isogenies.pdf))

[[!redirects Spin4]]
