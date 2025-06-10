
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--





# Stone duality
* table of contents
{: toc}

## Idea

Stone duality is a subject comprising various [[dualities]] between [[space and quantity]] in the area of [[general topology]] and topological [[algebra]].





## Particular cases

### Locales and frames

Perhaps the most general duality falling under this heading is that between [[locales]] (on the [[space]] side) and [[frames]] (on the [[quantity]] side).  Of course, this duality is not very deep at all; the category [[Loc]] of locales is simply *defined* to be the [[opposite category|opposite]] of the category [[Frm]] of frames.  But there are several interesting dualities between [[subcategories]] of these.


### Topological spaces

Stone duality is often described for [[topological spaces]] rather than for [[locales]].  In this case, the most general duality is that between [[sober spaces]] and frames with enough points (which correspond to [[topological locale]]s).  In many cases, one requires the [[ultrafilter theorem]] (or other forms of the [[axiom of choice]]) in order for the duality to hold when applied to topological spaces, while the duality holds for locales even in [[constructive mathematics]].


### Coherent spaces and distributive lattices

Any [[distributive lattice]] generates a [[free object|free]] frame.  The locales which arise in this way can be characterized as the [[coherent locale]]s, and this gives a duality between distributive lattices and coherent locales.  Note that one must additionally restrict to "coherent maps" between coherent locales.  Also, at least assuming the [[axiom of choice]], every coherent locale is [[topological locale|topological]], so we may say "coherent space" instead.


### Priestley spaces and distributive lattices

Assuming the [[axiom of choice]], [[Priestley spaces]] are the [[opposite category]] of [[distributive lattices]]. 

