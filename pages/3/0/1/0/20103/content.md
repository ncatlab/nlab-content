

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc} 


## Idea

Given a [[linear representation]] of a [[finite group]] $G$ on a [[finite-dimensional vector space]] $V$, this induces an [[associated bundle|associated]] [[vector bundle]] over the [[classifying space]] $B G$. The [[characteristic classes]] of this vector bundle, notably it [[Chern classes]] or [[Pontryagin]], are hence entirely determined by the linear representation, and may be associated with it.

## Definition

Under the identification of the [[representation ring]] with the [[equivariant K-theory]] of the [[point]] (see [there](equivariant+K-theory#eq:RepresentationRingAsEquivariantKTheoryOfThePoint)) and the [[Atiyah-Segal completion]] map

$$
  R_{\mathbb{C}}(G)
  \simeq
  KU_G^0(\ast)
    \overset{ \widehat{(-)} }{\longrightarrow}
  KU(BG)
  
$$

one may ask for Chern classes of the K-theory class $\widehat{V} \in KU(B G)$ expressed in terms of the actual [[character]] of the [[representation]] $V$. 

(...)

## Examples

### First Chern class

There is a closed formula at least for the [[first Chern class]] ([Atiyah 61, appendix](#Atiyah61)):

For 1-dimensional representations $V$ their [[first Chern class]]  $c_1(\widehat{V}) \in H^2(B G, \mathbb{Z})$ is their image under the canonical [[isomorphism]] from 1-[[dimension|dimensional]] characters in $Hom_{Grp}(G,U(1))$ to the [[group cohomology]] $H^2_{grp}(G, \mathbb{Z})$ and further to the [[ordinary cohomology]] $H^2(B G, \mathbb{Z})$ of the [[classifying space]] $B G$:

$$
  c_1\left(\widehat{(-)}\right)
  \;\colon\;
  Hom_{Grp}(G, U(1))
  \overset{\simeq}{\longrightarrow}
  H^2_{grp}(G,\mathbb{Z})
  \overset{\simeq}{\longrightarrow}
  H^2(B G, \mathbb{Z})
  \,.
$$

More generally, for $n$-[[dimension|dimensional]] [[linear representations]] $V$ their [[first Chern class]] $c_1(\widehat V)$ is the previously defined first Chern-class of the [[line bundle]] $\widehat{\wedge^n V}$ corresponding to the  $n$-th [[exterior power]] $\wedge^n V$ of $V$. The latter is a 1-dimensional representation, corresponding to the [[determinant line bundle]] $det(\widehat{V}) = \widehat{\wedge^n V}$:

$$
  c_1(\widehat{V}) 
    \;=\; 
  c_1(det(\widehat{V})) 
    \;=\; 
  c_1( \widehat{\wedge^n V} )
  \,.
$$

([Atiyah 61, appendix, item (7)](#Atiyah61))

More explicitly, via the formula for the [[determinant]] as a [[polynomial]] in [[traces]] of powers (see [there](determinant#eq:DeterminantAsPolynomialInTracesOfPowers)) this means that the first Chern class of the $n$-dimensional representation $V$ is expressed in terms of its [[character]] $\chi_V$ as

\[
  \label{FirstChernClassOfRepresentationInTermsOfTheCharacter}
  c_1(V)
  =
  \chi_{\left(\wedge^n V\right)}
  \;\colon\;
  g
  \;\mapsto\;
  \underset{ 
     { k_1,\cdots, k_n \in \mathbb{N} }
     \atop
     { \underoverset{\ell = 1}{n}{\sum} \ell k_\ell = n }
  }{\sum}
  \underoverset{ l = 1 }{ n }{\prod} 
  \frac{ (-1)^{k_l + 1} }{ l^{k_l} k_l !  }
  \left(\chi_V(g^l)\right)^{k_l}
\]

For example, for a representation of dimension $n = 2$ this reduces to 

$$
  c_1(V)
  =
  \chi_{V \wedge V}
  \;\colon\;
  g
  \;\mapsto\;
  \frac{1}{2}
  \left( 
    \left( \chi_V(g)\right)^2
    -
    \chi_V(g^2)
  \right)
$$

(see also e.g. [tom Dieck 09, p. 45](representation+theory#tomDieck09))


+-- {: .num_example}
###### Example

Let $G =\mathbb{Z}_{2n+1}$ be a [[finite group|finite]] [[cyclic group]] of [[odd number|odd]] [[order of a group|order]] and let $k[\mathbb{Z}_{2n+1}]$ be its [[regular representation]]. Then the first Chern class vanishes:

$$
  c_1\big( k[\mathbb{Z}_{2n+1}]\big)
  \;=\;
  0
$$

=--

+-- {: .proof}
###### Proof

The underlying [[set]] of $\mathbb{Z}_{2n+1}$ constitutes the canonical [[linear basis]] of $k[\mathbb{Z}_{2n+1}]$. Moreover, this carries a canonical [[linear order]] $(e, g_1, g_2, \cdots, g_{2n+1})$. With respect to this ordering, the [[action]] of each group element $g \in \mathbb{Z}_n$ is by a [[cyclic permutation]]. Since for [[odd number]] of elements the [[signature of a permutation|signature]] of a [[cyclic permutation]] is $+1$, it follows that for every group element

$$
  g(e \wedge g_1 \wedge \cdots \wedge g_{2n+1})
  = 
  + e \wedge g_1 \wedge \cdots \wedge g_{2n+1}
  \,.
$$

This shows that the [[character of a linear representation|character]] of $\wedge^{2n+1}k[\mathbb{Z}_{2n+1}]$ equals that of the [[trivial representation]] $\mathbf{1}$

=--


## Properties

### Splitting principle
 {#SplittingPrinciple}


> see at [Symonds' explicit Brauer induction](Brauer+induction+theorem#SymondExplicitBrauerInduction)

Let $G$ be a [[finite group]], let the [[ground field]] to be the [[complex numbers]].

Then by the [[Brauer induction theorem]] every [[virtual representation]]

$$
  [V] \in R_\mathbb{C}(G)
$$

has a presentation as a virtual combination of [[induced representations]] of 1-[[dimension|dimensional]] representations:

$$
 [V]
 \;=\;
 \underset{
     \mathclap{
         {H_i \hookrightarrow G} 
           \atop 
         { 
           { W_i \in Rep(H_i) \,, }
           \atop
           { dim(W_i) =1 }
         }
     }
   }{\sum}
   n_i
  \left[
     ind_{H_i}^G W_i
  \right]
$$

Of course this expansion is not unique.

According to [Symonds 91, p. 4 & Prop. 2.4](#Symonds91), there is a natural choice for this expansion, and for this there holds a [[splitting principle]] for the corresponding [[Chern classes]] summarized in the [[total Chern class]] (formal sum of all [[Chern classes]]) 

$$
  c(V)
  \;\coloneqq\;
  1 + c_2(V) + c_2(V) + \cdots
  \;\in\;
  \underset{k}{\prod} H^{2 k}\big( B G , \mathbb{Z}\big)
$$

as follows:

\[
  \label{SplittingFormulaForChernCharacterOfLinearRepresentation}
  ch
  \left(
     V
  \right)
  \;=\;
  \underset{ 
     \mathclap{
         {H_i \hookrightarrow G} 
           \atop 
         { 
           { W_i \in Rep(H_i)\,, } 
           \atop
           { dim(W_i) = 1 } 
         }
     }
   }{\prod}
   \mathcal{N}_{H_i}^G
   \Big(
     \overset{
        \mathclap{
          = (1 + c_1(W_i))
        }
      }{
      \overbrace{
        ch\left(W_i\right)
      }
     }
     {}^{\alpha(W_i)}
   \Big)
   \;\;
   \in 
   \underset{ k \in \mathbb{N} }{\prod}
   H^{2k}\big(B G, \mathbb{Z} \big)
\]

where 

1. the transfer maps 

   \[
     \label{MultiplicativeTransfer}
     \mathcal{N}_H^G
     \;\colon\;
     H^\bullet(B H, \mathbb{Z})
       \longrightarrow
     H^\bullet( B G, \mathbb{Z} )
   \] 

   are from [Evens 63, bottom of p. 7](#Evens63),

1. the $\alpha(W_i)$-s are the [[Euler characteristics]] of certain [[CW-complexes]], described in [Symonds 91, p. 3](#Symonds91).

Here over the brace we used that the $W_i$ are 1-dimensional, so that at most their [[first Chern class]] may be non-vanishing.

Notice that the transfer maps (eq:MultiplicativeTransfer) are multiplicative under [[cup product]] ([Evens 63, prop. 4](#Evens63)), whence [Symonds 91](#Symonds91) refers to them as the "mutliplicative transfer".




## References

* {#Atiyah61} [[Michael Atiyah]], Appendix of _Characters and cohomology of finite groups_, Publications Mathématiques de l'IHÉS, Volume 9 (1961) , p. 23-64 ([numdam]( http://www.numdam.org/item?id=PMIHES_1961__9__23_0))

* {#Evens63} [[Leonard Evens]], _A Generalization of the Transfer Map in the Cohomology of Groups_, Transactions of the American Mathematical Society Vol. 108, No. 1 (Jul., 1963), pp. 54-65 ([doi:10.1090/S0002-9947-1963-0153725-1](https://doi.org/10.1090/S0002-9947-1963-0153725-1), [jstor:1993825](https://www.jstor.org/stable/1993825))

* {#Evens65} [[Leonard Evens]], _On the Chern Classes of Representations of Finite Groups_, Transactions of the American Mathematical Society, Vol. 115 (Mar., 1965), pp. 180-193 ([doi:10.2307/1994264](https://www.jstor.org/stable/1994264))

* {#LamberTondeur67} F. Kamber, [[Philippe Tondeur]], _Flat Bundles and Characteristic Classes of Group-Representations_, American Journal of Mathematics, Vol. 89, No. 4 (Oct., 1967), pp. 857-886 ([doi:10.2307/2373408](https://www.jstor.org/stable/2373408))

* {#Kroll87} Ove Kroll, _An Algebraic Characterisation of Chern Classes of Finite Group Representations_, Bulletin of the LMS, Volume19, Issue3 May 1987 Pages 245-248 ([doi:10.1112/blms/19.3.245](https://doi.org/10.1112/blms/19.3.245))

* J. Gunarwardena, B. Kahn, C. Thomas, _Stiefel-Whitney classes of real representations of finite groups_, Journal of Algebra Volume 126, Issue 2, 1 November 1989, Pages 327-347 (<a href="https://doi.org/10.1016/0021-8693(89)90309-8">doi:10.1016/0021-8693(89)90309-8</a>)

* {#Beauville01} Arnaud Beauville, _Chern classes for representations of reductive groups_ ([arXiv:math/0104031](https://arxiv.org/abs/math/0104031))

[[splitting principle]]:

* {#Symonds91} [[Peter Symonds]], _A splitting principle for group representations_, Comment. Math. Helv. (1991) 66: 169 ([dml:140229](https://eudml.org/doc/140229), [doi:10.1007/BF02566643](https://doi.org/10.1007/BF02566643))

[[!redirects characteristic classes of a linear representation]]
[[!redirects characteristic classes of linear representations]]

[[!redirects Chern class of a linear representation]]
[[!redirects Chern classes of a linear representation]]
[[!redirects Chern classes of linear representations]]

[[!redirects total Chern class of a linear representation]]
[[!redirects total Chern classes of a linear representation]]
[[!redirects total Chern classes of linear representations]]
 



