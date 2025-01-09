
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

* automatic table of contents
{: toc}

## Idea

The **adjoint triangle theorem** in [[category theory]] gives conditions under which, given a [[pair]] of [[functors]] and an [[adjoint functor]], further adjoints exist.

Depending on the specific assumptions, the theorem has several variants. The following gives the most common formulation going back to [Dubuc (1968)](#dubuc68) and [Huq (1970)](#huq70).

## Statement ##

+-- {: .num_theorem #ATT}
###### Theorem

Suppose that $U \colon B\to C$ is a [[functor]] which has a [[left adjoint]] $F \,\colon\, C\to B$ with the property that the diagram
$$ 
  F U F U 
  \;
  \underoverset
    {\epsilon F U}
    {F U \epsilon}  
    {\rightrightarrows} 
   \; 
   F U \xrightarrow{\epsilon} 1_B 
$$
is a pointwise [[coequalizer]] (i.e. $U$ is of [[descent type]]).  Then for $A$ a category with [[reflexive coequalizer|coequalizers of reflexive pairs]], a functor $R \colon A\to B$ has a [[left adjoint]] if and only if the composite $U R$ does.

=--
+-- {: .proof}
###### Proof

The direction "only if" is obvious since adjunctions compose.  For "if", let $F'$ be a left adjoint of $U R$, and define $L:B\to A$ to be the pointwise coequalizer of
$$ F' U F U \xrightarrow{F' U \epsilon} F' U $$
and
$$
  F' U F U \xrightarrow{F' U \theta U}
  F' U R F' U \xrightarrow{\epsilon' F' U}
  F' U
$$
where $\theta:F \to R F'$ is the [[mate]] of the equality $U R = U R$ under the adjunctions $F\dashv U$ and $F'\dashv U R$.  One then verifies that this works.

=--

+-- {: .num_remark #Monadic}
###### Remark
The hypotheses on $U$ are satisfied whenever it is [[monadic functor|monadic]].
=--

+-- {: .num_remark #RegMono}
###### Remark
In fact, it suffices to assume that each counit $\epsilon : F U b \to b$ is a [[regular epimorphism]], rather than it is the coequalizer of a specific given pair of maps.  See [(Street-Verity), Lemma 2.1](#StreetVerity).
=--

## Ramifications

Similarly, the [[adjoint lifting theorem]] states conditions on a square of functors in order to ensure the existence of certain adjoints. Since a triangle can be viewed as a square with 'two sides composed', it is possible to deduce the adjoint lifting theorem from the adjoint triangle theorem as a corollary.

It is also possible to derive the [[monadicity theorem]] from the adjoint triangle theorem [Dubuc (1968)](#dubuc68).

## Related entries

* [[adjoint functor theorem]]

* [[adjoint lifting theorem]]

## References ##

* [[Michael Barr]], [[Charles Wells]], section 3.7, pp.131 in: *[[Toposes, Triples, and Theories]]*, Springer (1985), Reprints in Theories and Applications of Categories **12** (2005) 1-287 &lbrack;[tac:tr12](http://www.tac.mta.ca/tac/reprints/articles/12/tr12abs.html)&rbrack; 
 
* {#dubuc68} [[Eduardo Dubuc]], _Adjoint triangles_, pp.69-81 in LNM **61** Springer Heidelberg 1968. &lbrack;[doi:10.1007/BFb0077118](https://doi.org/10.1007/BFb0077118)&rbrack;

* {#huq70}S. A. Huq, _An interpolation theorem for adjoint functors_, Proc. AMS **25** (1970) pp.880-883. ([pdf](https://www.ams.org/journals/proc/1970-025-04/S0002-9939-1970-0260824-1/S0002-9939-1970-0260824-1.pdf))

* Geun Bin Im, [[Gregory Maxwell Kelly]], _Some remarks on conservative functors with left adjoints_,  J. Korean Math. Soc. __23__ (1986),  no. 1, 19&#8211;33, [MR87i:18002b](http://www.ams.org/mathscinet-getitem?mr=843247), [pdf](https://koreascience.kr/article/JAKO198621048976714.pdf)

* I. B. Im, [[Max Kelly|G. M. Kelly]], _Adjoint-Triangle Theorems for Conservative Functors_, Bulletin of the Australian Mathematical Society **36** 1 (1987) pp.133-136. &lbrack;[doi:10.1017/S000497270002637X](https://doi.org/10.1017/S000497270002637X)&rbrack;

* [[John Power]], _A unified approach to the lifting of adjoints_, Cahiers de Topologie et Géométrie Différentielle Catégoriques **29** 1 (1988) 67-77. ([numdam](http://www.numdam.org/item/CTGDC_1988__29_1_67_0))

* {#StreetVerity} [[Ross Street]], [[Dominic Verity]], _The comprehensive factorization and torsors_, Theory and Applications of Categories **23** 3 (2010) 42-75. ([TAC](http://www.tac.mta.ca/tac/volumes/23/3/23-03abs.html))

* [[Walter Tholen]], _Adjungierte Dreiecke, Colimites und Kan-Erweiterungen_, Mathematische Annalen **217** (1975) pp.121-129. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/img/?PPN=GDZPPN002311682))

See also Proposition 27 and Corollary 28 of:

* [[Ross Street]], _Wood fusion for magmal comonads_, [arXiv:2311.07088](https://arxiv.org/abs/2311.07088) (2023)

Generalizations of the adjoint triangle theorem to [[2-categories]] are considered in

* [[Fernando Lucatelli Nunes]], _On biadjoint triangles_, Theory and Applications of Categories **31** 9 (2016) 217-256. [TAC](http://tac.mta.ca/tac/volumes/31/9/31-09abs.html)

* [[Fernando Lucatelli Nunes]], _On lifting of biadjoints and lax algebras_, General Algebraic Structures with Applications **9** 1 (2018) 29-58. &lbrack;[doi:10.29252/CGASA.9.1.29](https://doi.org/10.29252/CGASA.9.1.29), [arXiv:1607.03087](https://arxiv.org/abs/1607.03087)&rbrack;

[[!redirects adjoint triangle]]
[[!redirects adjoint triangles]]
