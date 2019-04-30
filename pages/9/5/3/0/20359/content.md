

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

We discuss (Prop. \ref{CoBinarySullivanDifferentialIsWhiteheadProduct} below) how the [[rationalization]] of the [[Whitehead product]] is the co-binary part of the [[Sullivan model|Sullivan differential]] in [[rational homotopy theory]]. 

## Notation and conventions

We make explicit some notation and normalization conventions that enter the statement.

In the following, for $W$ a $\mathbb{Z}$-[[graded module]], we write

$$
  W \wedge W
  \;\coloneqq\;
  Sym^2(W)
  \;\coloneqq\;
  \big(
    W \otimes W
  \big)
  / 
  \big(
   \alpha \otimes \beta 
     \sim
   (-1)^{ n_\alpha n_\beta } 
   \beta \otimes \alpha
  \big)
  \,,
$$

where on the right $\alpha, \beta \in W$ are elements of homogeneous degree $n_\alpha, n_\beta \in \mathbb{Z}$, respectively. The point is just to highlight that "$(-)\wedge(-)$" is not to imply here a degree shift of the generators (as it typically does in the usual notation for [[Grassmann algebras]]).


Let $X$ be a [[simply connected topological space]] with [[Sullivan model]]  

\[
  \label{SullivanModelX}
  CE( \mathfrak{l} X )
  \;=\;
  \big( 
    Sym^\bullet\big(V^\ast\big), d_X 
  \big)
\]

for $V^\ast$ the [[graded vector space]] of generators, which is the $\mathbb{Q}$-linear [[dual space|dual]] [[graded vector space]] of the [[graded object|graded]] $\mathbb{Z}$-[[module]] (=[[graded abelian group]]) of [[homotopy groups]] of $X$:

$$
  V^\ast
  \;\coloneqq\;
  Hom_{Ab}\big(
    \pi_\bullet(X),
    \mathbb{Q}
  \big)
  \,.
$$

Declare the [[wedge product]] pairing to be given by

\[
  \label{WedgeProductNormalization}
  \array{
    V^\ast
    \wedge
    V^\ast
    &\overset{\Phi}{\longrightarrow}&
    Hom_{Ab}
    \big( 
      \pi_\bullet(X) \wedge \pi_\bullet(X)
      ,
      \mathbb{Q}
    \big)
    \\
    (\alpha, \beta)
    &\mapsto&
    \Big(
      v \wedge w
      \;\mapsto\;
      (-1)^{ n_\alpha \cdot n_\beta }
      \alpha(v)\cdot \beta(w)
      +
      \beta(v)\cdot \alpha(w)
    \Big)
  }
\]

where $\alpha$, $\beta$ are assumed to be of homogeneous degree $n_\alpha, n_\beta \in \mathbb{N}$, respectively.

