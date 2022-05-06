
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

The **Whitehead product** is a bilinear operation on the elements of the [[homotopy groups]] of a [[pointed space|pointed]] [[CW-complex]] $X$, which makes them a [[super Lie algebra]] over the [[ring]] of [[integers]] (often called a _graded quasi-Lie algebra_).

More specifically, it takes as input $\alpha\in\pi_r(X)$ and $\beta\in\pi_s(X)$ and produces $[\alpha,\beta]_{Wh}\in\pi_{r+s-1}(X)$.  The operation satisfies a graded [[Jacobi identity]] ([Hilton 55, Theorem B](#Hilton55)).

There is also a **generalized Whitehead product** where we can take more general homotopy classes ([[continuous maps]] up to [[homotopy]]) $\alpha\in [S^\cdot Y,X]$ and $\beta\in [S^\cdot Z,X]$ to produce a class $[\alpha,\beta]_{Wh}\in[Y\star Z,X]$. Here $S^\cdot$ denotes the [[reduced suspension]] operation on pointed spaces and $\star$ denotes the [[join of spaces|join]] of CW-complexes. Notice that $pt\star Z = C^\cdot(Z)$ and the reduced [[cone]] of a point is $C^\cdot(pt)=S^1$. Thus for $Y=Z=pt$ the generalized Whitehead product reduced to the usual Whitehead product.

The Whitehead products form one of the [[primary homotopy operation]]s and in fact with [[composition operation]]s and $\pi_1$-actions generate all such operations. This is related to the definition of [[Pi-algebra]].

In the context of [[simplicial group]]s, representing [[connected]] [[homotopy type]]s, there is a formula for the Whitehead product in terms of a [[Samelson product]], which in turn is derived from a [[shuffle]] product which is a sort of non-commutative version of the [[Eilenberg-Zilber map]].  These simplicial formulae come from an analysis of the structure of the [[product of simplices]]. (The formula for the Whitehead product is due to [[Dan Kan]] and can be found in the old survey article of [[Ed Curtis]].  The proof that it works was never published.)

## Properties

### Relation to the Sullivan models
 {#RelationToSullivanModels}

We discuss (Prop. \ref{CoBinarySullivanDifferentialIsWhiteheadProduct} below) how the [[rationalization]] of the [[Whitehead product]] is the co-binary part of the [[Sullivan model|Sullivan differential]] in [[rational homotopy theory]]. First we make explicit some notation and normalization conventions that enter this statement:

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

Then:


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

+-- {: .num_example #WhiteheadProductCorrespondingToComplexHopfFibration}
###### Example
**([[Whitehead product]] corresponding to [[complex Hopf fibration]])**

For $X = S^2$ the [[2-sphere]], consider the following two [[elements]] of its [[homotopy groups]] ([[homotopy groups of spheres|of spheres]], as it were):

1. $id_{S^2} \in \pi_2\big( S^2 \big)$ (represented by the [[identity function]] $S^2 \to S^2$)

1. $h_{\mathbb{C}} \in \pi_3\big(  S^3 \big)$ (represented by the [[complex Hopf fibration]])

Then the Whitehead product satisfies

$$
  \big[
    id_{s^2},
    \; 
    id_{S^2}
  \big]
  \;=\;
  2 \cdot h_{\mathbb{C}}
  \,.
$$

=--


\linebreak

## References

### General

Named after [[J. H. C. Whitehead]].

The concept originates with

* {#HiltonWhitehead53} [[Peter Hilton]], [[J. H. C. Whitehead]], _Note on the Whitehead Product_, Annals of Mathematics Second Series, Vol. 58, No. 3 (Nov., 1953), pp. 429-442  ([jstor:1969746](https://www.jstor.org/stable/1969746))

* {#Hilton55} [[Peter Hilton]], _On the homotopy groups of unions of spheres_, J. London Math. Soc., 1955, 30, 154–172 ([[Hilton55.pdf:file]])


See also 

* Wikipedia _[Whitehead product](http://en.wikipedia.org/wiki/Whitehead_product)_

Discussion of Whitehead products specifically of [[homotopy groups of spheres]]:

* {#James56} [[Ioan Mackenzie James]], _On the Suspension Triad_, Annals of Mathematics Second Series, Vol. 63, No. 2 (Mar., 1956), pp. 191-247 ([arXiv:1969607](https://www.jstor.org/stable/1969607))

* {#James57} [[Ioan Mackenzie James]], _On the Suspension Sequence_, Annals of Mathematics Second Series, Vol. 65, No. 1 (Jan., 1957), pp. 74-107 ([arXiv:1969666](https://www.jstor.org/stable/1969666))


Discussion of Whitehead products in [[homotopy type theory]]:

* [[Guillaume Brunerie]], section 3.3 of _On the homotopy groups of spheres in homotopy type theory_ ([arXiv:1606.05916](https://arxiv.org/abs/1606.05916))


### In rational homotopy theory
  {#ReferencesInRationalHomotopyTheory}

Discussion of Whitehead products in [[rational homotopy theory]]:

* {#Quillen69} [[Daniel Quillen]], section I.5 of _Rational Homotopy Theory_, Annals of Mathematics Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([jstor:1970725](https://www.jstor.org/stable/1970725))


* Christopher Allday, _Rational Whitehead products and a spectral sequence of Quillen_, Pacific J. Math. Volume 46, Number 2 (1973), 313-323 ([euclid:1102946308](https://projecteuclid.org/euclid.pjm/1102946308))

* Christopher Allday, _Rational Whitehead product and a spectral sequence of Quillen, II_, Houston Journal of Mathematics, Volume 3, No. 3, 1977 ([pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.434.8821&rep=rep1&type=pdf))

* {#DeligneGriffithsMorganSullivan75} [[Pierre Deligne]], [[Phillip Griffiths]], [[John Morgan]], [[Dennis Sullivan]], _Real homotopy theory of Kähler manifolds_, Invent Math (1975) 29: 245 ([doi:10.1007/BF01389853](https://doi.org/10.1007/BF01389853))

* {#AndrewsArkowitz78} Peter Andrews, [[Martin Arkowitz]], _Sullivan's Minimal Models and Higher Order Whitehead Products_, Canadian Journal of Mathematics, 30(5), 961-982, 1978 ([doi:10.4153/CJM-1978-083-6](https://doi.org/10.4153/CJM-1978-083-6))

* Francisco Belchí, [[Urtzi Buijs]], José M. Moreno-Fernández, Aniceto Murillo, _Higher order Whitehead products and $L_\infty$ structures on the homology of a DGL_, Linear Algebra and its Applications, Volume 520 (2017), pages 16-31 ([arXiv:1604.01478](https://arxiv.org/abs/1604.01478))
    


* Takahito Naito, _A model for the Whitehead product in rational mapping spaces_ ([arXiv:1106.4080](https://arxiv.org/abs/1106.4080))


[[!redirects Whitehead products]]