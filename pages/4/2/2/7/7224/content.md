+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Relative adjoint functors#
* table of contents
{:toc}

## Idea ##

The notion of *relative adjoint functors* with respect to a functor $J$ is a generalization of that of [[adjoint functor]] (to which it reduces for $J$ an [[identity functor]]). 
In generalization of the [relation between adjunctions and monads](monad#RelationBetweenAdjunctionsAndMonads),
relative adjoint functors are related to [[relative monads]].


## Definition ##

### Via hom-isomorphism  ###

Fix a functor $J\colon B \to D$. Then, for a functor 

\[
	R \colon C \longrightarrow D
\] 

to have _left $J$-relative adjoint_ (or *$J$-left adjoint*) means that there is a functor 

\[ 
	L \colon B \longrightarrow C
\]

and a [[natural isomorphism]] of the ofrm

\[
  Hom_C\big(L(-),-\big) 
  \;\simeq\; 
  Hom_D\big(J(-),R(-)\big)
  \,.
\]

[[formal duality|Dually]], for $L \colon C \longrightarrow D$ to have a _$J$-right adjoint_ $R \colon B \longrightarrow C$ means that there is a [[natural isomorphism]] of the form

\[
  Hom_D\big(L(-), J(-)\big) 
   \;\simeq\; 
  Hom_C\big(-, R(-)\big)
\]

One writes

- $L {\,\,}_J\!\dashv R$ stands for $L$ being the $J$-left adjoint of $R$
- $L \dashv_J R$ stands for $R$ being the $J$-right adjoint of $L$

### Via absolute lifting ###

Just as with regular adjoints, in the unenriched setting, relative adjoints can be defined in a more conceptual way in terms of _absolute [[Kan lift|liftings]]_. We have

1. $L {\,\,}_J\!\dashv R$ if $L = \mathop{Lift}_R J$, and this left lifting is _absolute_
2. $L \dashv_J R$ if $R = \mathop{Rift}_L J$, and this right lifting is _absolute_

However, this is not true for [[enriched functors]].

## Properties ##

### asymmetry ###

The most important difference with regular adjunctions is the asymmetry of the concept. First, for $L {\,\,}_J\!\dashv R$ it makes no sense to ask for $R \dashv_J L$ (domains and comodomains do not typecheck). And secondly, and more importantly:

* **$L$ is $J$-left adjoint to $R$:** $R$ _determines_ $L$ 
* **$R$ is $J$-right adjoint to $L$:** $L$ _determines_ $R$

(this is obvious from the definition in terms of liftings). Because of this, even if most of the properties of adjunctions have a generalization to the relative setting, they do that in a one-sided way.

### unit, counit ###

Asymmetry manifests itself here: 

1. $L {\,\,}_J\!\dashv R$ yields a $J$-relative _unit_ 2-cell $\iota\colon J \to R L$
2. while $L \dashv_J R$ gives a $J$-relative _counit_ $\epsilon\colon L R \to J$

with no naturally available counterpart for them in each case. 

These 2-cells are directly provided by the definition in terms of liftings, as the universal 2-cells 

- $\iota\colon J \to R L$ given by $L = \mathop{Lift}_R J$
- $\epsilon\colon L R \to J$ given by $R = \mathop{Rift}_L J$

Alternatively, and just as with regular adjunctions, their components can be obtained from the natural hom-isomorphism: in the unit case, evaluating at $Lb$ we get a bijection

\[
	Hom_C(Lb, Lb) \simeq Hom_D(Jb, RLb)
\]

and 

\[
	\iota_b \colon J b \to R L b
\]

is given by evaluating at $1_{Lb}$ the aforementioned bijection. A completely analogous procedure yields a description of the counit for $L \dashv_J R$.

### Relative monads and comonads ###

Just as adjunctions give rise to [[monad|monads]] and [[comonad|comonads]], for relative adjoints

1. If $L {\,\,}_J\!\dashv R$, then $RL$ is a [[relative monad]]
2. If $L \dashv_J R$, then $LR$ is a [[relative comonad]]

with relative units and counits as above, respectively.

There are also relative analogues of [[Eilenberg-Moore category|Eilenberg-Moore]] and [[Kleisli category|Kleisli]] categories for these.

### Relative adjointness generalizes adjointness ###

The concept of relative adjoint functors is a generalization of the concept of adjoint functors: if a functor $R\colon C\to D$ has a left adjoint in the usual sense, then it also has a $J$-left adjoint for $J=id_D$.

## Examples ##

**fully faithful functors**
:	A functor $F: A \to B$ is fully faithful iff it is representably fully faithful iff $1_A = \mathop{Lift}_F F$, and this lifting is absolute. Thus, $F$ fully faithful can be expressed as
	\[
		1 {\,\,}_F\!\dashv F
	\]
	

**partially defined adjoints** 
:	As remarked in the [[adjoint functor|local definition of adjoint functor]], given a functor 
	\[
		L \colon C \to D
	\]
	it may happen that $Hom_D(L(-),d)$ is [[representable functor|representable]] only for _some_ $d$, but not for all of them. In that case, taking 
	\[
		J \colon B \to D
	\]
	be the inclusion of the [[full subcategory|full subcategory]] determined by $Hom_D(L(-),d)$ representable, and defining $R \colon B \to C$ accordingly, we have
	\[
		L \dashv_J R
	\]
	This can be specialized to situations such as a category having _some_ but not all [[limit|limits]] of some kind, partially defined [[Kan extension|Kan extensions]], etc. See also [[free object]].
	


**nerves**
:	Take $A$ a locally small category, and $F\colon A \to B$ a locally left-small functor (one for which $B(Fa,b)$ is always small). The _$A$-nerve_ induced by $F$ is the functor
	\[
		N_F \colon B \to \mathbf{Set}^{A^{\mathop{op}}}
	\]
	given by $N_F(b)(a) = B(Fa,b)$. It is a fundamental fact that $F = \mathop{Lift}_{N_F} y_A$ and this lifting is _absolute_; or, in relative adjoint notation, $F {\,\,}_{y_A}\!\dashv N_F$. The universal 2-cell $\iota\colon y_A \to N_F F$ is given by the action of $F$ on morphisms:
	\[
		\iota_a \colon y_A a \to (N_F F)(a)
	\]
	at $a' \colon A$ is
	\[
		F_{a,a'}\colon A(a,a') \to B(Fa, Fa')
	\]
	
	Note that when specialized to $F = 1_A$, this reduces to the [[yoneda lemma|Yoneda lemma]]: first $N_{1_A} \simeq y_A$, and then $1_A = \mathop{Lift}_{y_A} y_A$ absolute in hom-isomorphism terms reads: 
	\[
		A(x,y) \simeq \mathbf{Set}^{A^{\mathop{op}}}(y_A x, y_A y)
	\]

	One of the axioms of a [[yoneda structure|Yoneda structure]] on a 2-category abstract over this situation, by requiring the existence of $F$-nerves with respect to yoneda embeddings such that the 1-cell $F$ is an absolute left lifting as above; see [Weber](#Weber2007) or [Street--Walters](#StreetWalters1978)
.

## Related concepts

* [[relative monad]]

## References ##

### General

* [[Friedrich Ulmer]], _Properties of dense and relative adjoint functors_, Journal of Algebra, **8** 1 (1968) 77-95 &lbrack;<a href="https://doi.org/10.1016/0021-8693(68)90036-7">doi:10.1016/0021-8693(68)90036-7</a>&rbrack;

*  {#StreetWalters1978} [[Ross Street]], [[Bob Walters]], *Yoneda structures on 2-categories*, Journal of Algebra, **50** 2 (1978) 350-379 &lbrack;<a href="https://doi.org/10.1016/0021-8693(78)90160-6">doi:10.1016/0021-8693(78)90160-6</a>, [mendeley](http://www.mendeley.com/research/yoneda-structures-2categories/)&rbrack;

* {#ACU14} [[Thorsten Altenkirch]], [[James Chapman]], [[Tarmo Uustalu]], *Monads need not be endofunctors*, Logical Methods in Computer Science **11** 1:3 (2015) 1–40 &lbrack;[arXiv:1412.7148](https://arxiv.org/abs/1412.7148), [pdf](http://www.cs.nott.ac.uk/~txa/publ/jrelmon.pdf), <a href="https://doi.org/10.2168/LMCS-11(1:3)2015">doi:10.2168/LMCS-11(1:3)2015</a>&rbrack;


*  {#Weber2007} [[Mark Weber]] - _Yoneda structures from 2-toposes_, Appl Categor Struct. **15** (2007) 259. &lbrack;doi:10.1007/s10485-007-9079-2, [pdf](https://sites.google.com/site/markwebersmaths/home/yoneda-structures-from-2-toposes)&rbrack;

### Examples

On the [[categorical semantics]] of [[dependent product types]] as *[[relative adjoint functor|relative]]* [[right adjoints]] to [[context extension]] in [[comprehension categories]]:

* [[Michael Lindgren]], *Dependent products as relative adjoints*, Stockholm (2021) &lbrack;[[Lindgren-DependentProductsAsRelativeAdjoints.pdf:file]]&rbrack;



[[!redirects relative adjoint functors]]
[[!redirects relative right adjoint]]
[[!redirects relative left adjoint]]
[[!redirects relative adjoint]]
[[!redirects relative adjoints]]
[[!redirects relative adjunction]]
[[!redirects relative adjunctions]]