### Stone spaces and Boolean algebras
 {#StoneSpacesAndBooleanAlgebras}

The duality which is due to [[Marshall Stone]], and which gives its name to the subject, is the duality between [[Stone spaces]] and [[Boolean algebras]].  Specifically, a [[distributive lattice]] is a Boolean algebra precisely when the free frame it generates is the topology of a Stone space, and any continuous map of Stone spaces is coherent.  Therefore, the category of Stone spaces is dual to the category of Boolean algebras.  The Boolean algebra corresponding to a Stone space consists of its [[clopen sets]].


This duality may be realized via a [[dualizing object]] as follows. The two-element [[Boolean algebra]] may be regarded as a Boolean algebra object $\mathbf{2}$ [[internalization|internal to]] the [[category]] of [[compact Hausdorff spaces]] $CH$. Thus, for each finitary Boolean algebra operation $\theta\colon \mathbf{2}^n \to \mathbf{2}$, there is a corresponding operation on the [[representable functor]] $CH(-, \mathbf{2}): CH^{op} \to Set$ given by 

$$CH(-, \mathbf{2})^n \cong CH(-, \mathbf{2}^n) \stackrel{CH(-, \theta)}{\to} CH(-, \mathbf{2})$$ 

and therefore we obtain a lift 

$$CH(-, \mathbf{2}): CH^{op} \to Bool$$ 

A _[[Stone space]]_ is by definition a [[totally disconnected topological space|totally disconnected]] [[compact topological space|compact]] [[Hausdorff topological space]]. Let $Stone \hookrightarrow CH$ denote the [[full subcategory]] of Stone spaces. 

+-- {: .num_theorem}
###### Theorem (Stone representation)

The representable functor restricts to an [[equivalence of categories]] $Stone^{op} \to Bool$. 
=-- 

This important theorem can be exploited to give a third description of the free Boolean algebra on a set $X$: 

$$Bool(X) \cong CH(2^X, \mathbf{2})$$ 

where $2$ denotes the 2-element compact Hausdorff space, and $2^X$ the product space $\prod_X 2$. Indeed, the inverse equivalence 

$$Bool^{op} \to Stone$$ 

takes a Boolean algebra $B$ to its [[spectrum]], i.e., the space of Boolean algebra maps $Bool(B, 2)$ (*this* $2$ is the two-element Boolean algebra $\mathbb{Z}_2$!) equipped with the [[Zariski topology]]. Applied to $B = Bool(X)$, we have 

$$Bool(B, 2) \cong Set(X, 2) = 2^X$$ 

where the Zariski topology coincides with the [[product topology]] on $2^X$. By the equivalence, we therefore retrieve $Bool(X)$ as $CH(2^X, \mathbf{2})$. This in turn is identified with the Boolean algebra of [[clopen subset]]s of the generalised [[Cantor space]] $2^X$.

A second description of the inverse equivalence $Bool^{op} \to Stone$ comes about through the yoga of [[ambimorphic object|ambimorphic objects]]. Namely, the Boolean compact Hausdorff space $\mathbf{2}$ can equally well be seen as a [compact Hausdorff object](/nlab/show/compact+Hausdorff+object#comphaus) in the category of Boolean algebras. Thus, the representable functor $Bool(-, \mathbf{2}): Bool^{op} \to Set$ lifts canonically to a functor 
$$Bool^{op} \to CH$$ 
and in fact part of the Stone representation theorem is that this factors through the inclusion $Stone \hookrightarrow CH$ as the inverse equivalence $Bool^{op} \to Stone$. In particular this lift determines the topology, providing an description alternative to the description in terms of the Zariski topology (although they are of course the same). 



An extension of the classical Stone duality to the category of Boolean spaces (= zero-dimensional locally compact Hausdorff spaces) and continuous maps (respectively, perfect maps) was obtained by G. D. Dimov (respectively, by H. P. Doctor) (see the references below). 


### Stone spaces and profinite sets
 {#StoneSpacesAndProfiniteSets}

Note that a finite [[Stone space]] is necessarily [[discrete space|discrete]], and these correspond to the finite Boolean algebras, i.e. $FinSet \simeq FinStoneTop \simeq FinBool^{op}$.  However, since Boolean algebras form a [[locally finitely presentable category]], we have $Bool \simeq Ind(FinBool) \simeq Pro(FinSet)^{op}$ (see [[ind-object]] and [[pro-object]]).  In consequence, $StoneTop \simeq Pro(FinSet)$: i.e. [[Stone spaces]] are equivalent to *[[profinite sets]]*, in this context then often called _[[profinite spaces]]_.

One way of explaining this classical Stone duality is hence via the following sequence of [[equivalences of categories]]

$$
  Bool \simeq Ind(FinBool) \simeq Ind(FinSet^{op}) \simeq Pro(FinSet)^{op}
  \,,
$$

where "[[FinSet]]" is the [[category]] of [[finite sets]], "$Ind$" stands for [[ind-objects]], "$Pro$" for [[pro-objects]] and ${}^{op}$ for the [[opposite category]] and the [[equivalence of categories|equivalence]] $FinSet^{op} \simeq FinBool$ is that discussed at _[FinSet -- Opposite category](FinSet#OppositeCategory)_.


### Stonean spaces and complete Boolean algebras

The [[category]] of [[Stonean spaces]],
i.e., compact [[extremally disconnected]] Hausdorff topological spaces
equipped with open continuous maps as morphisms,
is contravariantly equivalent to the category
of [[complete Boolean algebras]] and continuous Boolean homomorphisms
as morphisms.

See [[complete Boolean algebra]] for more information.


### Profinite algebras

If $T$ is a [[Lawvere theory]] on $Set$, we can talk about *Stone $T$-algebras*, i.e. $T$-algebras with a compatible Stone topology, and compare the resulting category $T Alg(Stone)$ with the category $Pro(Fin T Alg)$ of pro-(finite $T$-algebras).  The previous duality says that these categories are equivalent when $T$ is the identity theory.  It is also true in many other cases, such as:

* the theory of [[groups]], resulting in the rich theory of [[profinite groups]]
* the theories of [[semigroups]] and [[monoids]]
* the theory of [[rings]] (with or without 1)
* the theories of [[distributive lattices]], [[Heyting algebras]], and [[Boolean algebras]]
* the theory of $M$-sets, where $M$ is a finite monoid
* the theories of $R$-modules and $R$-algebras, where $R$ is a finite ring

However it is false for some $T$, such as:

* the theory of $\mathbb{N}$-sets, i.e. sets equipped with an endomorphism
* the theory of [[Jónsson-Tarski algebras]]
* the theory of [[lattices]]

All of these can be found in chapter VI of Johnstone's book cited below.

The corresponding fact is also notably false for [[groupoids]], i.e. $Gpd(Stone)$ is not equivalent to $Pro(FinGpd)$, in contrast to the case for groups.  (Of course, groupoids are not described by a Lawvere theory.)

## Related concepts

* [[canonical extension]]

* [[syntax - semantics duality]]

* [[abstract Stone duality]]

* [[Gelfand duality]]

* [[Isbell duality]]

* [[Stone gamut]]

## References


* [[Peter Johnstone]], _[[Stone Spaces]]_ 

* [[Olivia Caramello]], _A topos-theoretic approach to Stone-type dualities_, [arxiv/1103.3493](http://arxiv.org/abs/1103.3493) 158 pp.

* G. D. Dimov, Some generalizations of the Stone Duality Theorem, Publ. Math. Debrecen 80/3-4 (2012), 255--293.

* G. Dimov, E. Ivanova-Dimova, [[W. Tholen]], _Categorical extension of dualities: From Stone to de Vries and beyond, I._ Appl. Categ. Struct. 30, 287–329 (2022) [doi](https://doi.org/10.1007/s10485-021-09658-6)

* H. P. Doctor, _The categories of Boolean lattices, Boolean rings and Boolean spaces_, Canad. Math. Bulletin 7 (1964), 245--252 [doi](https://doi.org/10.4153/CMB-1964-022-6)

* [[Jacob Lurie]], section A.1.1 of _[[Spectral Algebraic Geometry]]_.

* {#CCGM24} [[Felix Cherubini]], [[Thierry Coquand]], [[Freek Geerligs]], [[Hugo Moeneclaey]], *A Foundation for Synthetic Stone Duality* ([arXiv:2412.03203](https://arxiv.org/abs/2412.03203))

There is a version in model theory, [[Makkai duality]],

* [[M. Makkai]], _Stone duality for first-order logic_, Adv. Math. __65__ (1987) no. 2, 97--170, <a href="http://dx.doi.org/10.1016/0001-8708(87)90020-X">doi</a>, [MR89h:03067](http://www.ams.org/mathscinet-getitem?mr=900266); _Duality and definability in first order logic_, Mem. Amer. Math. Soc. __105__ (1993), no. 503

Other variants are in

* Henrik Forssell, _First-order logical duality_, Ph.D. thesis, Carnegie Mellon U. 2008, [pdf](http://www.andrew.cmu.edu/user/awodey/students/forssell.pdf)

* Spencer Breiner, _Scheme representation for first-order logic_, Ph.D. thesis, Carnegie Mellon U. 2014, [pdf](https://www.andrew.cmu.edu/user/awodey/students/breiner.pdf)

Discussion in [[E-∞ geometry]] is in

* [[Jacob Lurie]], section A of _[[Proper Morphisms, Completions, and the Grothendieck Existence Theorem]]_

Discussion of an $(\infty, 1)$-version of Stone duality is in 

* [[Jacob Lurie]], section 3.5.3 of [[Spectral Algebraic Geometry]]

[[!redirects Stone duality]]
[[!redirects Stone dualities]]
[[!redirects Stone-type duality]]
[[!redirects Stone-type dualities]]

[[!redirects Stone spectrum]]
[[!redirects Stone spectra]]

[[!redirects Stone representation theorem]]
[[!redirects Stone representation theorems]]
[[!redirects Stone's representation theorem]]
[[!redirects Stone's representation theorems]]
[[!redirects Stone's representation theorem]]
[[!redirects Stone's representation theorems]]

[[!redirects profinite algebra]]
[[!redirects profinite algebras]]

[[!redirects Stone algebra]]
[[!redirects Stone algebras]]

[[!redirects Stone topological algebra]]
[[!redirects Stone topological algebras]]