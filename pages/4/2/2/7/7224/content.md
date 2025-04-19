+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

* table of contents
{:toc}

## Idea ##

The notion of *relative adjoint functor* (with respect to a functor $J$) is a generalisation of the notion of [[adjoint functor]], in which the domain of the left adjoint is not required to be the same as the codomain on the right adjoint. Dually, the notion of *relative coadjoint functor* is a generalisation of the notion of adjoint functor, in which the domain of the right adjoint is not required to be the same as the codomain of the left adjoint. In both cases, when $J$ is an [[identity functor]], the notions reduce to the notion of adjoint functor.

In generalization of the [relation between adjunctions and monads](monad#RelationBetweenAdjunctionsAndMonads),
relative adjoint functors are related to [[relative monads]], whilst relative coadjoint functors are related to [[relative comonads]].

## Definition ##

Fix a functor $J\colon A \to E$. Then, for a functor 

\[
	R \colon C \longrightarrow E
\] 

to have a _left $J$-relative adjoint_ (or _left $J$-adjoint_) means that there is a functor 

\[ 
	L \colon A \longrightarrow C
\]

and a [[natural isomorphism]] of the form

\[
  C\big(L(-),-\big) 
  \;\simeq\; 
  E\big(J(-),R(-)\big)
  \,.
\]

Such a situation is called a *$J$-relative adjunction* and is denoted $L \dashv_J R$.
\begin{tikzcd}
	& C \\
	A && E
	\arrow[""{name=0, anchor=center, inner sep=0}, "R", from=1-2, to=2-3]
	\arrow[""{name=1, anchor=center, inner sep=0}, "L", from=2-1, to=1-2]
	\arrow["J"', from=2-1, to=2-3]
	\arrow["\dashv"{anchor=center}, shift right=2, draw=none, from=1, to=0]
\end{tikzcd}

[[formal duality|Dually]], for a functor $L \colon C \longrightarrow E$ to have a _right $J$-relative coadjoint_ (or _right $J$-coadjoint_) $R \colon A \longrightarrow C$ means that there is a [[natural isomorphism]] of the form

\[
  E\big(L(-), J(-)\big) 
   \;\simeq\; 
  C\big(-, R(-)\big)
\]

Such a situation is called a *$J$-relative coadjunction* and is denoted $L {\,\,}_J\!\dashv R$.
\begin{tikzcd}
	& C \\
	A && E
	\arrow[""{name=0, anchor=center, inner sep=0}, "L", from=1-2, to=2-3]
	\arrow[""{name=1, anchor=center, inner sep=0}, "R", from=2-1, to=1-2]
	\arrow["J"', from=2-1, to=2-3]
	\arrow["\dashv"{anchor=center, rotate=180}, shift left=2, draw=none, from=0, to=1]
\end{tikzcd}

Importantly, there is a bifurcation of concepts, which is not visible for ordinary adjunctions: the notion of relative adjunction is not self-dual.

## Terminology and notation

In the literature, relative adjunctions and relative coadjunctions have not been adequately distinguished, with the term "relative adjunction" frequently being used for both. However, they are distinct concepts and behave differently (albeit dually).

Similarly, the convention $L \dashv_J R$ for relative adjunctions and $L {\,\,}_J\!\dashv R$ relative coadjunctions is sometimes reversed in the literature. On this page, we follow the conventions of [AM24](#AM24), who give a more detailed history of the concept.

## Properties

- A left $J$-relative adjoint is unique up to isomorphism. A right $J$-relative adjoint is unique up to isomorphism only if $J$ is [[dense functor|dense]]. See Lemma 5.7 of [AM24](#AM24).
- A left $J$-relative adjoint preserves those colimits that $J$ preserves (Proposition 5.11 of [AM24](#AM24)). A right $J$-relative adjoint preserves limits when $J$ is dense (Proposition 5.12 of [AM24](#AM24)).
- A left relative adjoint is an _absolute [[Kan lift|lift]]_. In particular, if $L \dashv_J R$, then $L = \mathop{Lift}_R J$, and this left lift is _absolute_. Dually, for a right relative coadjoint $L {\,\,}_J\!\dashv R$, we have $R = \mathop{Rift}_L J$, and this right lift is _absolute_. Note that, for the converse to hold, we must additionally require that the lifts are _pointwise_. See Proposition 5.8 and Remark 5.9 of [AM24](#AM24).
- A relative adjunction has a unit $\eta \colon J \Rightarrow R L$; whereas a relative coadjunction has a counit $\varepsilon \colon L R \Rightarrow J$ (both may be seen to be induced from the hom-set definition, like for ordinary adjunctions). In fact, these may be used to give an alternative definition of relative adjunctions and relative coadjunctions, akin to the unit--counit formulation of an adjunction. See Lemma 5.5 of [AM24](#AM24).

### Relative monads and comonads

Just as adjunctions give rise to [[monad|monads]] and [[comonad|comonads]],

1. For relative adjunctions, if $L \dashv_J R$, then $R L$ admits the structure of a [[relative monad|monad relative to $J$]].
2. For relative coadjunctions, if $L {\,\,}_J\!\dashv R$, then $L R$ admits the structure of a [[relative comonad|comonad relative to $J$]].

(with the units and counits respectively induced as described above).

Conversely, there are anlogues of the [[Kleisli category]] and [[Eilenberg–Moore category]] for relative monads and relative comonads, which induce the relative monads and relative comonads.

## Examples ##

**ordinary adjointness**

:	An $id$-relative adjunction is simply an ordinary adjunction. Dually, an $id$-relative coadjunction is simply an ordinary adjunction.

**fully faithful functors**
:	A functor $F: A \to B$ is fully faithful iff the canonical natural transformation $1 \Rightarrow B(F{-}, F{-})$ is invertible iff there exists any such isomorphism, i.e. iff
	\[
		1 {\,\,}_F\!\dashv F
	\]

**partially defined adjoints** 
:	As remarked in the [[adjoint functor|local definition of adjoint functor]], given a functor 
	\[
		L \colon C \to E
	\]
	it may happen that $E(L(-),e)$ is [[representable functor|representable]] only for _some_ $e \in E$, but not for all of them. In that case, taking 
	\[
		J \colon A \to E
	\]
	to be the inclusion of the [[full subcategory|full subcategory]] determined by $E(L(-),e)$ representable, and defining $R \colon A \to C$ accordingly, we have
	\[
		L {\,\,}_J\!\dashv R
	\]
	This can be specialized to situations such as a category having _some_ but not all [[limit]] of some kind, partially defined [[Kan extension|extensions]], etc. See also [[free object]].

**nerves**
:	Take $A$ a locally small category, and $F\colon A \to B$ a small-admissible functor (one for which $B(Fa,b)$ is always small). The [[restricted Yoneda embedding|nerve]] of $F$ is the functor
	\[
		N_F \colon B \to \mathbf{Set}^{A^{\mathop{op}}}
	\]
	given by $N_F(b)(a) = B(Fa,b)$. The nerve forms a right adjoint to $F$ relative to the [[Yoneda embedding]]: $F \dashv_{y_A} N_F$. The universal 2-cell $\eta\colon y_A \to N_F F$ is given by the action of $F$ on morphisms:
	\[
		\eta_a \colon y_A a \to (N_F F)(a)
	\]
	at $a' \colon A$ is
	\[
		F_{a,a'}\colon A(a,a') \to B(F a, F a')
	\]
	
	Note that, when specialized to $F = 1_A$, this reduces to [[full faithfulness]] of the [[Yoneda embedding]]: first $N_{1_A} \simeq y_A$, and then:
	\[
		A(x,y) \simeq \mathbf{Set}^{A^{\mathop{op}}}(y_A x, y_A y)
	\]

	In fact, one of the axioms of a [[Yoneda structure]] on a 2-category axiomatises this situation, by requiring the existence of absolute left lifting with respect to Yoneda embeddings, as above: see [Street--Walters](#StreetWalters1978).

## Related concepts

* [[relative monad]]

## References ##

### General

A comprehensive account of relative adjunctions (covering also adjoint functors in [[enriched category theory]], and more generally [[formal category theory]]) may be found in:

* {#AM24} [[Nathanael Arkor]], [[Dylan McDermott]], _The formal theory of relative monads_, Journal of Pure and Applied Algebra 107676. (2024) &lbrack;[arXiv:2302.14014](https://arxiv.org/abs/2302.14014)&rbrack;

The original reference for relative adjunctions is:

* [[Friedrich Ulmer]], _Properties of dense and relative adjoint functors_, Journal of Algebra, **8** 1 (1968) 77-95 &lbrack;<a href="https://doi.org/10.1016/0021-8693(68)90036-7">doi:10.1016/0021-8693(68)90036-7</a>&rbrack;

Relative adjunctions were rediscovered in the context of [[relative monads]] in:

* {#ACU14} [[Thorsten Altenkirch]], [[James Chapman]], [[Tarmo Uustalu]], *Monads need not be endofunctors*, Logical Methods in Computer Science **11** 1:3 (2015) 1–40 &lbrack;[arXiv:1412.7148](https://arxiv.org/abs/1412.7148), [pdf](http://www.cs.nott.ac.uk/~txa/publ/jrelmon.pdf), <a href="https://doi.org/10.2168/LMCS-11(1:3)2015">doi:10.2168/LMCS-11(1:3)2015</a>&rbrack;

For the role of nerves in [[Yoneda structures]], see:

*  {#StreetWalters1978} [[Ross Street]], [[Bob Walters]], *Yoneda structures on 2-categories*, Journal of Algebra, **50** 2 (1978) 350-379 &lbrack;<a href="https://doi.org/10.1016/0021-8693(78)90160-6">doi:10.1016/0021-8693(78)90160-6</a>, [mendeley](http://www.mendeley.com/research/yoneda-structures-2categories/)&rbrack;

*  {#Weber2007} [[Mark Weber]] - _Yoneda structures from 2-toposes_, Appl Categor Struct. **15** (2007) 259. &lbrack;doi:10.1007/s10485-007-9079-2, [pdf](https://sites.google.com/site/markwebersmaths/home/yoneda-structures-from-2-toposes)&rbrack;

### Examples

On the [[categorical semantics]] of [[dependent product types]] as *[[relative adjoint functor|relative]]* [[right adjoints]] to [[context extension]] in [[comprehension categories]]:

* [[Michael Lindgren]], *Dependent products as relative adjoints*, Stockholm (2021) &lbrack;[[Lindgren-DependentProductsAsRelativeAdjoints.pdf:file]]&rbrack;


[[!redirects relative adjoint functors]]
[[!redirects relative right adjoint]]
[[!redirects relative left adjoint]]
[[!redirects relative right adjoints]]
[[!redirects relative left adjoints]]
[[!redirects right relative adjoint]]
[[!redirects left relative adjoint]]
[[!redirects right relative adjoints]]
[[!redirects left relative adjoints]]
[[!redirects relative adjoint]]
[[!redirects relative adjoints]]
[[!redirects relative adjunction]]
[[!redirects relative adjunctions]]
[[!redirects partial adjoint]]
[[!redirects partial adjoints]]
[[!redirects partial adjoint functor]]
[[!redirects partial adjoint functors]]
[[!redirects partial adjunction]]
[[!redirects partial adjunctions]]

[[!redirects relative coadjoint functor]]
[[!redirects relative coadjoint functors]]
[[!redirects relative right coadjoint]]
[[!redirects relative left coadjoint]]
[[!redirects relative right coadjoints]]
[[!redirects relative left coadjoints]]
[[!redirects right relative coadjoint]]
[[!redirects left relative coadjoint]]
[[!redirects right relative coadjoints]]
[[!redirects left relative coadjoints]]
[[!redirects relative coadjoint]]
[[!redirects relative coadjoints]]
[[!redirects relative coadjunction]]
[[!redirects relative coadjunctions]]