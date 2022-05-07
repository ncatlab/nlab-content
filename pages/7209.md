
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $G$ a [[topological group]] a _compact subgroup_ is a topological [[subgroup]] $K \subset G$ which is a [[compact group]].

+-- {: .num_defn}
###### Definition

A [[compact topological space|compact]] [[subgroup]] $K \hookrightarrow G$ is called **maximal compact** if every compact subgroup of $G$ is [[conjugation|conjugate]] to a subgroup of $K$.

=--

If it exists then, by definition, it is unique up to conjugation.

## Properties

+-- {: .num_defn #AlmostConnected}
###### Definition

A [[locally compact topological group]] $G$ is called **[[almost connected topological group|almost connected]]** if the [[quotient]] [[topological space]] $G/G_0$ (of $G$ by the [[connected component]] of the neutral element) is  [[compact topological space|compact]].

=--

See for instance ([Hofmann-Morris, def. 4.24](#HofmannMorris)).

+-- {: .num_defn }
###### Example

Every [[compact topological space|compact]] and every [[connected topological space|connected]] [[topological group]] is almost connected.

Also every [[quotient]] of an almost connected group is almost connected.

=--

+-- {: .num_theorem #MalcevIwasawa}
###### Theorem

Let $G$ be a [[locally compact topological space|locally compact]] [almost connected](#AlmostConnected) [[topological group]].

Then 

* $G$ has a maximal compact subgroup $K$;

* the [[coset]] space $G/K$ is [[homeomorphism|homeomorphic]] to a [[Euclidean space]].


=--

This is due to ([Malcev](#Malcev)) and ([Iwasawa](#Iwasawa)). See for instance ([Stroppel, theorem 32.5](#Stroppel)).

+-- {: .num_theorem}
###### Theorem

Let $G$ be a [[locally compact topological space|locally compact]] [almost connected](#AlmostConnected) [[topological group]].

Then a [[compact topological space|compact]] subgroup $K \hookrightarrow G$ is maximal compact precisely if the [[coset]] space $G/K$ is [[contractible space|contractible]]

(in which case, due to theorem \ref{MalcevIwasawa}, it is necessarily [[homeomorphism|homeomorphic]] to a [[Euclidean space]]).

=--

This is ([Antonyan, theorem 1.2](#Antonyan)).


+-- {: .num_remark}
###### Remark

In particular, in the above situation the [[subgroup]] inclusion

$$
  K \hookrightarrow G
$$

is a [[homotopy equivalence]] of [[topological spaces]]. 

=--

## Examples


### For Lie groups
 {#ExamplesForLieGroups}

The following table lists some [[Lie groups]] and their maximal compact Lie subgroups (e.g. [Conrad](#Conrad)). See also _[[compact Lie group]]_.


|            Lie group                         |     maximal compact subgroup    |
|----------------------------------------------|---------------------------------|
| [[real numbers|real]] [[general linear group]] $GL(n, \mathbb{R})$  | [[orthogonal group]] $O(n)$    |
| its connected component $GL(n,\mathbb{R})_0$ | [[special orthogonal group]] $SO(n)$ |
| [[complex numbers|complex]] [[general linear group]] $GL(n, \mathbb{C})$  | [[unitary group]] $U(n)$        |
| [[complex numbers|complex]] [[special linear group]] $SL(n, \mathbb{C})$  | [[special unitary group]] $SU(n)$        |
| [[symplectic group]] $Sp(2n,\mathbb{R})$                | [[unitary group]] $U(n)$        |
| [[complex symplectic group]] $Sp(2n,\mathbb{C})$ | [[compact symplectic group]] $Sp(n)$ |
| [[Narain group]] $O(n,n)$ | [[direct product group]] of two [[orthogonal groups]] $O(n) \times O(n)$ |
| [[unitary group]] $U(p,q)$ | $U(p) \times U(q)$ |
| special [[Lorentz group|Lorentz]]/[[anti de Sitter group|AdS]] etc. group $SO(p,q)$ | $S\big(O(p) \times O(q)\big)$ |
| Lorentz / AdS [[pin group]] $Pin(q,p)$ | $Pin(q) \times Pin(q) / \{(1,1), (-1,-1)\}$ |

The following table lists specifically the maximal compact subgroups of the "$E$-series" of Lie groups culminating in the  [[exceptional Lie groups]] $E_n$.

| $n$ | [[real form]] $E_{n(n)}$ | maximal compact subgroup $H_n$ | $dim(E_{n(n)})$ | $dim(E_{n(n)}/H_n ) $ |
|---|---|---|---|---|
| 2 | $SL(2, \mathbb{R}) \times \mathbb{R}$ | $SO(2)$ | 4 | 3 |
| 3 | $SL(3,\mathbb{R}) \times SL(2,\mathbb{R})$ | $SO(3) \times SO(2)$ | 11 | 7 | 
| 4 | $SL(5, \mathbb{R})$ | $SO(5)$ | 24 | 14 |
| 5 | $Spin(5,5)$  | $(Sp(2) \times Sp(2))/\mathbb{Z}_2$ | 45 | 25|
| 6 | [[E6|E6(6)]] | $Sp(4)/\mathbb{Z}_2$ | 78 | 42 |
| 7 | [[E7|E7(7)]] | $SU(8)/\mathbb{Z}_2$ | 133 | 70 |
| 8 | [[E8|E8(8)]] | $Spin(16)/\mathbb{Z}_2$ | 248 | 128 |

### Counterexamples

A maximal compact subgroup may not exist at all without the almost connectedness assumption. An example is the [[Prüfer group]] $\mathbb{Z}[1/p]/\mathbb{Z}$ endowed with the discrete ($0$-dimensional) smooth structure. This is a union of an increasing sequence of finite cyclic groups, each obviously compact.

## Related concepts

* [[closed subgroup]]

* [[locally compact topological group]]

* [[compact Lie group]]

* [[maximal subgroup]]

* [[maximal torus]]

* [[reduction and lift of structure groups]]

## References


Textbooks with relevant material include

* M. Stroppel, _Locally compact groups_, European Math. Soc., (2006)
  {#Stroppel}

* Karl Hofmann, Sidney Morris, _The Lie theory of connected pro-Lie groups_, Tracts in Mathematics 2, European Mathematical Society,  (2000)
 {#HofmannMorris}


See also

* Wikipedia, _[Maximal compact subgroup](http://en.wikipedia.org/wiki/Maximal_compact_subgroup)_


Original articles include

* {#Malcev} A. Malcev, _On the theory of the Lie groups in the large_, Mat.Sbornik N.S. vol. 16 (1945) pp. 163-189
 


* {#Iwasawa} K. Iwasawa, _On some types of topological groups_, Ann. of Math. vol.50 (1949) pp. 507-558.
 

* M. Peyrovian, _Maximal compact normal subgroups_, Proceedings of the American Mathematical Society, Vol. 99, No. 2, (1987) ([jstor](http://www.jstor.org/pss/2046647))

* {#Antonyan} Sergey A. Antonyan, _Characterizing maximal compact subgroups_ ([arXiv:1104.1820v1](http://arxiv.org/abs/1104.1820v1)) 

The maximal compact subgroups inside the (indefinite) rotation groups

* {#Conrad} [[Brian Conrad]], _Examples of maximal compact subgroups_ ([pdf](http://virtualmath1.stanford.edu/~conrad/210CPage/handouts/maxcompact.pdf))
 

[[!redirects maximal compact subgroups]]

[[!redirects compact subgroup]]
[[!redirects compact subgroups]]
