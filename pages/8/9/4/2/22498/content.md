
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[representation theory]] of the [[symmetric groups]].

## Properties

### Irreducible representations
 {#IrreducibleRepresentations}


\begin{proposition}\label{IrrepsLabeledByPartitions}
In [[characteristic zero]], the [[irreducible representations]] of the symmetric group are, up to [[isomorphism]], given by the [[Specht modules]] labeled by [[partitions]] $\lambda \in Part(n)$. 
\end{proposition}
(e.g. [Sagan 01, Thm. 2.4.6](#Sagan01)).

### Dimension of irreps and hook length

Over the [[complex numbers]]:

The [[dimension]] of the [[irrep]] $S^{(\lambda)}$ ([[Specht module]]) equals the [[number]] of [[standard Young tableau]] of shape $\lambda$:

\[
  \label{DimensionOfSPechtModuleEqualsNumberofStandardYoungDiagrams}
  dim\big(S^{(\lambda)}\big)  
  \;=\;
  \left\vert
    sYTableaux_\lambda
  \right\vert
\]

(e.g. [Sagan, Thm. 2.6.5](#Sagan01)) 

Moreover, the [[number]] of [[standard Young tableaux]] of shape $\lambda$ is given by the [[hook length formula]]

\[
  \label{HookLengthFormulaCountingNumberOfStandardYoungTableau}
  \left\vert 
    sYTableaux_\lambda
  \right\vert
    \;=\; 
    n!
    \,  
    \left(
      \prod_{
        { 1 \leq i \leq rows(\lambda) }   
        \atop
        { 1 \leq j \leq \lambda_i }
      } 
      \ell hook_\lambda(i,j)
    \right)^{-1}
  \,.
\]


This is due to [Frame, Robinson & Thrall 54](hook+length+formula#FrameRobinsonThrall54). Textbook accounts include [Stanley 99, Cor. 7.21.6](hook+length+formula#Stanley99), [Sagan 01 Thm. 3.10.2](#Sagan01).

Combining (eq:DimensionOfSPechtModuleEqualsNumberofStandardYoungDiagrams) with (eq:HookLengthFormulaCountingNumberOfStandardYoungTableau) gives the [[hook length formula]] for the [[dimension]] of the [[Specht modules]]

$$
  dim\big(S^{(\lambda)}\big)  
  \;=\;
  n!  
  \left(
    \prod_{
      { 1 \leq i \leq rows(\lambda) }   
      \atop
      { 1 \leq j \leq \lambda_i }
    } 
    \ell hook_\lambda(i,j)
  \right)^{-1}
  \,.
$$

(e.g. [James 78, Thm. 20.1](#James78))


[[!include hook length and content formulas -- table]]


## Examples

### The standard representation

\begin{example}\label{StandardRepresentation}
**(standard representation)**
\linebreak
  What is sometimes called the *standard representation* of the [[symmetric group]] $Sym_n$ is the [[restricted representation|restriction]] of the $n$-dimensional [[permutation representation]] on $k^n$ (by [[permutation]] of the canonical [[linear basis|basis vectors]]) to the $(n-1)$-dimensional [[linear subspace|subspace]] where the [[sum]] of [[coefficients]] of these basis vectors is [[zero]].

This is an [[irreducible representation]] whose corresponding [[partition]] (according to Prop. \ref{IrrepsLabeledByPartitions}) is $\big((n-1),1\big)$.
\end{example}
(cf. [Kao Def. 2.5](#Kao), [[Groupprops]]: *[Standard representation of the symmetric group](https://groupprops.subwiki.org/wiki/Standard_representation_of_the_symmetric_group)*)




\begin{example}
\label{UnitarizationOfStandardRepOfSym3}
  The [[unitarization]] of the [standard representation](representation+theory+of+the+symmetric+group#StandardRepresentation) of the [[symmetric group]] $Sym_3$ has two generating [[permutations]] represented by (what in [[quantum information theory]] is called)

1. the [[Pauli Z-gate]] $Z$, 

1. the [[rotation gate]] $R_y(8\pi/3) = -R_y(2\pi/3)$.

\end{example}
\begin{proof}
The defining [[permutation representation]] of $Sym_3$ --- with canonical [[linear basis]]  $\{e_1, e_2, e_3\}$ acted on as 
$
  \sigma e_i \,=\, e_{\sigma(i)}
$ ---
is [[unitary representation|unitary]] with respect to the canonical [[inner product]] $\langle e_i, e_j\rangle \equiv \delta_{i j}$.

Therefore a [[unitary representation|unitary]] form of the standard representation is obtained as the [[orthogonal complement]] of the [[trivial representation|trivial]] [[subrepresentation]] [[linear span|spanned]] by $e_1 + e_2 + e_3$.

One [[orthonormal basis|orthonormal]] [[linear basis]] for this [[orthogonal complement]] is clearly:

$$
  \Bigg(
  \;
  \left[
    \begin{array}{c}
      1
      \\
      0
    \end{array}
  \right]
  \;\coloneqq\;
  \tfrac{1}{\sqrt{6}}
  (e_1 + e_2 - 2 e_3)
  \;,\,\;\;\;
  \left[
  \begin{array}{c}
    0
    \\
    1
  \end{array}
  \right]
  \;\coloneqq\;
  \tfrac{1}{\sqrt{2}}
  (e_1 - e_2)
  \;
  \Bigg)
  \,.
$$

On this basis, the [[transposition]] $(213)$ acts as
$$
  (213)
  \,
  \tfrac{1}{\sqrt{6}}
  (e_1 + e_2 - 2 e_3)
  \;=\;
  \tfrac{1}{\sqrt{6}}
  (e_1 + e_2 - 2 e_3)
  \,,
$$
and
$$
  (213)
  \,
  \tfrac{1}{\sqrt{2}}
  (e_1 - e_2)
  \;=\;
  -
  \tfrac{1}{\sqrt{2}}
  (e_1 - e_2)
  \,,
$$
hence is given by the [[matrix]] 
$$
  [213] 
  \;\equiv\;
  \underset{
    Z
  }{
  \underbrace{
  \left[
  \begin{array}{c}
    1 & 0 
    \\  
    0 & -1
  \end{array}
  \right]
  }
  }
  \,,
$$
which in [[quantum information theory]] is called the *[[Pauli Z-gate]]*.

On the other hand, the [[cyclic permutation]] $(231)$ acts as
$$
  (231)
  \,
  \tfrac{1}{\sqrt{6}}(e_1 + e_2 - 2 e_3)
  \;=\;
  \tfrac{1}{\sqrt{6}}(- 2 e_1 + e_2 + e_3)
  \;=\;
  -\tfrac{1}{2}
  \tfrac{1}{\sqrt{6}}
  (e_1 + e_2 - 2 e_3)
  -
  \tfrac{\sqrt{3}}{2}
  \tfrac{1}{\sqrt{2}}(e_1 - e_2)
$$
and
$$
  (231)
  \,
  \tfrac{1}{\sqrt{2}}(e_1 - e_2)
  \;=\;
  \tfrac{1}{\sqrt{2}}(e_2 - e_3)
  \;=\;
  \tfrac{\sqrt{3}}{2}
  \tfrac{1}{\sqrt{6}}(e_1 + e_2 - 2 e_3)
  -
  \tfrac{1}{2}
  \tfrac{1}{\sqrt{2}}
  (e_1 - e_2)
$$
and is hence given by the [[matrix]]
$$
  [231]
  \;=\; 
  -
  \left[
    \begin{array}{cc}
      1/2 & - \sqrt{3}/2
      \\
      \sqrt{3}/2 & 1/2
    \end{array}
  \right]
  \;=\;
  \underset{
    R_y(4\pi \tfrac{2}{3})
  }{
  \underbrace{
  \left[
    \begin{array}{cc}
      cos(4\pi/3) & - sin(4\pi/3)
      \\
      sin(4\pi/3) & cos(4\pi/3)
    \end{array}
  \right]
  }
  }
  \,,
$$
known in [[quantum information theory]] as a *[[rotation gate]]*. 
\end{proof}



## Related concepts

* [[Specht module]]

* [[parastatistics]]

* [[representation theory of the general linear group]]

* [[representation theory of the special unitary group]]

* [[Schur-Weyl duality]]

* [[Jucys-Murphy element]]

* [[FI-representation]]


## References

Monographs:

* {#James78} [[G. D. James]], *The Representation Theory of the Symmetric Groups*, Lecture Notes in Mathematics **682**, Springer (1978) &lbrack;[doi:10.1007/BFb0067708](https://link.springer.com/book/10.1007/BFb0067708)&rbrack;

* [[Gordon D. James]], Adalbert Kerber: *The Representation Theory of the Symmetric Group*, Cambridge University Press (1984) &lbrack;[doi:10.1017/CBO9781107340732](https://doi.org/10.1017/CBO9781107340732)&rbrack;

* {#Diaconis88} [[Persi Diaconis]], Chapter 7 of: *Group Representations  in Probability  and  Statistics*, IMS Lecture Notes Monogr. Ser., 11: 198pp. (1988) ([jstor:i397389](https://www.jstor.org/stable/i397389), [ISBN: 0940600145](https://projecteuclid.org/ebooks/institute-of-mathematical-statistics-lecture-notes-monograph-series/Group-representations-in-probability-and-statistics/toc/10.1214/lnms/1215467407), [pdf](https://jdc.math.uwo.ca/M9140a-2012-summer/Diaconis.pdf))

* {#Fulton97} [[William Fulton]], Section 7 of: _Young Tableaux, with Applications to Representation Theory and Geometry_, Cambridge U. Press, 1997 ([doi:10.1017/CBO9780511626241](https://doi.org/10.1017/CBO9780511626241))


* {#Sagan01} [[Bruce Sagan]], _The symmetric group_, Springer 2001 ([doi:10.1007/978-1-4757-6804-6](https://link.springer.com/book/10.1007/978-1-4757-6804-6), [pdf](http://math.sfsu.edu/federico/Clase/RepTh/sagan.pdf))

See also:

* Wikipedia, *[Representation theory of the symmetric group](https://en.wikipedia.org/wiki/Representation_theory_of_the_symmetric_group)*

Notes:

* [[Yufei Zhao]], _Young Tableaux and the Representations of the Symmetric Group_ ([pdf](https://yufeizhao.com/research/youngtab-hcmr.pdf), [[ZhaoYoungTableaux.pdf:file]])

* {#Kao} Daphne Kao: *Representations of the Symmetric Group*, VIGRE 2010 &lbrack;[pdf](https://www.math.uchicago.edu/~may/VIGRE/VIGRE2010/REUPapers/Kao.pdf)&rbrack;

Discussion of [[character of a linear representation|characters]] for the [[symmetric group]] that depend only on [[Cayley distance]] from the [[neutral element]] ("block character"):

* {#GnedinGorinKerov11} [[Alexander Gnedin]], [[Vadim Gorin]], [[Sergei Kerov]], *Block characters of the symmetric groups*, Journal of Algebraic Combinatorics, 38, no. 1 (2013), 79-101 ([arXiv:1108.5044](https://arxiv.org/abs/1108.5044), [doi:10.1007/s10801-012-0394-9](https://doi.org/10.1007/s10801-012-0394-9))

From the perspective of the [[seminormal representation]]:

On the [[representation theory of the symmetric group]] via the [[seminormal representation]]:

* {#VershikOkounkov04} [[Anatoly Vershik]], [[Andrei Okounkov]], *A New Approach to the Representation Theory of the Symmetric Groups*,
Part I: Selecta Mathematica, New Series **2**, 581-605 ([arXiv:math/0503040](https://arxiv.org/abs/math/0503040), [doi:10.1007/BF02433451](https://doi.org/10.1007/BF02433451));
Part II (incorporates Part I in revised and improved form):
Russian version: [Записки научных семинаров ПОМИ 307 (2004), 57–98](ftp://ftp.pdmi.ras.ru/pub/publicat/znsl/v307/p057.ps.gz) (Zapiski nauchnyh seminarov POMI 307 (2004), 57–98); 
English version: Journal of Mathematical Sciences 131 (2005), 5471–5494 ([doi:10.1007/s10958-005-0421-7](https://doi.org/10.1007/s10958-005-0421-7)).

 

In relation to [[quantum information theory]]:

* [[Alonso Botero]], *Quantum Information and the Representation Theory of the Symmetric Group*, Rev. colomb. mat. vol.50 no. 2 Bogotá July/Dec. 2016 ([doi:10.15446/recolma.v50n2.62210](https://doi.org/10.15446/recolma.v50n2.62210), [pdf](http://www.scielo.org.co/pdf/rcm/v50n2/v50n2a05.pdf))

[[!redirects representation theory of the symmetric groups]]
[[!redirects representation theory of symmetric groups]]

[[!redirects symmetric group representation]]
[[!redirects symmetric group representations]]

[[!redirects representation of the symmetric group]]
[[!redirects representations of the symmetric group]]

[[!redirects representation of a symmetric group]]
[[!redirects representations of a symmetric group]]