(Notice that the usual normalization factor of $1/2$ is _not_ included on the right. This normalization follows [Andrews-Arkowitz 78, above Thm. 6.1](#AndrewsArkowitz78).)

Finally, write

\[
  \label{PojectionToBinary}
  [-]_2
  \;\colon\;
  Sym^\bullet\big(V^\ast\big)  
  \longrightarrow
  V^\ast \wedge V^\ast
\]

for the linear projection on quadratic polynomials in the graded [[symmetric algebra]].


## Statement

+-- {: .num_prop #CoBinarySullivanDifferentialIsWhiteheadProduct}
###### Proposition
**([[co-binary Sullivan differential is Whitehead product]])**

Let $X$ be a [[simply connected topological space]] of rational [[finite type]], so that it has a [[Sullivan model]] with Sullivan differential $d_X$ (eq:SullivanModelX).

Then the co-binary component (eq:PojectionToBinary) of the Sullivan differential equals the $\mathbb{Q}$-[[linear dual map]] of the [[Whitehead product]] $[-,-]_X$ on the [[homotopy groups]] of $X$:
 
$$
  [d_X \alpha]_2
  \;=\;
  [-,-]_X^\ast
  \,.
$$

More explicitly, the following [[commuting diagram|diagram commutes]]:

$$
  \array{
    V^\ast 
      &\overset{ [-]_2\circ d_X }{\longrightarrow}& 
    V^\ast \wedge V^\ast
    \\
    \big\downarrow^{ \mathrlap{=} }
    &&
    \big\downarrow^{ \mathrlap{\Phi} }
    \\
    Hom_{Ab}
    \big(
      \pi_\bullet(X),
      \mathbb{Q}
    \big)
    &
      \underset{
        Hom_{Ab}\big(
          [-,-]_X
          ,
          \;
          \mathbb{Q}
        \big)
      }{
        \longrightarrow
      }
    &
    Hom_{Ab}
    \big(
      \pi_\bullet(X)
        \wedge    
      \pi_\bullet(X),
      \;
      \mathbb{Q}
    \big)
  }
  \,,
$$

where the wedge product on the right is normalized as in (eq:WedgeProductNormalization).

=--

([Andrews-Arkowitz 78, Thm. 6.1](#AndrewsArkowitz78), following [Deligne-Griffiths-Morgan-Sullivan 75](#DeligneGriffithsMorganSullivan75))

## Examples

### Hopf fibrations
 {#HopfFibrations}

For $X = S^2$ the [[2-sphere]], consider the following two [[elements]] of its [[homotopy groups]] ([[homotopy groups of spheres|of spheres]], as it were):

1. $id_{S^2} \in \pi_2\big( S^2 \big)$ (represented by the [[identity function]] $S^2 \to S^2$)

1. $h_{\mathbb{C}} \in \pi_3\big(  S^3 \big)$ (represented by the [[complex Hopf fibration]])

Then the Whitehead product satisfies

\[
  \label{WhiteheadProductOf2Sphere}
  \big[
    id_{s^2},
    \; 
    id_{S^2}
  \big]
  \;=\;
  2 \cdot h_{\mathbb{C}}
  \,.
\]

(by [this Example](Whitehead+product#WhiteheadProductCorrespondingToComplexHopfFibration)).

Now let 

$$
  vol_{S^2},\; vol_{S^3}
  \;\in\;
  CE\big( \mathfrak{l}S^2 \big)
$$

be the two generators of the [[rational n-sphere|Sullivan model of the 2-sphere]], _normalized_ such that they correspond to the [[volume forms]] of the [[2-sphere]] and (after [[pullback of differential forms|pullback]] along the [[complex Hopf fibration]] $h_{\mathbb{C}}$) of the [[3-sphere]], respectively.

This means that the [[Sullivan model|Sullivan differential]] is

\[
  \label{GenericDifferentialForSullivanModelOf2Sphere}
  d_{S^2} vol_{S^3}
  \;=\;
  c \cdot 
  vol_{S^2} \wedge vol_{S^2}
\]

for some [[rational number]] $c \in \mathbb{Q}$.

Here on the right the [[wedge product]] is that corresponding to the ordinary wedge product of [[differential forms]].

How does this relate to the normalization of the wedge product $\Phi$ in (eq:WedgeProductNormalization)?

Notice that with the normalization in (eq:WedgeProductNormalization) we 
have

$$
  \begin{aligned}
  \Phi(vol_{S^2}, vol_{S^2})\big(  id_{S^2} \wedge id_{S^2} \big)
  & =
  (-1)^{2 \cdot 2}
  vol_{S^2}\big( id_{S^2}\big)
  \cdot
  vol_{S^2}\big( id_{S^2}\big)
  +  
  vol_{S^2}\big( id_{S^2}\big)
  \cdot
  vol_{S^2}\big( id_{S^2}\big)
  \\
  & =
  2
  \end{aligned}
$$

Therefore Prop. \ref{CoBinarySullivanDifferentialIsWhiteheadProduct} gives

$$
  \array{
    \big\{
      vol_{S^3}
    \big\}
    &\overset{[-]_2\circ d_{S^2}}{\longrightarrow}&
    c' \cdot ( vol_{S^2} \otimes vol_{S^2} )
    \\
    \big\downarrow
    &&
    \big\downarrow^{\mathrlap{\Phi}}
    \\
    \big\{
     h_{\mathbb{H}}
    \big\}
    &\overset{ [-,-]_X^\ast }{\longrightarrow}&
    \big\{
      id_{S^2} \wedge id_{S^2}
      \mapsto 
      2
    \big\}
  }
$$

where in the bottom row we used the Whitehead product (eq:WhiteheadProductOf2Sphere).

Hence $c' = 1$:

$$
  d_{S^2} vol_3 \;=\; 1 \cdot \Phi\big( vol_{S^2}, vol_{S^2} \big)
  \,.
$$

Now what is the right hand side really, in terms of the usual wedge product of differential forms?
In other words: what is $c$ in (eq:GenericDifferentialForSullivanModelOf2Sphere)?


With the usual normalization of the wedge product of differential forms, shouldn't we have

$$
  vol_{S^2} 
    \wedge 
  vol_{S^2} 
  \big( 
    id_{S^2} 
      \wedge 
    id_{S^2} 
  \big)
  \;=\;
  1
$$

?

Hence that

$$
  vol_{S^2} \wedge vol_{S^2} 
  \;=\; 
  \tfrac{1}{2} \Phi\big( vol_{S^2}, vol_{S^2} \big)
$$

?


If that is the case, it would follow that

$$
  d_{S^2} vol_{S^3}
  \;=\;
  2 \cdot vol_{S^2} \wedge vol_{S^2} 
$$

and hence that $c = 2$

?



## References

Under the general relation between the Sullivan model and the original Quillen model of [[rational homotopy theory]], the statement comes from

* {#Quillen69} [[Daniel Quillen]], section I.5 of _Rational Homotopy Theory_, Annals of Mathematics Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([jstor:1970725](https://www.jstor.org/stable/1970725))

The explicit version for Sullivan models is due to

* {#DeligneGriffithsMorganSullivan75} [[Pierre Deligne]], [[Phillip Griffiths]], [[John Morgan]], [[Dennis Sullivan]], _Real homotopy theory of Kähler manifolds_, Invent Math (1975) 29: 245 ([doi:10.1007/BF01389853](https://doi.org/10.1007/BF01389853))

and made more explicit in

* {#AndrewsArkowitz78} Peter Andrews, [[Martin Arkowitz]], Theorem 6.1 _Sullivan's Minimal Models and Higher Order Whitehead Products_, Canadian Journal of Mathematics, 30(5), 961-982, 1978 ([doi:10.4153/CJM-1978-083-6](https://doi.org/10.4153/CJM-1978-083-6))

[[!redirects the co-binary Sullivan differential is the dual Whitehead product]]
[[!redirects the co-binary Sullivan differential is the dual of the Whitehead product]]

