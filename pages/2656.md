
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## The idea

Young diagrams are used to describe many objects in algebra and combinatorics, including:

* integer [[partitions]].  For example, the integer partition 

  $$ 17 = 5 + 4 + 4 + 2 + 1 + 1 $$ 

  is drawn as the Young diagram

+-- {: #Young style="text-align:center"}
<svg width="120" height="140" xmlns="http://www.w3.org/2000/svg" se:nonce="39384" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <desc>Young diagram (5,4,4,2,1,1)</desc>
 <g>
  <title>Layer 1</title>
  <rect x="10" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_1"/>
  <rect x="30" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_2"/>
  <rect x="50" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_3"/>
  <rect x="70" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_4"/>
  <rect x="90" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_5"/>
  <rect x="10" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_6"/>
  <rect x="30" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_7"/>
  <rect x="50" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_8"/>
  <rect x="70" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_9"/>
  <rect x="10" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_10"/>
  <rect x="30" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_11"/>
  <rect x="50" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_12"/>
  <rect x="70" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_13"/>
  <rect x="10" y="70" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_14"/>
  <rect x="30" y="70" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_15"/>
  <rect x="10" y="90" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_16"/>
  <rect x="10" y="110" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_17"/>
 </g>
</svg>
=--

* [[conjugacy classes]] in $S_n$.

* [[irreducible representations]]:

  * [[irreducible representations]] of the [[symmetric groups]] $S_n$ over any field of characteristic zero

  * [[irreducible representations|irreducible]] (algebraic) representation of the [[special linear groups]] $SL(N,\mathbb{C})$

  * [[irreducible representation|irreducible]] [[unitary representations]] of the [[special unitary group|special unitary groups]] $SU(N)$

* [[elementary symmetric functions]]

* [[Schur functors]]

* [[linear basis|basis]] vectors for the free [[lambda-ring]] on one generator, $\Lambda$

* [[flag varieties]] for the [[special linear groups]] $SL(N,k)$, where $k$ is any field

* [[characteristic classes]] for complex [[vector bundles]]: that is, [[cohomology]] classes on the [[classifying spaces]] of the [[general linear groups]] $GL(N,\mathbb{C})$

* [[characteristic classes]] for hemitian vector bundles: that is, [[cohomology]] classes on the [[classifying spaces]] of the [[unitary groups]] $U(N)$

* finite-dimensional [[C*-algebras]]: any such algebra is of the form $M_{n_1}(\mathbb{C}) \oplus \cdots \oplus M_{n_k}(\mathbb{C})$ for some unique list of natural numbers $n_1 \ge n_2 \ge \cdots \ge n_k$.

* finite [[abelian group|abelian]] [[p-groups]]: any such group is of the form $\mathbb{Z}/p^{n_1} \oplus \cdots \oplus \mathbb{Z}/p^{n_k}$ for some unique list of natural numbers $n_1 \ge n_2 \ge \cdots \ge n_k$.

* finite [[commutative algebra|commutative]] [[semisimple algebras]] over a [[prime field]] $\mathbb{F}_p$: any such algebra is of the form $\mathbb{F}_{p^{n_1}} \oplus \cdots \oplus \mathbb{F}_{p^{n_k}}$ for some unique list of natural numbers $n_1 \ge n_2 \ge \cdots \ge n_k$.

* the [[trace of a category|trace of the category of finite sets]] has isomorphism classes of objects corresponding to Young diagrams.

## Young diagram 

A **Young diagram** $F^\lambda$, also called **Ferrers diagram**, is a graphical representation of an unordered integer partition $\lambda = (\lambda_1\ge\lambda_2\ge\ldots\ge\lambda_l$). If $\lambda\vdash n$ is a partition of $n$ then the Young diagram has $n$ boxes. A partition can be addressed as a multiset over $\mathbb{N}$.

There are two widely used such representations. The _English_ one uses matrix-like indices, and the _French_ one uses Cartesian coordinate-like indices for the boxes $x_{i,j}$ in the diagram $F^\lambda$.

In the English representation the boxes are adjusted to the north-west in the 4th quadrant of a 2-dimensional Cartesian coordinate system, with the 'y'-axis being downward oriented. For instance the diagram $F^{(5,4,4,2,1,1)}$ representing the partition $(5,4,4,2,1,1)$ of $17$ is given in the English representation as:

+-- {: #Young style="text-align:center"}
<svg width="120" height="140" xmlns="http://www.w3.org/2000/svg" se:nonce="39384" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <desc>Young diagram (5,4,4,2,1,1)</desc>
 <g>
  <title>Layer 1</title>
  <rect x="10" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_1"/>
  <rect x="30" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_2"/>
  <rect x="50" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_3"/>
  <rect x="70" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_4"/>
  <rect x="90" y="10" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_5"/>
  <rect x="10" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_6"/>
  <rect x="30" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_7"/>
  <rect x="50" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_8"/>
  <rect x="70" y="30" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_9"/>
  <rect x="10" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_10"/>
  <rect x="30" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_11"/>
  <rect x="50" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_12"/>
  <rect x="70" y="50" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_13"/>
  <rect x="10" y="70" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_14"/>
  <rect x="30" y="70" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_15"/>
  <rect x="10" y="90" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_16"/>
  <rect x="10" y="110" width="20" height="20" fill="#ffdddd" stroke="#000000" stroke-width="2" id="svg_39384_17"/>
 </g>
</svg>
=--

Let $\mathbb{Y}$ be the set of Young diagrams. Important functions on Young 
diagrams include:

* {#Conjugation} **conjugation**: denoted by a prime $\prime : \mathbb{Y} \rightarrow \mathbb{Y}$
  reflects the Young diagram along its main diagonal (north-west to south-east). 
  In the above example the conjugated partition would be $\lambda^\prime=(6,4,3,3,1)$.
* **weight**: $wt \colon \mathbb{Y} \rightarrow \mathbb{N}$ provides the number 
  of boxes.
* **length**: $\ell \colon \mathbb{Y} \rightarrow \mathbb{N}$ provides the number
  of rows or equivalently the number of positive parts of the partition $\lambda$.
  The length of the conjugated diagram gives the number of columns. 
* **plus**: $+ \colon \mathbb{Y}\times \mathbb{Y} \rightarrow \mathbb{Y} :: 
  (\mu,\nu) \mapsto \mu + \nu = (\mu_1+\nu_1,\ldots,\mu_l+\nu_l)$
* **times**: $\times \colon \mathbb{Y}\times \mathbb{Y} \rightarrow \mathbb{Y} ::
 (\mu,\nu) \mapsto (\mu \cup \nu)_{\ge}$ the unordered union of the multisets. It
  follows that $\mu\times \nu =(\mu^\prime + \nu^\prime)^\prime$.

A **filling** of a Young diagram with elements from a set $S$ is called a [[Young tableau]].

## Skew Young diagram

A generalization of a Young diagram is a skew Young diagram. Let $\mu,\nu$ be two partitions, and let $\nu \le \mu$ be defined as $\forall i : \nu_i\le \mu_i$ (possibly adding trailing zeros). The **skew Young diagram** $F^{\mu/\nu}$ is given by the Young diagram $F^\mu$ with all boxes belonging to $F^\nu$ when superimposed removed. If $\mu=(5,4,4,2,1,1)$ and $\nu=(3,3,2,1)$ then $F^{\mu/\nu}$ looks like:

+-- {: #SkewYoung style="text-align:center"}
<svg width="120" height="140" xmlns="http://www.w3.org/2000/svg" se:nonce="39424" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:se="http://svg-edit.googlecode.com">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <desc>Skew Young diagram (5,4,4,2,1,1)/(3,3,2,1)</desc>
 <g>
  <title>Layer 1</title>
  <rect id="svg_39424_1" stroke-width="2" stroke="#cccccc" fill="none" height="20" width="20" y="10" x="0"/>
  <rect id="svg_39424_2" stroke-width="2" stroke="#cccccc" fill="none" height="20" width="20" y="10" x="20"/>
  <rect id="svg_39424_3" stroke-width="2" stroke="#cccccc" fill="none" height="20" width="20" y="10" x="40"/>
  <rect id="svg_39424_4" stroke-width="2" stroke="#000000" fill="#ffdddd" height="20" width="20" y="10" x="60"/>
  <rect id="svg_39424_5" stroke-width="2" stroke="#000000" fill="#ffdddd" height="20" width="20" y="10" x="80"/>
  <rect id="svg_39424_6" stroke-width="2" stroke="#cccccc" fill="none" height="20" width="20" y="30" x="0"/>
  <rect id="svg_39424_7" stroke-width="2" stroke="#cccccc" fill="none" height="20" width="20" y="30" x="20"/>
  <rect id="svg_39424_8" stroke-width="2" stroke="#cccccc" fill="none" height="20" width="20" y="30" x="40"/>
  <rect id="svg_39424_9" stroke-width="2" stroke="#000000" fill="#ffdddd" height="20" width="20" y="30" x="60"/>
  <rect id="svg_39424_10" stroke-width="2" stroke="#cccccc" fill="none" height="20" width="20" y="50" x="0"/>
  <rect id="svg_39424_11" stroke-width="2" stroke="#cccccc" fill="none" height="20" width="20" y="50" x="20"/>
  <rect id="svg_39424_12" stroke-width="2" stroke="#000000" fill="#ffdddd" height="20" width="20" y="50" x="40"/>
  <rect id="svg_39424_13" stroke-width="2" stroke="#000000" fill="#ffdddd" height="20" width="20" y="50" x="60"/>
  <rect id="svg_39424_14" stroke-width="2" stroke="#cccccc" fill="none" height="20" width="20" y="70" x="0"/>
  <rect id="svg_39424_15" stroke-width="2" stroke="#000000" fill="#ffdddd" height="20" width="20" y="70" x="20"/>
  <rect id="svg_39424_16" stroke-width="2" stroke="#000000" fill="#ffdddd" height="20" width="20" y="90" x="0"/>
  <rect id="svg_39424_17" stroke-width="2" stroke="#000000" fill="#ffdddd" height="20" width="20" y="110" x="0"/>
 </g>
</svg>
=--

* A skew diagram is called **connected** if all boxes share an edge.
* A skew diagram is called a **horizontal strip** if every column contains at most one box.
* A skew diagram is called a **vertical strip** if every row contains at most one box.
* conjugation, weight, length extend to skew diagrams accordingly.

## Young tableau

...

## Related concepts

* [[semistandard Young tableau]], [[hook-content formula]]

* [[Schur polynomial]]

* [[representation theory of the symmetric group]]

* [[representation theory of the general linear group]]

## References ##

Quick introduction

* Alexander Yong, What is ... a Young Tableau, _Notices of the American Mathematical Society_ *54* (February 2007), 240&#8211;241.   ([pdf](http://www.ams.org/notices/200702/whatis-yong.pdf))

Textbook accounts are in any book on [[representation theory]] in general and on the [[representation theory of the symmetric group]] in particular; such as:

* {#FultonHarris91} [[William Fulton]], [[Joe Harris]], _Representation Theory: a First Course_, Springer, Berlin, 1991 ([pdf](http://isites.harvard.edu/fs/docs/icb.topic1381051.files/fulton-harris-representation-theory.pdf))

More details:

* Kazuhiko Koike, Itaru Terada, _Young-diagrammatic methods for the representation theory of the classical groups of type $B_n$, $C_n$, $D_n$_,  Journal of Algebra, Volume 107, Issue 2, May 1987, Pages 466-511

* [[William Fulton]], _Young Tableaux, with Applications to Representation Theory and Geometry_, Cambridge U. Press, 1997 ([doi:10.1017/CBO9780511626241](https://doi.org/10.1017/CBO9780511626241))

* [[Ron M. Adin]], [[Yuval Roichman]], *Enumeration of Standard Young Tableaux*, Chapter 14 in: Miklós Bóna, *Handbook of Enumerative Combinatorics*, CRC Press 2015  ([arXiv:1408.4497](https://arxiv.org/abs/1408.4497), [ISBN:9781482220858](https://www.routledge.com/Handbook-of-Enumerative-Combinatorics/Bona/p/book/9781482220858))


Connection to [[algebraic geometry]]:

* C. de Concini, [[D. Eisenbud]], C. Procesi, _Young diagrams and determinantal varieties_, Invent. Math. __56__ (1980), 129-165.


category: combinatorics

[[!redirects Young diagram]]
[[!redirects Young diagrams]]
[[!redirects Ferrers diagram]]
[[!redirects Ferrers diagrams]]
[[!redirects Young tableau]]
[[!redirects Young tableaus]]
[[!redirects Young tableaux]]
