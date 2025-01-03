
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
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

In [[characteristic zero]], the [[irreducible representations]] of the symmetric group are, up to [[isomorphism]], given by the [[Specht modules]] labeled by [[partitions]] $\lambda \in Part(n)$ (e.g. [Sagan 01, Thm. 2.4.6](#Sagan01)).

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



## Related concepts

* [[Specht module]]

* [[representation theory of the general linear group]]

* [[representation theory of the special unitary group]]

* [[Schur-Weyl duality]]

* [[Jucys-Murphy element]]

* [[FI-representation]]

## References

Textbook accounts:

* {#James78} [[G. D. James]], *The Representation Theory of the Symmetric Groups*,  Lecture Notes in Mathematics, volume 682, Springer 1978 ([doi:10.1007/BFb0067708](https://link.springer.com/book/10.1007/BFb0067708), [pdf](http://www-users.math.umn.edu/~webb/oldteaching/Year2010-11/the-representation-theory-of-the-symmetric-groups-SLN.pdf))

* {#Diaconis88} [[Persi Diaconis]], Chapter 7 of: *Group Representations  in Probability  and  Statistics*, IMS Lecture Notes Monogr. Ser., 11: 198pp. (1988) ([jstor:i397389](https://www.jstor.org/stable/i397389), [ISBN: 0940600145](https://projecteuclid.org/ebooks/institute-of-mathematical-statistics-lecture-notes-monograph-series/Group-representations-in-probability-and-statistics/toc/10.1214/lnms/1215467407), [pdf](https://jdc.math.uwo.ca/M9140a-2012-summer/Diaconis.pdf))


* {#Fulton97} [[William Fulton]], Section 7 of: _Young Tableaux, with Applications to Representation Theory and Geometry_, Cambridge U. Press, 1997 ([doi:10.1017/CBO9780511626241](https://doi.org/10.1017/CBO9780511626241))


* {#Sagan01} [[Bruce Sagan]], _The symmetric group_, Springer 2001 ([doi:10.1007/978-1-4757-6804-6](https://link.springer.com/book/10.1007/978-1-4757-6804-6), [pdf](http://math.sfsu.edu/federico/Clase/RepTh/sagan.pdf))

See also:

* Wikipedia, *[Representation theory of the symmetric group](https://en.wikipedia.org/wiki/Representation_theory_of_the_symmetric_group)*

Notes:

* [[Yufei Zhao]], _Young Tableaux and the Representations of the Symmetric Group_ ([pdf](https://yufeizhao.com/research/youngtab-hcmr.pdf), [[ZhaoYoungTableaux.pdf:file]])


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

